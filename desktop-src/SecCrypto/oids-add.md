---
description: Добавляет указанный объект OID в коллекцию.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Метод OID. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff686ae816fa61d68e0a0c40326581025ced8f4c94fb5cffc633ff452ac4f0ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979655"
---
# <a name="oidsadd-method"></a>Метод OID. Add

\[Метод **Add** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс оидколлектион**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Метод **Add** добавляет указанный объект [**OID**](oid.md) в коллекцию.

## <a name="syntax"></a>Синтаксис


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Идентификатор объекта* \[ окне\]
</dt> <dd>

Объект [**OID**](oid.md) , добавляемый в коллекцию. Объект **OID** добавляется в отсортированном порядке на основе его точечного значения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
