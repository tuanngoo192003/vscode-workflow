# Eclipse Temurin
    * An open-source Java SE build based upon OpenJDK 
    * `eclipse-temurin` refers to official container images provided on Docker Hub by the Eclipse Adoptium project

# Jammy and Alpine
 ## Alpine
    * light weight (image sizes are small, typically <10MB before adding Java)
    * uses musl libc instead of glibc, which sometimes causes compatibility issues with certain Java libraries or native dependencies.
    * if you're used to environments like EC2(Amazon Linux - glibc-based), developing with musl libc may produce subtle issues due to differences in libc implementation.
 ## Focal/Jammy/Noble
    * ubuntu based
      * Focal: Ubuntu-20.04 TLS
      * Jammy: Ubuntu-22.04 TLS
      * Noble: Ubuntu-24.04 TLS
    * more weighted
    * safer compatibility-wise
    * bigger package ecosystem