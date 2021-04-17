---
description: Содержит определения терминов безопасности, начинающихся с буквы R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc85a0da8aa4a0b985b8be040ef95e37068e8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683807"
---
# <a name="r-security-glossary"></a>R (глоссарий по безопасности)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [р](h-gly.md) [.](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

Имя алгоритма [*CryptoAPI*](c-gly.md) для алгоритма RC2.

См. также *алгоритм блокировки RC2*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**Алгоритм блокировки RC2**
</dt> <dd>

Алгоритм [*шифрования*](e-gly.md) данных на основе симметричного блочного шифра RC2 64. RC2 определяется \_ типами поставщика Prov RSA \_ . [*CryptoAPI*](c-gly.md) ссылается на этот алгоритм по его идентификатору (калг \_ RC2), имени (RC2) и классу \_ ( \_ Шифрование данных класса ALG \_ ).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

Имя алгоритма [*CryptoAPI*](c-gly.md) для алгоритма RC4.

См. также *алгоритм потока RC4*.

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**Алгоритм потока RC4**
</dt> <dd>

Алгоритм [*шифрования*](e-gly.md) данных на основе симметричного потокового шифра RC4. RC4 задается в \_ \_ типах поставщиков Prov RSA Full. [*CryptoAPI*](c-gly.md) ссылается на этот алгоритм по его идентификатору (калг \_ RC4), имени (RC4) и классу \_ ( \_ Шифрование данных класса ALG \_ ).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**RDN**
</dt> <dd>

См. раздел *относительное различающееся имя*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**сканер**
</dt> <dd>

Стандартное устройство в подсистеме [*смарт-карт*](s-gly.md) . Устройство интерфейса (IFD), которое поддерживает двунаправленный ввод-вывод на смарт-карту. Она может быть связана со всей системой, одной или несколькими группами читателей или с конкретным терминалом. Подсистема смарт-карт позволяет выделить устройство чтения для терминала, которому она назначена. Однако в настоящее время на компьютере существует только один терминал.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**драйвер модуля чтения**
</dt> <dd>

Конкретный драйвер, который сопоставляет службы драйверов с конкретным устройством чтения оборудования. Он должен передавать события вставки и удаления карт в драйвер класса [*смарт-карты*](s-gly.md) для перенаправления в Диспетчер ресурсов смарт-карт и предоставлять возможности обмена данными с картой любыми необработанными, t = 0, t = 1 или PTS протоколами.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**Группа читателей**
</dt> <dd>

Логическая группа читателей. Группы читателей могут быть определены системой или созданы пользователями или администраторами. Группы читателей используются функциями смарт-карт, которые могут действовать при работе с группами читателей. Чтобы избежать конфликтов имен с определяемыми пользователем группами, корпорация Майкрософт оставляет за собой использование любого имени, содержащего знак доллара ($).

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**вспомогательный драйвер модуля чтения**
</dt> <dd>

Предоставляет общие подпрограммы поддержки драйверов смарт-карт и дополнительную поддержку T = 0 и T = 1 для конкретных драйверов, если это необходимо.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**число ссылок**
</dt> <dd>

Целочисленное значение, используемое для наблюдения за COM-объектом. При создании объекта его счетчик ссылок устанавливается равным 1. Каждый раз, когда интерфейс привязан к объекту, его счетчик ссылок увеличивается; При удалении подключения к интерфейсу счетчик ссылок уменьшается. Объект уничтожается, когда счетчик ссылок достигает нуля. Все интерфейсы для этого объекта являются недопустимыми.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**относительное различающееся имя**
</dt> <dd>

RDN Сущность, входящая в качестве субъекта в запрос сертификата. Элементы в RDN определяются их атрибутами и не обязательно должны включать имя. В отношении [*CryptoAPI*](c-gly.md)атрибут RDN определяется \_ структурой RDN сертификата, которая, в свою очередь, указывает на массив \_ структур атрибутов RDN в сертификате \_ . Каждая структура атрибута задает один атрибут.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**относительный идентификатор**
</dt> <dd>

ИЗБЕЖАТЬ Часть [*идентификатора безопасности*](s-gly.md) (SID), определяющая пользователя или группу в отношении центра, который выдал идентификатор безопасности.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**хранилище перемещено**
</dt> <dd>

[*Хранилище сертификатов*](c-gly.md) , которое было перемещено из своего расположения реестра по умолчанию в другое расположение в реестре.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**удаленное хранилище**
</dt> <dd>

[*Хранилище сертификатов*](c-gly.md) , расположенное на другом компьютере, например на файловом сервере или другом общем удаленном компьютере.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**ответ КАТЕГОРИЯХ APDU**
</dt> <dd>

[*Блок данных протокола приложения*](a-gly.md) (категориях APDU), отправленный в ответ на полученный категориях APDU.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**разглашение**
</dt> <dd>

Способность пользователя ложно опровергнуть факт выполнения им определенного действия, когда другие стороны не могут доказать, что он его выполнял. Например, пользователь, который удалил файл, и который может успешно отказаться от этого.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**Диспетчер ресурсов**
</dt> <dd>

Модуль подсистемы [*смарт-карт*](s-gly.md) , управляющий доступом к нескольким модулям чтения и смарт-картам. Диспетчер ресурсов идентифицирует и отслеживает ресурсы, выделяет модули чтения и ресурсы в нескольких приложениях и поддерживает примитивы транзакций для доступа к службам, доступным на данной карте.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**API Resource Manager**
</dt> <dd>

Набор функций Windows, обеспечивающих прямой доступ к службам Resource Manager.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**контекст Resource Manager**
</dt> <dd>

Контекст, используемый диспетчером ресурсов при доступе к базе данных смарт-карты. Контекст Resource Manager в основном используется функциями запросов и управления при доступе к базе данных. Областью действия контекста диспетчера ресурсов может быть текущий пользователь или система.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**список отзыва**
</dt> <dd>

См. [*список отзыва сертификатов*](c-gly.md).

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**ИЗБЕЖАТЬ**
</dt> <dd>

См. *относительный идентификатор*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**корневой центр сертификации**
</dt> <dd>

[*Центр сертификации*](c-gly.md) (ЦС) в верхней части иерархии ЦС. Корневой центр сертифицирует центры сертификации, расположенные на следующем уровне иерархии.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**корневой сертификат**
</dt> <dd>

Самозаверяющий сертификат [*центра сертификации*](c-gly.md) (ЦС), определяющий ЦС. Он называется корневым сертификатом, так как он является сертификатом для корневого ЦС. Корневой ЦС должен подписать собственный сертификат ЦС, так как по определению не существует центра сертификации для подписания сертификата ЦС.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**RSA**
</dt> <dd>

RSA Data Security, Inc. — основной разработчик и издатель [*стандартов криптографии с открытым ключом*](p-gly.md) (PKCS). RSA в имени означает имена трех разработчиков и владельцев компании: Ривест, Шамир и Адельман.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**\_KEYX RSA**
</dt> <dd>

Имя алгоритма [*CryptoAPI*](c-gly.md) для алгоритма обмена ключами RSA. CryptoAPI также ссылается на этот алгоритм по идентификатору алгоритма (КАЛГ \_ RSA \_ KEYX) и классу ( \_ \_ Обмен ключами класса ALG \_ ).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**\_знак RSA**
</dt> <dd>

Имя алгоритма CryptoAPI для алгоритма подписи RSA. CryptoAPI также ссылается на этот алгоритм по идентификатору алгоритма (КАЛГ \_ RSA \_ Sign) и классу ( \_ \_ сигнатура класса ALG).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**Алгоритм открытого ключа RSA**
</dt> <dd>

Алгоритм обмена ключами и подписи на основе популярного шифра открытого ключа RSA. Этот алгоритм используется PROV \_ RSA \_ Full, Prov \_ RSA \_ SIG, PROV \_ MS \_ Exchange и Prov \_ SSL Type Providers. CryptoAPI ссылается на этот алгоритм по его идентификаторам (КАЛГ \_ RSA \_ KEYX и \_ калг \_ Sign RSA), именам (RSA \_ KEYX и RSA \_ ) и класс ( \_ \_ Обмен ключами класса ALG \_ ).

</dd> </dl>

 

 



