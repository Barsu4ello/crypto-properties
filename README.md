Чтобы корректно зашифровать через командну строку:
mvn jasypt:encrypt -D'jasypt.encryptor.password'="pas" -D'jasypt.encryptor.algorithm'="PBEWithMD5AndDES"
Или если мы хотим в каком-то определенном файле поработать с шифрованием:
mvn jasypt:encrypt -D'jasypt.encryptor.password'="secret" -D'jasypt.encryptor.algorithm'="PBEWithMD5AndDES" -D'packaging.type'="war" -D'jasypt.plugin.path'="file:src/main/resources/secret/secret-de
v-zone.properties"

