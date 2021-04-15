---
description: Задает или получает закрытый ключ, связанный с сертификатом.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Свойство Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669517"
---
# <a name="certificateprivatekey-property"></a>Свойство Certificate. PrivateKey

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **PrivateKey** задает или получает закрытый ключ, связанный с сертификатом. Это свойство было представлено в CAPICOM 2,0.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>Значение свойства

Объект [**PrivateKey**](privatekey.md) , представляющий закрытый ключ, связанный с сертификатом.

## <a name="remarks"></a>Комментарии

Если задать для свойства **PrivateKey** значение Nothing, связь между закрытым ключом и сертификатом будет удалена, но закрытый ключ не будет удален. Чтобы удалить закрытый ключ, вызовите метод [**PrivateKey. Delete**](privatekey-delete.md) , а затем установите для этого свойства значение Nothing.

Это свойство вызывает CAPICOM \_ E \_ не \_ разрешено, если оно задано из веб-приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Certificate**](certificate.md)
</dt> </dl>

 

 
