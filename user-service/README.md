KEY VALUE
MONGO_URI mongodb+srv://...
JWT_SECRET super-strong-secret-987654
PORT 8080

MONGO_URI = mongodb+srv://<user>:<password>@cluster.mongodb.net/userdb
JWT_SECRET = super-strong-secret-key-123

//Local Testing Commands:
mvn clean package
mvn spring-boot:run

export MONGO_URI="mongodb+srv://username:password@cluster0.mongodb.net/oms"
export JWT_SECRET="my-secret-123"

4️⃣ Build & Start Commands for Render

Build Command:

mvn clean package

Start Command:

java -jar target/user-service-0.0.1.jar
