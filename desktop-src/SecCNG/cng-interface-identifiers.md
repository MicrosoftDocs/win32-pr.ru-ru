---
description: Для идентификации интерфейса шифрования CNG используются следующие идентификаторы.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: Идентификаторы интерфейса CNG (BCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ebadf561df916eedde1175a39911da55628b113022378cee9e74b61d021792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908275"
---
# <a name="cng-interface-identifiers"></a>Идентификаторы интерфейса CNG

Для идентификации интерфейса шифрования CNG используются следующие идентификаторы. В CNG интерфейс определяет тип криптографических действий, поддерживаемых поставщиком. Например, поставщик может быть генератором случайных чисел или поставщиком хэширования.



| Константа/значение                                                                                                                                                                                                                                                                                             | Описание                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ \_Интерфейс шифра**</dt> <dt>0x00000001</dt> </dl>                                               | Интерфейс симметричного шифра.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ ХЭШ- \_ интерфейс**</dt> <dt>0x00000002</dt> </dl>                                                     | Хэш-интерфейс.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ 0x00000003 \_ \_ интерфейса асимметричного шифрования**</dt> <dt></dt> </dl> | Интерфейс асимметричного шифрования.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ \_ \_ Интерфейс секретного соглашения**</dt> <dt>0x00000004</dt> </dl>                | Интерфейс секретного соглашения.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ 0x00000005 \_ интерфейса подписи**</dt> <dt></dt> </dl>                                      | Интерфейс подписи.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ \_Интерфейс РНГ**</dt> <dt>0x00000006</dt> </dl>                                                        | Интерфейс генератора случайных чисел.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Интерфейс хранилища ключей**</dt> <dt>0x00010001</dt> </dl>                               | Интерфейс хранилища ключей.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ \_Интерфейс SChannel**</dt> <dt>0x00010002</dt> </dl>                                         | Интерфейс подписи SChannel.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Интерфейс подписи SChannel**</dt> <dt>0x00010003</dt> </dl>          | Интерфейс набора шифров SChannel.<br/> **Windows server 2008, Windows Vista, Windows Server 2003, Windows XP и Windows 2000:** Это значение не поддерживается.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                                                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                                                                |
| Header<br/>                   | <dl> <dt>BCrypt. h; </dt> <dt>NCrypt. h</dt> </dl> |



 

 




