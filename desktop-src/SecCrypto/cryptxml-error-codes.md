---
description: Ниже приведены коды ошибок времени выполнения, определенные в Криптксмл. h, которые могут возвращаться функциями Криптксмл.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Коды ошибок Криптксмл (Криптксмл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5906c406f14081844ddce042f0e170668950e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664476"
---
# <a name="cryptxml-error-codes"></a>Коды ошибок Криптксмл

Ниже приведены коды ошибок времени выполнения, определенные в Криптксмл. h, которые могут возвращаться функциями Криптксмл.



| Константа/значение                                                                                                                                                                                                                                                                             | Описание                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**Шифрования \_ XML \_ E \_ Large**</dt> <dt>0x80092101L</dt> </dl>                                               | Указано слишком большое значение.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**Шифрования \_ 0x80092103L \_ \_ кодирования XML E**</dt> <dt></dt> </dl>                                      | Указанная кодировка XML не поддерживается.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**Шифрования \_ 0x80092104L \_ \_ алгоритма XML E**</dt> <dt></dt> </dl>                                   | Указанный алгоритм XML не поддерживается.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**Шифрования \_ \_ \_ Преобразование XML E**</dt> <dt>0x80092105L</dt> </dl>                                   | Указанное преобразование не поддерживается.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**Шифрования \_ 0x80092106L XML \_ E \_ Handle**</dt> <dt></dt> </dl>                                            | Указан недопустимый обработчик.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**Шифрования \_ 0x80092107L \_ \_ операции XML E**</dt> <dt></dt> </dl>                                   | Недопустимая операция.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**Шифрования \_ \_ \_ Неразрешенная \_ ссылка на 0x80092108L XML E**</dt> <dt></dt> </dl> | Не удалось разрешить элемент **ссылки** .<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**Шифрования \_ \_ \_ Недопустимый \_ дайджест**</dt> <dt>0x80092109L</dt> для XML E </dl>                   | Недопустимое значение дайджеста.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**Шифрования \_ \_ \_ Недопустимый \_ 0x8009210AL подписи XML E**</dt> <dt></dt> </dl>          | Недопустимое значение подписи.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**Шифрования \_ \_ \_ \_ Не удалось 0x8009210BL хэш-код XML E**</dt> <dt></dt> </dl>                            | Не удалось создать или вычислить хэш.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**Шифрования \_ \_ \_ \_ Не удалось подписать XML E**</dt> <dt>0x8009210CL</dt> </dl>                            | Сбой операции криптографической подписи.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**Шифрования \_ \_Проверка XML \_ E \_ не пройдена**</dt> <dt>0x8009210DL</dt> </dl>                      | Сбой проверки сигнатуры.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**Шифрования \_ \_ \_ Слишком \_ много \_ подписей в формате XML E**</dt> <dt>0x8009210EL</dt> </dl>   | Число элементов **сигнатуры** в документе превысило максимально допустимый предел для обработки.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**Шифрования \_ \_ \_ Недопустимый \_ KEYVALUE 0x8009210FL XML E**</dt> <dt></dt> </dl>             | Указано недопустимое значение ключа.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**Шифрования \_ XML \_ E \_ непредвиденный 0x80092110L \_ XML**</dt> <dt></dt> </dl>                   | Обнаружен недопустимый или непредвиденный XML.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**Шифрования \_ 0x80092111L \_ - \_ подпись XML E**</dt> <dt></dt> </dl>                                            | Не удалось разместить ключ подписывания.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**Шифрования \_ 0x80092112L \_ \_ без \_ уникального \_ идентификатора XML E**</dt> <dt></dt> </dl>                     | Найден неуникальный атрибут **ID** .<br/>                                                                 |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Криптксмл. h</dt> </dl> |



 

 




