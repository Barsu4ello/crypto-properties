Чтобы корректно зашифровать через командну строку(если не указать, то будет выбран файл application.properties):
mvn jasypt:encrypt -D'jasypt.encryptor.password'="secret"  -D'packaging.type'="war"  -D'jasypt.plugin.path'="file:src/main/resources/secret/secret-dev-zone.properties"
Или если мы хотим в каком-то определенном файле поработать с шифрованием(НО УБЕДИСЬ В ЛОГАХ, ЧТО НЕ БЫЛ ВЫБРАН ДЕФОЛТОВЫЙ АЛГОРИТМ PBEWITHHMACSHA512ANDAES_256 или можно без -D'jasypt.encryptor.algorithm'="PBEWithMD5AndDES"):
mvn jasypt:encrypt -D'jasypt.encryptor.password'="secret" -D'jasypt.encryptor.algorithm'="PBEWithMD5AndDES" -D'packaging.type'="war" -D'jasypt.plugin.path'="file:src/main/resources/secret/secret-de
v-zone.properties"

