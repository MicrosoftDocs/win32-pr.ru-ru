---
description: Задает или получает длину ключа.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Свойство Algorithm. KeyLength
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685103"
---
# <a name="algorithmkeylength-property"></a>Свойство Algorithm. KeyLength

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс алгорисмидентифиер**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **keylength** задает или получает длину ключа.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>Значение свойства

Значение перечисления [**\_ \_ \_ длины ключа шифрования CAPICOM**](capicom-encryption-key-length.md) , указывающее длину ключа. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                        | Значение                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**\_ \_ \_ Максимальная длина ключа шифрования \_ CAPICOM**</dt> </dl>     | Используйте максимальную длину ключа, доступную в указанном алгоритме шифрования.<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 40 \_ бит**</dt> </dl>    | Используйте 40-разрядные ключи.<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 56 \_ бит**</dt> </dl>    | Используйте 56-разрядные ключи, если они доступны.<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 128 \_ бит**</dt> </dl> | Используйте 128-разрядные ключи, если они доступны.<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 192 \_ бит**</dt> </dl> | Используйте 192-разрядные ключи. Эта длина ключа доступна только для алгоритма AES.<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**\_ \_ Длина ключа шифрования \_ CAPICOM \_ 256 \_ бит**</dt> </dl> | Используйте 256-разрядные ключи. Эта длина ключа доступна только для алгоритма AES.<br/>                  |



 

## <a name="remarks"></a>Комментарии

При использовании алгоритмов шифрования DES и 3DES Длина ключей составляет Standard, а свойство **keylength** игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Алгоритм**](algorithm.md)
</dt> </dl>

 

 
