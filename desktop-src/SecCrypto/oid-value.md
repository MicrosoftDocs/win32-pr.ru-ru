---
description: Задает или получает значение кода OID с точкой в идентификаторе.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: Кода. Value, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669457"
---
# <a name="oidvalue-property"></a>Кода. Value, свойство

\[Свойство **value** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **value** задает или получает значение кода OID с точками идентификатора.

## <a name="syntax"></a>Синтаксис


```VB
OID.Value As String
```



## <a name="property-value"></a>Значение свойства

Значение кода OID с точками идентификатора. Возможные значения см. в разделе Винкрипт. h.

## <a name="remarks"></a>Комментарии

Если задано свойство **value** , для свойства [**FriendlyName**](oid-friendlyname.md) задается соответствующее отображаемое имя. Если задано свойство **FriendlyName** , свойству **value** присваивается соответствующее значение с точками.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**КОДА**](oid.md)
</dt> </dl>

 

 
