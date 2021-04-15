---
description: Возвращает логическое значение, указывающее, находится ли закрытый ключ в съемном хранилище.
ms.assetid: 9371d7cf-65b2-4c0f-a387-195a058d6a8b
title: PrivateKey. in, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsRemovable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6684d40302746a736701b824685a54faeff5354a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689100"
---
# <a name="privatekeyisremovable-method"></a>PrivateKey. in, метод

\[Метод « **несъемный** » доступен для использования в операционных системах, указанных в разделе «требования». Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод « **несъемный** » возвращает логическое значение, указывающее, находится ли закрытый ключ в съемном носителе.

## <a name="syntax"></a>Синтаксис


```VB
PrivateKey.IsRemovable()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если значение — true, закрытый ключ находится в съемном хранилище.

## <a name="remarks"></a>Комментарии

Возвращаемое значение этого метода зависит от используемого [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP). Этот метод возвращает надежное значение, если используется Microsoft CSP. Если CSP не является CSP Майкрософт, возвращаемое значение не может быть точным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
