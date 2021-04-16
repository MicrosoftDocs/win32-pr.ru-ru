---
description: Закрывает открытое хранилище сертификатов.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Метод Store. Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669139"
---
# <a name="storeclose-method"></a>Метод Store. Close

\[Метод **Close** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Close** закрывает открытое [*хранилище сертификатов*](../secgloss/c-gly.md).

## <a name="syntax"></a>Синтаксис


```VB
Store.Close()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

После вызова метода **Close** объект [**Store**](store.md) уничтожается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,1 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Магазин**](store.md)
</dt> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> <dt>

[**Открыт**](store-open.md)
</dt> </dl>

 

 
