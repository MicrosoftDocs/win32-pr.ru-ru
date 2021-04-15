---
description: Задает или получает отображаемое имя для идентификатора.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: Кода. FriendlyName, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669166"
---
# <a name="oidfriendlyname-property"></a>Кода. FriendlyName, свойство

\[Свойство **FriendlyName** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **FriendlyName** задает или получает отображаемое имя для идентификатора.

## <a name="syntax"></a>Синтаксис


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a>Значение свойства

Отображаемое имя [**OID**](oid.md).

## <a name="remarks"></a>Комментарии

Если задано свойство **FriendlyName** , свойству [**value**](oid-value.md) присваивается соответствующее значение с точками. Если задано свойство **value** , для свойства **FriendlyName** задается соответствующее отображаемое имя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**КОДА**](oid.md)
</dt> </dl>

 

 
