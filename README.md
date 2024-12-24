Чтобы корректно зашифровать через командну строку:
mvn jasypt:encrypt -D'jasypt.encryptor.password'="pas" -D'jasypt.encryptor.algorithm'="PBEWithMD5AndDES"
