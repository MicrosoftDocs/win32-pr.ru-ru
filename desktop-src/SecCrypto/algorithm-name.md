---
description: Задает или получает алгоритм, используемый для подписывания, запечатывание и шифрования операций. Это свойство по умолчанию.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Algorithm.Name, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4d9860e9a3f04f2f17ebcda08a4ec2610c5af3cbb5fbb5e7afa98227264992b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880154"
---
# <a name="algorithmname-property"></a>Algorithm.Name, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс алгорисмидентифиер**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **Name** задает или получает алгоритм, используемый для подписывания, запечатывание и шифрования операций. Это свойство по умолчанию.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a>Значение свойства

Значение перечисления [**\_ \_ алгоритма CAPICOM**](capicom-encryption-algorithm.md) , указывающее используемый алгоритм. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                       | Значение                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <dt>**\_Алгоритм шифрования \_ CAPICOM \_ RC2**</dt> </dl>    | Используйте шифрование RC2.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <dt>**\_Алгоритм шифрования \_ CAPICOM \_ RC4**</dt> </dl>    | Используйте алгоритм шифрования RC4.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <dt>**\_алгоритм шифрования \_ CAPICOM \_ des**</dt> </dl>    | Используйте шифрование DES.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <dt>**\_Алгоритм шифрования \_ CAPICOM \_ 3DES**</dt> </dl> | Используйте тройное шифрование DES.<br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <dt>**\_алгоритм шифрования \_ CAPICOM \_ AES**</dt> </dl>    | Используйте алгоритм AES.<br/>     |



 

## <a name="remarks"></a>Remarks

Когда значение этого свойства сбрасывается прямо или косвенно, полное состояние объекта сбрасывается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
