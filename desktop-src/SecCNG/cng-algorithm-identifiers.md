---
description: Используется для распознавания стандартных алгоритмов шифрования в различных функциях и структурах CNG, таких \_ как \_ Структура reg интерфейса шифрования.
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: Идентификаторы алгоритма CNG (BCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e853d7cd0d1dd34104d3cffa20f301c11e45304c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481890"
---
# <a name="cng-algorithm-identifiers"></a>Идентификаторы алгоритма CNG

Следующие идентификаторы используются для идентификации стандартных алгоритмов шифрования в различных функциях и структурах CNG, таких как [**Структура \_ \_ reg интерфейса шифрования**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) . Сторонние поставщики могут иметь дополнительные алгоритмы, которые они поддерживают.




| Константа/значение | Описание | 
|----------------|-------------|
| <span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl><dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt><dt>"3DES"</dt></dl> | Алгоритм симметричного шифрования стандарта Triple Data Encryption Standard.<br /> Стандартный: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl><dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt><dt>"3DES_112"</dt></dl> | 112-разрядный алгоритм симметричного шифрования стандарта шифрования данных Triple.<br /> Стандартный: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl><dt><strong>BCRYPT_AES_ALGORITHM</strong></dt><dt>"AES"</dt></dl> | Алгоритм симметричного шифрования стандарта расширенного шифрования.<br /> Стандартный: FIPS 197<br /> | 
| <span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt><dt>"AES-Кмак"</dt></dl> | Симметричный алгоритм шифрования кода проверки подлинности сообщений на основе шифра AES (КМАК).<br /> Стандартный: SP 800-38B<br /><strong>Windows 8:</strong> Начинается поддержка этого алгоритма.<br /><br /> | 
| <span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt><dt>"AES-гмак"</dt></dl> | Алгоритм симметричного шифрования с кодом проверки подлинности Галоис (ГМАК) стандарта AES.<br /> Стандартный: SP800-38D<br /><strong>Windows Vista:</strong> этот алгоритм поддерживается начиная с Windows Vista с пакетом обновления 1 (SP1).<br /> | 
| <span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl><dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt><dt>L "CAPI_KDF"</dt></dl> | Алгоритм функции наследования ключа Crypto API (CAPI). Используется функциями <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>бкрипткэйдериватион</strong></a> и <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>нкрипткэйдериватион</strong></a> .<br /> | 
| <span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl><dt><strong>BCRYPT_DES_ALGORITHM</strong></dt><dt>"Des"</dt></dl> | Алгоритм симметричного шифрования стандарта шифрования данных.<br /> Standard: FIPS 46-3, FIPS 81<br /> | 
| <span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl><dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt><dt>"DESX"</dt></dl> | Алгоритм симметричного шифрования стандарта расширенного шифрования данных.<br /> Стандартный: нет<br /> | 
| <span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl><dt><strong>BCRYPT_DH_ALGORITHM</strong></dt><dt>"DH"</dt></dl> | Алгоритм обмена ключами Diffie-Hellman.<br /> Стандартный: PKCS #3<br /> | 
| <span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl><dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt><dt>"DSA"</dt></dl> | Алгоритм цифровой подписи.<br /> Стандартный: FIPS 186-2<br /><strong>Windows 8:</strong> начиная с Windows 8 этот алгоритм поддерживает FIPS 186-3. Ключи, меньшие или равные 1024 бит, придерживаются FIPS 186-2 и ключи больше 1024 в FIPS 186-3.<br /> | 
| <span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt><dt>"ECDH_P256"</dt></dl> | В 256-разрядной простой эллиптической кривой Diffie-Hellman алгоритм обмена ключами.<br /> Стандартный: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt><dt>"ECDH_P384"</dt></dl> | В 384-разрядной простой эллиптической кривой Diffie-Hellman алгоритм обмена ключами.<br /> Стандартный: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt><dt>"ECDH_P521"</dt></dl> | В 521-разрядной простой эллиптической кривой Diffie-Hellman алгоритм обмена ключами.<br /> Стандартный: SP800-56A<br /> | 
| <span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt><dt>"ECDSA_P256"</dt></dl> | 256-разрядный алгоритм цифровой подписи эллиптической кривой (FIPS 186-2).<br /> Стандартный: FIPS 186-2, X 9.62<br /> | 
| <span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt><dt>"ECDSA_P384"</dt></dl> | 384-разрядный алгоритм цифровой подписи эллиптической кривой (FIPS 186-2).<br /> Стандартный: FIPS 186-2, X 9.62<br /> | 
| <span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt><dt>"ECDSA_P521"</dt></dl> | 521-разрядный алгоритм цифровой подписи эллиптической кривой (FIPS 186-2).<br /> Стандартный: FIPS 186-2, X 9.62<br /> | 
| <span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl><dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt><dt>"MD2"</dt></dl> | Хэш-алгоритм MD2.<br /> Стандартный: RFC 1319<br /> | 
| <span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl><dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt><dt>MD4</dt></dl> | Хэш-алгоритм MD4.<br /> Стандартный: RFC 1320<br /> | 
| <span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl><dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt><dt>MD5</dt></dl> | Хэш-алгоритм MD5.<br /> Стандартный: RFC 1321<br /> | 
| <span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl><dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt><dt>"RC2"</dt></dl> | Алгоритм симметричного шифрования RC2.<br /> Стандартный: RFC 2268<br /> | 
| <span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl><dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt><dt>RC4</dt></dl> | Алгоритм симметричного шифрования RC4.<br /> Стандартный: различные<br /> | 
| <span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl><dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt><dt>"РНГ"</dt></dl> | Алгоритм генератора случайных чисел.<br /> Standard: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br /><blockquote>[!Note]<br />начиная с версии Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008 генератор случайных чисел основан на режиме счетчика AES, указанном в стандарте NIST SP 800-90.</blockquote><br /><strong>Windows Vista:</strong> Генератор случайных чисел основан на генераторе случайных чисел на основе хэша, указанном в стандарте FIPS 186-2.<br /><strong>Windows 8:</strong> начиная с Windows 8 алгоритм рнг поддерживает FIPS 186-3. Ключи, меньшие или равные 1024 бит, придерживаются FIPS 186-2 и ключи больше 1024 в FIPS 186-3.<br /> | 
| <span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl><dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt><dt>"дуалекрнг"</dt></dl> | Алгоритм генератора случайных чисел с двумя эллиптическими кривыми. <br /> Стандартный: SP800-90.<br /><strong>Windows 8:</strong> начиная с Windows 8 алгоритм EC рнг поддерживает FIPS 186-3. Ключи, меньшие или равные 1024 бит, придерживаются FIPS 186-2 и ключи больше 1024 в FIPS 186-3.<br /><strong>Windows 10:</strong> начиная с Windows 10 алгоритм генератора случайных чисел на основе двух эллиптических кривых был удален. Существующие применения этого алгоритма будут продолжать работать. Однако генератор случайных чисел основан на режиме счетчика AES, указанном в стандарте NIST SP 800-90. Новый код должен использовать <strong>BCRYPT_RNG_ALGORITHM</strong>, поэтому рекомендуется изменить существующий код для использования <strong>BCRYPT_RNG_ALGORITHM</strong>. <br /> | 
| <span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl><dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt><dt>"FIPS186DSARNG"</dt></dl> | Алгоритм генератора случайных чисел, подходящий для DSA (алгоритм цифровых подписей). <br /> Стандартный: FIPS 186-2.<br /><strong>Windows 8:</strong> Начинается поддержка FIPS 186-3.<br /> | 
| <span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl><dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt><dt>RSA</dt></dl> | Алгоритм открытого ключа RSA. <br /> Стандартная версия: PKCS #1 версии 1.5 и 2.0.<br /> | 
| <span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl><dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt><dt>"RSA_SIGN"</dt></dl> | Алгоритм подписи RSA. Этот алгоритм в настоящее время не поддерживается. Для выполнения операций подписывания RSA можно использовать алгоритм <strong>BCRYPT_RSA_ALGORITHM</strong> . <br /> Стандартная версия: PKCS #1 версии 1.5 и 2.0.<br /> | 
| <span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl><dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt><dt>SHA1</dt></dl> | 160-разрядный алгоритм SHA. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl><dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt><dt>SHA256</dt></dl> | 256-разрядный алгоритм SHA.<br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl><dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt><dt>"SHA384"</dt></dl> | 384-разрядный алгоритм SHA. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl><dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt><dt>"SHA512"</dt></dl> | 512-разрядный алгоритм SHA. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl><dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt><dt>L "SP800_108_CTR_HMAC"</dt></dl> | Режим счетчика, алгоритм формирования ключа кода проверки подлинности сообщений на основе хэша (HMAC). Используется функциями <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>бкрипткэйдериватион</strong></a> и <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>нкрипткэйдериватион</strong></a> .<br /> | 
| <span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl><dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt><dt>L "SP800_56A_CONCAT"</dt></dl> | Алгоритм функции формирования ключа SP800-56A. Используется функциями <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>бкрипткэйдериватион</strong></a> и <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>нкрипткэйдериватион</strong></a> .<br /> | 
| <span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl><dt><strong>BCRYPT_PBKDF2_ALGORITHM</strong></dt><dt>L "PBKDF2"</dt></dl> | Алгоритм наследования ключа на основе пароля 2 (PBKDF2). Используется функциями <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>бкрипткэйдериватион</strong></a> и <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>нкрипткэйдериватион</strong></a> .<br /> | 
| <span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt><dt>"ECDSA"</dt></dl> | Универсальный алгоритм цифровых подписей эллиптических кривых (Дополнительные сведения см. в разделе <strong>"Примечания"</strong> ). <br /> Стандартный: ANSI X 9.62.<br /> | 
| <span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt><dt>"ECDH"</dt></dl> | Универсальный простой эллиптической кривой Diffie-Hellman алгоритм обмена ключами (Дополнительные сведения см. в разделе <strong>"Примечания"</strong> ). <br /> Стандартный: SP800-56A.<br /> | 
| <span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl><dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt><dt>"XTS-AES"</dt></dl> | Алгоритм симметричного шифрования стандарта расширенного шифрования в режиме XTS. <br /> Standard: SP-800-38E, IEEE STD 1619-2007.<br /><strong>Windows 10:</strong> Начинается поддержка этого алгоритма.<br /> | 




## <a name="remarks"></a>Комментарии

Чтобы использовать алгоритм **BCrypt \_ ECDSA \_ алгоритм** или **BCrypt \_ ECDH \_**, вызовите [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) с помощью **\_ \_ алгоритма BCrypt ECDSA** или с помощью **\_ \_ алгоритма BCrypt ECDH** в качестве *псзалгид*. Затем используйте [**бкриптсетпроперти**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) , чтобы задать для свойства " **\_ \_ \_ имя кривой ECC** " с именованным алгоритмом, указанным в CNG именованные кривые.

Для непосредственного определения пользовательских параметров эллиптической кривой используйте [**бкриптсетпроперти**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) , чтобы установить свойство **\_ \_ параметров BCRYPT ECC** . скачайте [комплект разработчика Windows 10 поставщика служб шифрования (кпдк)](https://www.microsoft.com/download/details.aspx?id=30688) для получения дополнительных сведений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>BCrypt. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**нкрипткреатеперсистедкэй**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




