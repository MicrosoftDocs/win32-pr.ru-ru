---
description: Начиная с Windows 10 CNG поддерживает следующие именованные эллиптические кривые (ANSI X 9.62, X 9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Именованные эллиптические кривые CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896741"
---
# <a name="cng-named-elliptic-curves"></a>CNG с именем "эллиптические кривые"

Начиная с Windows 10 CNG поддерживает следующие именованные эллиптические кривые (ANSI X 9.62, X 9.63, FIPS 186-2).

<dl> <dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**\_ \_ Кривая ECC BCRYPT \_ 25519**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------|
| Имя              | curve25519                                                  |
| Standard          | [Кривая 25519](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| Размер ключа (в битах)   | 255                                                         |
| Поддерживается TLS       |                                                             |
| Идентификаторы объектов | Нет                                                        |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**\_ \_ BRAINPOOLP160R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP160r1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 160                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.1                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP160T1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP160t1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 160                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.2                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**\_ \_ BRAINPOOLP192R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP192r1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 192                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.3                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**\_ \_ BRAINPOOLP192T1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP192t1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 192                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.4                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**\_ \_ BRAINPOOLP224R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP224r1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 224                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.5                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**\_ \_ BRAINPOOLP224T1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP224t1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 224                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.6                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**\_ \_ BRAINPOOLP256R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP256r1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 256                                                                                                               |
| Поддерживается TLS       | Да                                                                                                               |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.7                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**\_ \_ BRAINPOOLP256T1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP256t1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 256                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.8                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**\_ \_ BRAINPOOLP320R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP320r1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 320                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.9                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**\_ \_ Кривая ECC BCRYPT \_ BRAINPOOLP32 0T1**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP320t1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 320                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.10                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP384R1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP384r1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 384                                                                                                               |
| Поддерживается TLS       | Да                                                                                                               |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.11                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**\_ \_ BRAINPOOLP384T1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP384t1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 384                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.12                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**\_ \_ BRAINPOOLP512R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP512r1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 512                                                                                                               |
| Поддерживается TLS       | Да                                                                                                               |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.13                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**\_ \_ BRAINPOOLP512T1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Имя              | brainpoolP512t1                                                                                                   |
| Standard          | [Генерирование кривых ECC Brainpool Standard и создание кривых](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Размер ключа (в битах)   | 512                                                                                                               |
| Поддерживается TLS       | Нет                                                                                                                |
| Идентификаторы объектов | 1.3.36.3.3.2.8.1.1.14                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ \_ \_ EC192WAPI кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|----------------------------------------------------------------|
| Имя              | ec192wapi                                                      |
| Standard          | Китайский национальный стандарт для беспроводных локальных сетей (GB 15629.11-2003) |
| Размер ключа (в битах)   | 192                                                            |
| Поддерживается TLS       | Нет                                                             |
| Идентификаторы объектов | 1.2.156.11235.1.1.2.1                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**\_ \_ NISTP192 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Имя              | nistP192                                                                                                                     |
| Standard          | [Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Размер ключа (в битах)   | 192                                                                                                                          |
| Поддерживается TLS       | Да                                                                                                                          |
| Идентификаторы объектов | 1.2.840.10045.3.1.1                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Имя              | nistP224                                                                                                                     |
| Standard          | [Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Размер ключа (в битах)   | 224                                                                                                                          |
| Поддерживается TLS       | Да                                                                                                                          |
| Идентификаторы объектов | 1.3.132.0.33                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**\_ \_ NISTP256 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Имя              | nistP256                                                                                                                     |
| Standard          | [Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Размер ключа (в битах)   | 256                                                                                                                          |
| Поддерживается TLS       | Да                                                                                                                          |
| Идентификаторы объектов | 1.2.840.10045.3.1.7                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Имя              | nistP384                                                                                                                     |
| Standard          | [Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Размер ключа (в битах)   | 384                                                                                                                          |
| Поддерживается TLS       | Да                                                                                                                          |
| Идентификаторы объектов | 1.3.132.0.34                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**\_ \_ NISTP521 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Имя              | nistP521                                                                                                                     |
| Standard          | [Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Размер ключа (в битах)   | 521                                                                                                                          |
| Поддерживается TLS       | Да                                                                                                                          |
| Идентификаторы объектов | 1.3.132.0.35                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Имя              | numsP256t1                                                                                                                              |
| Standard          | [Спецификация выбора кривой и поддерживаемые параметры кривой в MSR Екклиб](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Размер ключа (в битах)   | 256                                                                                                                                     |
| Поддерживается TLS       | Нет                                                                                                                                      |
| Идентификаторы объектов | Нет                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Имя              | numsP384t1                                                                                                                              |
| Standard          | [Спецификация выбора кривой и поддерживаемые параметры кривой в MSR Екклиб](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Размер ключа (в битах)   | 384                                                                                                                                     |
| Поддерживается TLS       | Нет                                                                                                                                      |
| Идентификаторы объектов | Нет                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**\_ \_ NUMSP512T1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Имя              | numsP512t1                                                                                                                              |
| Standard          | [Спецификация выбора кривой и поддерживаемые параметры кривой в MSR Екклиб](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Размер ключа (в битах)   | 512                                                                                                                                     |
| Поддерживается TLS       | Нет                                                                                                                                      |
| Идентификаторы объектов | Нет                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP160k1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 160                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.9                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP160r1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 160                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.8                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP160r2                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 160                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.30                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**\_ \_ SECP192K1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP192k1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 192                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.31                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP192r1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 192                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.2.840.10045.3.1.1                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**\_ \_ SECP224K1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP224k1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 224                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.32                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**\_ \_ SECP224R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP224r1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 224                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.33                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**\_ \_ SECP256K1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP256k1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 256                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.10                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**\_ \_ SECP256R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP256r1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 256                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.2.840.10045.3.1.7                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP384r1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 384                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.34                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**\_ \_ SECP521R1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Имя              | secP521r1                                                                       |
| Standard          | [Рекомендуемые параметры домена эллиптической кривой](https://www.secg.org/sec2-v2.pdf) |
| Размер ключа (в битах)   | 521                                                                             |
| Поддерживается TLS       | Да                                                                             |
| Идентификаторы объектов | 1.3.132.0.35                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**\_ \_ WTLS12 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|--------------|
| Имя              | wtls12       |
| Standard          | втлс         |
| Размер ключа (в битах)   | 224          |
| Поддерживается TLS       | Нет           |
| Идентификаторы объектов | 1.3.132.0.33 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**\_ \_ WTLS7 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|--------------|
| Имя              | wtls7        |
| Standard          | втлс         |
| Размер ключа (в битах)   | 160          |
| Поддерживается TLS       | Нет           |
| Идентификаторы объектов | 1.3.132.0.30 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------|
| Имя              | wtls9         |
| Standard          | втлс          |
| Размер ключа (в битах)   | 160           |
| Поддерживается TLS       | Нет            |
| Идентификаторы объектов | 2.23.43.1.4.9 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**\_ \_ X962P192V1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------|
| Имя              | x962P192v1          |
| Standard          | ANSI X 9.62          |
| Размер ключа (в битах)   | 192                 |
| Поддерживается TLS       | Нет                  |
| Идентификаторы объектов | 1.2.840.10045.3.1.1 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ \_ \_ X962P192V2 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------|
| Имя              | x962P192v2          |
| Standard          | ANSI X 9.62          |
| Размер ключа (в битах)   | 192                 |
| Поддерживается TLS       | Нет                  |
| Идентификаторы объектов | 1.2.840.10045.3.1.2 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**\_ \_ X962P192V3 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------|
| Имя              | x962P192v3          |
| Standard          | ANSI X 9.62          |
| Размер ключа (в битах)   | 192                 |
| Поддерживается TLS       | Нет                  |
| Идентификаторы объектов | 1.2.840.10045.3.1.3 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ \_ \_ X962P239V1 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------|
| Имя              | x962P239v1          |
| Standard          | ANSI X 9.62          |
| Размер ключа (в битах)   | 239                 |
| Поддерживается TLS       | Нет                  |
| Идентификаторы объектов | 1.2.840.10045.3.1.4 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ \_ \_ X962P239V2 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------|
| Имя              | x962P239v2          |
| Standard          | ANSI X 9.62          |
| Размер ключа (в битах)   | 239                 |
| Поддерживается TLS       | Нет                  |
| Идентификаторы объектов | 1.2.840.10045.3.1.5 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ \_ \_ X962P239V3 кривой ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------|
| Имя              | x962P239v3          |
| Standard          | ANSI X 9.62          |
| Размер ключа (в битах)   | 239                 |
| Поддерживается TLS       | Нет                  |
| Идентификаторы объектов | 1.2.840.10045.3.1.6 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**\_ \_ X962P256V1 кривая \_ ECC**</dt> <dd> <dl> <dt> 

| Требование | Значение |
|-------------------|---------------------|
| Имя              | x962P256v1          |
| Standard          | ANSI X 9.62          |
| Размер ключа (в битах)   | 256                 |
| Поддерживается TLS       | Нет                  |
| Идентификаторы объектов | 1.2.840.10045.3.1.7 |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы использовать именованную кривую, вызовите [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) , **используя \_ \_ алгоритм BCrypt ECDSA** или **BCrypt \_ ECDH \_** в качестве идентификатора алгоритма. Затем вызовите [**бкриптсетпроперти**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) и задайте для свойства " **\_ \_ \_ название кривой с кодом коррекции ошибок** " одну из приведенных выше кривых или именованных кривых, зарегистрированных на компьютере, как показано в `certutil -displayEccCurve` команде.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                |
| Header<br/>                   | <dl> <dt>BCrypt. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**нкрипткреатеперсистедкэй**](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




