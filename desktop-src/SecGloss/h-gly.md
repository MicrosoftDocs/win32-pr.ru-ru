---
description: Содержит определения терминов безопасности, начинающихся с буквы H.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4165b820-30fc-477e-a690-81109f161323
title: H (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665cd90cfc8a849030b6a1cfd1cb4e6d6f687557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683811"
---
# <a name="h-security-glossary"></a>H (глоссарий по безопасности)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) р [.](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**справиться**
</dt> <dd>

Маркер, используемый для обнаружения или доступа к объекту, например к поставщику служб шифрования, хранилищу сертификатов, сообщениям или паре ключей.

</dd> <dt>

<span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**функции**
</dt> <dd>

Результат фиксированного размера, полученный путем применения математической функции ( *алгоритма хэширования*) к произвольному объему данных. (Также называется "дайджестом сообщений".)

См. также *функции хэширования*.

</dd> <dt>

<span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**хэш-объект**
</dt> <dd>

Объект, используемый для хэширования сообщений или ключей сеанса. Хэш-объект создается путем вызова **CryptCreateHash**. Определение объекта определяется CSP, указанным в вызове.

</dd> <dt>

<span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**алгоритм хэширования**
</dt> <dd>

Алгоритм, используемый для получения хэш-значения некоторого блока данных, например сообщения или сеансового ключа. К типичным хэш-алгоритмам относятся MD2, MD4, MD5 и SHA-1.

</dd> <dt>

<span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**функции хэширования**
</dt> <dd>

Набор функций, используемых для создания и уничтожения хэш-объектов, получения или задания параметров хэш-объекта, а также хэш-данных и ключей сеанса.

</dd> <dt>

<span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**код проверки подлинности сообщения на основе хэша**
</dt> <dd>

HMAC Алгоритм хэширования с симметричным ключом, реализованный поставщиками служб шифрования (Майкрософт). HMAC используется для проверки целостности данных, чтобы гарантировать, что они не изменялись во время хранения или передачи. Его можно использовать с любым циклическим хэш-алгоритмом шифрования, например MD5 или SHA-1. CryptoAPI ссылается на этот алгоритм по идентификатору алгоритма (КАЛГ \_ HMAC) и классу ( \_ хэш класса алгоритма \_ ).

См. также [*код проверки подлинности сообщения*](m-gly.md).

</dd> <dt>

<span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**хксбк**
</dt> <dd>

Тип данных, который служит в качестве маркера для контекста резервного копирования служб сертификатов. Его роль заключается в поддержке состояния контекста между сервером и API-интерфейсами резервного копирования при выполнении резервного копирования.

</dd> <dt>

<span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**HMAC**
</dt> <dd>

См. раздел *код проверки подлинности сообщения на основе хэша*.

</dd> </dl>

 

 



