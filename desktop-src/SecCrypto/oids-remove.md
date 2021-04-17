---
description: Удаляет указанный объект OID из коллекции.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: Метод OID. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685179"
---
# <a name="oidsremove-method"></a>Метод OID. Remove

\[Метод **Remove** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс оидколлектион**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Метод **Remove** удаляет указанный объект [**OID**](oid.md) из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Индекс объекта [**OID**](oid.md) , который необходимо удалить. Это может быть либо индекс в коллекции, либо точечное значение OID.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
