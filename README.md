<?xml version="1.0" encoding="UTF-8"?>

<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd">
  <localRepository>D:\apache-maven-3.3.9\.m2\repository</localRepository>
  <mirrors>
		<!-- mirror | Specifies a repository mirror site to use instead of a given 
			repository. The repository that | this mirror serves has an ID that matches 
			the mirrorOf element of this mirror. IDs are used | for inheritance and direct 
			lookup purposes, and must be unique across the set of mirrors. | -->
		<mirror>
			<id>nexus-osc</id>
			<mirrorOf>central</mirrorOf>
			<name>Nexus osc</name>
			<url>http://maven.oschina.net/content/groups/public/</url>
		</mirror>
		<mirror>
			<id>nexus-osc-thirdparty</id>
			<mirrorOf>thirdparty</mirrorOf>
			<name>Nexus osc thirdparty</name>
			<url>http://maven.oschina.net/content/repositories/thirdparty/</url>
		</mirror>
		<mirror>  
			  <id>repo2</id>  
			  <mirrorOf>central</mirrorOf>  
			  <name>Human Readable Name for this Mirror.</name>  
			  <url>http://repo2.maven.org/maven2/</url>  
		</mirror>  
		<mirror>  
			  <id>ui</id>  
			  <mirrorOf>central</mirrorOf>  
			  <name>Human Readable Name for this Mirror.</name>  
			 <url>http://uk.maven.org/maven2/</url>  
		</mirror>  
		<mirror>  
			  <id>ibiblio</id>  
			  <mirrorOf>central</mirrorOf>  
			  <name>Human Readable Name for this Mirror.</name>  
			 <url>http://mirrors.ibiblio.org/maven2/</url>  
		</mirror>  
		<mirror>  
			  <id>jboss-public-repository-group</id>  
			  <mirrorOf>central</mirrorOf>  
			  <name>JBoss Public Repository Group</name>  
			 <url>http://repository.jboss.org/nexus/content/groups/public</url>  
		</mirror>
	</mirrors>
	<profiles>
		<profile>
			<id>jdk-1.7</id>

			<activation>
				<jdk>1.7</jdk>
			</activation>

			<repositories>
				<repository>
					<id>nexus</id>
					<name>local private nexus</name>
					<url>http://maven.oschina.net/content/groups/public/</url>
					<releases>
						<enabled>true</enabled>
					</releases>
					<snapshots>
						<enabled>false</enabled>
					</snapshots>
				</repository>
			</repositories>
			<pluginRepositories>
				<pluginRepository>
					<id>nexus</id>
					<name>local private nexus</name>
					<url>http://maven.oschina.net/content/groups/public/</url>
					<releases>
						<enabled>true</enabled>
					</releases>
					<snapshots>
						<enabled>false</enabled>
					</snapshots>
				</pluginRepository>
			</pluginRepositories>
		</profile>
	</profiles>
</settings>
