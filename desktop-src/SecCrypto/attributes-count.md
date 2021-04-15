---
description: Возвращает количество объектов атрибутов в коллекции.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Свойство Attributes. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668698"
---
# <a name="attributescount-property"></a>Свойство Attributes. Count

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]

Свойство **Count** извлекает количество объектов [**атрибутов**](attribute.md) в коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Значение свойства

Число объектов [**атрибутов**](attribute.md) в коллекции. Каждый объект **атрибута** представляет один атрибут в коллекции.

## <a name="remarks"></a>Комментарии

Свойство **Count** можно использовать для указания последнего объекта [**атрибута**](attribute.md) в коллекции при извлечении определенного объекта **атрибута** с помощью свойства [**Attributes. Item**](attributes-item.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Атрибуты**](attributes.md)
</dt> </dl>

 

 
