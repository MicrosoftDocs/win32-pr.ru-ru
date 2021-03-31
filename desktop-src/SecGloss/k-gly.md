---
description: Содержит определения терминов безопасности, начинающихся с буквы K.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: K (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7d1b474b774b5cdb7a0b8d05a512a8d291573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998888"
---
# <a name="k-security-glossary"></a>K (глоссарий по безопасности)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [р](h-gly.md) [. J](i-gly.md) K [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**кка**
</dt> <dd>

См. *раздел центр сертификации ключей*.

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**KDC**
</dt> <dd>

См. *центр распространения ключей*.

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**кеа**
</dt> <dd>

См. *раздел алгоритм обмена ключами*.

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Протокол Kerberos**
</dt> <dd>

Протокол, определяющий порядок взаимодействия клиентов с сетевой службой проверки подлинности. Клиенты получают билеты в центре распространения ключей Kerberos и предъявляют их серверам при установлении соединений. Билеты Kerberos представляют собой сетевые учетные данные клиента.

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**большой двоичный объект ключа**
</dt> <dd>

Большой двоичный объект, содержащий зашифрованный закрытый ключ. Ключевые BLOB-объекты предоставляют способ хранения ключей за пределами CSP. Ключевые BLOB-объекты создаются путем экспорта существующего ключа из CSP путем вызова функции **криптекспорткэй** . Позднее большой двоичный объект ключа можно импортировать в поставщик (часто это другой CSP на другом компьютере), вызвав функцию **криптимпорткэй** . При этом создается ключ в CSP, который является дубликатом экспортированного объекта.

См. также [*простой ключ BLOB*](s-gly.md), [*большой двоичный объект открытого ключа*](p-gly.md)и [*BLOB-объект закрытого ключа*](p-gly.md).

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**формат большого двоичного объекта ключа**
</dt> <dd>

Формат большого двоичного объекта ключа при экспорте открытого или сеансового ключа из CSP. Формат определяется типом поставщика экспортируемого CSP. Большой двоичный объект ключа создается путем вызова **криптекспорткэй**.

См. также [*BLOB-объект открытого ключа*](p-gly.md) и [*простой ключ большого двоичного объекта*](s-gly.md).

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**центр сертификации ключей**
</dt> <dd>

(ККА) Доверенная сущность, которая обычно хранит защищенную базу данных составных сообщений, подписанных с помощью закрытого ключа ККА. В практических реализациях составные сообщения состоят из имени пользователя, открытого ключа пользователя и любых других важных сведений о пользователе. Когда принимающее приложение получает подписанное сообщение от пользователя, приложение может проверить открытый ключ, полученный с помощью сообщения, сравнив его с открытым ключом, хранящимся в базе данных ККА.

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**контейнер ключей**
</dt> <dd>

Часть ключевой базы данных, содержащая все пары ключей (пары ключей Exchange и Signature), принадлежащие конкретному пользователю. Каждый контейнер имеет уникальное имя, которое используется при вызове функции **CryptAcquireContext** для получения маркера в контейнере.

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**база данных ключей**
</dt> <dd>

База данных, содержащая постоянные криптографические ключи для конкретного CSP. База данных содержит один или несколько контейнеров ключей, которые по отдельности хранят все пары криптографических ключей для конкретного пользователя.

См. также *контейнер ключей*.

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**центр распространения ключей**
</dt> <dd>

KDC Сетевая служба, предоставляющая билеты сеансов и временные ключи сеансов, используемые в протоколе проверки подлинности Kerberos V5. KDC запускается как привилегированный процесс на всех контроллерах домена.

См. также *протокол Kerberos*.

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Алгоритм обмена ключами**
</dt> <dd>

Алгоритм, используемый для шифрования и расшифровки ключей обмена (симметричных ключей сеанса). Некоторые распространенные алгоритмы обмена ключами включают Diffie-Hellman и Кеа, алгоритм обмена ключами, заданный \_ типом поставщика Prov Fortezza. Алгоритм Кеа — это улучшенная версия алгоритма Diffie-Hellman. Каждый тип поставщика может указывать только один алгоритм обмена ключами.

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**Алгоритм обмена ключами**
</dt> <dd>

(КЕА) Алгоритм обмена ключами, заданный \_ типом поставщика Prov Fortezza. Этот алгоритм является улучшенной версией алгоритма Diffie-Hellman.

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**сертификат обмена ключами**
</dt> <dd>

Сертификат, используемый для шифрования информации, отправленной другой стороне. Клиент может использовать сертификат обмена ключами центра сертификации (ЦС) для шифрования данных, отправляемых в ЦС.

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**функции обмена ключами**
</dt> <dd>

Набор функций, используемых для обмена или передачи ключей. Функции обмена ключами также можно использовать для реализации полностью прошедших проверку подлинности обмена ключами.

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**пара ключей обмена ключами**
</dt> <dd>

См. [*раздел пара ключей Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**закрытый ключ обмена ключами**
</dt> <dd>

Закрытый ключ пары ключей Exchange.

См. также: [*пара ключей обмена*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**Протокол обмена ключами**
</dt> <dd>

Протокол, с помощью которого две стороны обмениваются данными для установки общего секрета. Общий секрет обычно используется в качестве симметричного ключа шифрования.

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**Открытый ключ обмена ключами**
</dt> <dd>

Открытый ключ пары ключей Exchange.

См. также: [*пара ключей обмена*](e-gly.md).

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**функции создания ключей**
</dt> <dd>

Набор функций, используемых приложениями для создания и настройки криптографических ключей. Эти функции включают в себя полную поддержку изменения режимов цепочки, векторов инициализации и других функций шифрования.

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**Длина ключа**
</dt> <dd>

Значения, заданные некоторыми поставщиками, которые указывают длину пар открытого и закрытого ключей и ключей сеанса, используемых с этим поставщиком.

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**пара ключей**
</dt> <dd>

Закрытый ключ и связанный с ним открытый ключ.

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**поставщик хранилища ключей**
</dt> <dd>

KSP Независимый программный модуль, который реализует функциональные возможности для создания, хранения и получения [*закрытых ключей*](p-gly.md), управления ими.

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**KSP**
</dt> <dd>

См. *раздел поставщик хранилища ключей*.

</dd> </dl>

 

 



