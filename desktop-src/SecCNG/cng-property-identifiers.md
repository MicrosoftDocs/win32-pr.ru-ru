---
description: Используется с функциями BCryptGetProperty и Бкриптсетпроперти для обнаружения свойства.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Идентификаторы свойств примитивов шифрования (BCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896738"
---
# <a name="cryptography-primitive-property-identifiers"></a>Идентификаторы свойств примитивов шифрования

Для обнаружения свойства используются следующие значения с функциями [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) и [**бкриптсетпроперти**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_имя алгоритма BCRYPT \_**
</dt> <dd> <dl> <dt>

L "AlgorithmName"
</dt> <dt>



Строка в Юникоде, заканчивающаяся нулем и содержащая имя алгоритма.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**\_длина тега проверки подлинности BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "Аустагленгс"
</dt> <dt>



Длина тега проверки подлинности, поддерживаемая алгоритмом. Это свойство представляет структуру [**структуры \_ проверки подлинности \_ тегов \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Это свойство применяется только к алгоритмам.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_Длина блока \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Блоккленгс"
</dt> <dt>



Размер блока шифра в байтах для алгоритма. Это свойство применимо только к алгоритмам блочного шифрования. Этот тип данных — **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_ \_ список размеров блоков \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Блокксизелист"
</dt> <dt>



Список длин блоков, поддерживаемых алгоритмом шифрования. Этот тип данных является массивом типов **DWORD**. Количество элементов в массиве можно определить, разделив число байтов, полученных размером одного **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_режим цепочки \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Чаинингмоде"
</dt> <dt>



Указатель на строку в Юникоде, завершающуюся нулем, которая представляет режим цепочки алгоритма шифрования. Это свойство может быть задано для обработчика алгоритма или для одного из следующих значений.



| Идентификатор                   | Значение                         | Описание                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_режим цепочки BCRYPT \_ \_ CBC** | L "Чаинингмодекбк"<br/> | Устанавливает режим цепочки алгоритма для [*шифрования цепочек блоков*](/windows/desktop/SecGloss/c-gly).<br/>            |
| **\_CCM в \_ режиме ЦЕПОЧКи BCRYPT \_** | L "Чаинингмодеккм"<br/> | Задает для алгоритма режим цепочки "Счетчик" с помощью CBC-MAC Mode (CCM). **Windows Vista:** Это значение поддерживается начиная с Windows Vista с пакетом обновления 1 (SP1).<br/> <br/> |
| **\_CFB режим цепочки BCRYPT \_ \_** | L "Чаинингмодекфб"<br/> | Задает режим цепочки алгоритма для [*шифрования отзывов*](/windows/desktop/SecGloss/c-gly).<br/>                              |
| **\_режим цепочки BCRYPT \_ \_ ECB** | L "Чаинингмодикб"<br/> | Задает для алгоритма режим цепочки " [*электронный режимом*](/windows/desktop/SecGloss/e-gly)".<br/>                  |
| **\_gcm в \_ режиме ЦЕПОЧКи BCRYPT \_** | L "Чаинингмодегкм"<br/> | Устанавливает режим цепочки алгоритма в режим Галоис/Counter (GCM). **Windows Vista:** Это значение поддерживается начиная с Windows Vista с пакетом обновления 1 (SP1).<br/> <br/>       |
| **\_режим цепочки BCRYPT в \_ \_ НД**  | L "Чаинингмоден/A"<br/> | Алгоритм не поддерживает создание цепочек.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**\_Параметры BCRYPT DH \_**
</dt> <dd> <dl> <dt>

L "Дхпараметерс"
</dt> <dt>



Указывает параметры для использования с ключом Diffie-Hellman. Этот тип данных является указателем на структуру [**\_ \_ \_ заголовков параметра BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Это свойство может быть задано только и должно быть установлено для ключа до завершения выполнения ключа.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**Параметры "BCRYPT \_ DSA" \_**
</dt> <dd> <dl> <dt>

L "Дсапараметерс"
</dt> <dt>



Указывает параметры для использования с ключом DSA. Это свойство является [**\_ \_ \_ заголовком параметра BCrypt DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) или структурой [**\_ \_ \_ заголовка \_ 2 параметра BCrypt DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Это свойство может быть задано только и должно быть установлено для ключа до завершения выполнения ключа.

**Windows 8:** Начиная с Windows 8, это свойство может иметь структуру [**\_ \_ \_ заголовка \_ версии 2 параметра DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Используйте эту структуру, если размер ключа превышает 1024 бит и меньше или равен 3072 бит. Если размер ключа больше или равен 512, но меньше или равен 1024 бит, используйте структуру [**\_ \_ \_ заголовка параметра BCRYPT DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**\_Длина действующего \_ ключа BCRYPT \_**
</dt> <dd> <dl> <dt>

L "Еффективекэйленгс"
</dt> <dt>



Размер (в битах) эффективной длины ключа RC2. Этот тип данных — **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_ \_ Длина блока хэша \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Хашблоккленгс"
</dt> <dt>



Размер (в байтах) блока для хэша. Это свойство применяется только к алгоритмам хэширования. Этот тип данных — **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_Длина ХЭША \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Хашдижестленгс"
</dt> <dt>



Размер (в байтах) хэш-значения поставщика хэша. Этот тип данных — **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_список хэш-кодов \_ объекта BCRYPT \_**
</dt> <dd> <dl> <dt>

L "Хашоидлист"
</dt> <dt>



Список [*идентификаторов объектов*](/windows/desktop/SecGloss/o-gly) хэширования, закодированных в [*der*](/windows/desktop/SecGloss/d-gly). Это свойство представляет собой [**структуру \_ \_ списка объекта BCRYPT OID**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) . Это свойство может быть доступно только для чтения.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_вектор инициализации \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "IV"
</dt> <dt>



Содержит [*вектор инициализации*](/windows/desktop/SecGloss/i-gly) (IV) для ключа. Это свойство применяется только к ключам.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_Длина ключа \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "KeyLength"
</dt> <dt>



Размер значения ключа поставщика симметричного ключа (в битах). Этот тип данных — **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_Длина ключей \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Кэйленгсс"
</dt> <dt>



Длина ключа, поддерживаемая алгоритмом. Это свойство представляет структуру [**структуры \_ ключей \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Это свойство применяется только к алгоритмам.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**\_ \_ длина объекта ключа \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Кэйобжектленгс"
</dt> <dt>



Это свойство не используется. Для получения этих сведений используется свойство **\_ \_ Length объекта BCRYPT** .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_сила ключа \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Кэйстренгс"
</dt> <dt>



Число битов в ключе. Этот тип данных — **DWORD**. Это свойство применяется только к ключам.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_ \_ Длина блока сообщений \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Мессажеблоккленгс"
</dt> <dt>



Это можно задать для любого маркера ключа, в котором установлен режим цепочки CFB. По умолчанию для этого свойства задано значение 1 для 8-битного CFB. Если задать для него размер блока в байтах, то CFB будет использоваться полностью. Для ключей XTS он используется для задания размера (в байтах) единицы данных XTS (обычно 512 или 4096).


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT \_ Длина множественных \_ объектов \_**
</dt> <dd> <dl> <dt>

L "Мултиобжектленгс"
</dt> <dt>



Это свойство возвращает [**\_ \_ \_ \_ структуру объекта BCRYPT с несколькими объектами**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), которая содержит сведения, необходимые для вычисления размера буфера объекта. Это свойство поддерживается только в версиях операционной системы, поддерживающих функцию [**бкрипткреатемултихаш**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_длина объекта \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Обжектленгс"
</dt> <dt>



Размер (в байтах) подобъекта поставщика. Этот тип данных — **DWORD**. В настоящее время поставщики алгоритмов хэширования и симметричного шифра используют выделенные вызывающими буферами буферы для хранения своих подобъектов. Например, поставщик хэша требует выделения памяти для хэш-объекта, полученного с помощью функции [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Это свойство предоставляет размер буфера для объекта поставщика, чтобы можно было выделить память для объекта, созданного поставщиком.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_схемы заполнения BCRYPT \_**
</dt> <dd> <dl> <dt>

L "Паддингсчемес"
</dt> <dt>



Представляет схему заполнения поставщика алгоритма RSA. Этот тип данных — **DWORD**. Это может быть одно из следующих значений.



| Идентификатор                             | Значение      | Описание                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **\_поддерживаемый \_ маршрутизатор Pad (BCRYPT) \_**     | 0x00000001 | Поставщик поддерживает дополнение, добавленное маршрутизатором.         |
| **\_Поддерживаемая \_ панель \_ PKCS1 (BCRYPT) \_** | 0x00000002 | Поставщик поддерживает схему заполнения шифрования PKCS1. |
| **\_Поддержка BCRYPT \_ Pad \_ PKCS1 \_ SIG** | 0x00000004 | Поставщик поддерживает схему заполнения подписи PKCS1.  |
| **поддерживаемый для заполнения заполненный заполненный \_ \_ \_ OAEP**       | 0x00000008 | Поставщик поддерживает схему заполнения OAEP.             |
| **\_поддерживаемая \_ панелью \_ поддержки BCRYPT**        | 0x00000010 | Поставщик поддерживает схему заполнения PSS.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_маркер поставщика \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Провидерхандле"
</dt> <dt>



Маркер поставщика CNG, который создал объект, переданный в параметре *хобжект* . Этот тип данных является **\_ \_ обработчиком алгоритма BCRYPT**. Это свойство может быть извлечено только. его нельзя задать.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**\_Длина подписи \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "Сигнатуреленгс"
</dt> <dt>



Размер (в байтах) длины подписи для ключа. Этот тип данных — **DWORD**. Это свойство применяется только к ключам. Это свойство может быть извлечено только. его нельзя задать.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>BCrypt. h</dt> </dl> |



 

