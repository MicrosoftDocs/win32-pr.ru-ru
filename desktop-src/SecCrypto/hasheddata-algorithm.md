---
description: Задает или получает тип используемого алгоритма хэширования.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: Хашеддата. algorithm, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685224"
---
# <a name="hasheddataalgorithm-property"></a>Хашеддата. algorithm, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс HashAlgorithm**](/previous-versions/windows/) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **Algorithm** задает или получает тип используемого алгоритма хэширования.

## <a name="syntax"></a>Синтаксис


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a>Значение свойства

Значение перечисления хэш [**\_ - \_ алгоритма CAPICOM**](capicom-hash-algorithm.md) , определяющее хэш-алгоритм. Значение по умолчанию — \_ алгоритм ХЭША CAPICOM \_ \_ SHA1. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                               | Значение                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <dt>**\_Алгоритм ХЭША \_ CAPICOM \_ SHA1**</dt> </dl>           | Алгоритм хэширования SHA1.<br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <dt>**\_ \_ MD2 алгоритма CAPICOM hash \_**</dt> </dl>              | Алгоритм хэширования MD2.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <dt>**\_Хэш- \_ алгоритмы CAPICOM \_ MD4**</dt> </dl>              | Алгоритм хэширования MD4.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <dt>**\_MD5- \_ алгоритм хеширования \_**</dt> </dl>              | Алгоритм хэширования MD5.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <dt>**\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 256"**</dt> </dl> | Алгоритм хеширования SHA-256.<br/> **CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <dt>**\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 384"**</dt> </dl> | Алгоритм хеширования SHA-384.<br/> **CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <dt>**\_Хэш-алгоритм "CAPICOM hash \_ \_ SHA \_ 512"**</dt> </dl> | Алгоритм хеширования SHA-512.<br/> **CAPICOM 2.0.0.3 и более ранние версии:** Это значение не поддерживается.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**хашеддата**](hasheddata.md)
</dt> </dl>

 

 
