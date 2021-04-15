---
description: Свойство Феатурекуррентстате объекта Session является свойством только для чтения, которое возвращает текущее установленное состояние указанного компонента. Значения состояния см. в описании свойства Феатуререкуестстате.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Свойство Session. Феатурекуррентстате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675721"
---
# <a name="sessionfeaturecurrentstate-property"></a>Свойство Session. Феатурекуррентстате

Свойство **феатурекуррентстате** объекта [**Session**](session-object.md) является свойством только для чтения, которое возвращает текущее установленное состояние указанного компонента. Значения состояния см. в описании свойства [**феатуререкуестстате**](session-featurerequeststate.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Значение свойства

Обязательное строковое имя запрошенной функции и первичный ключ в [таблице Feature](feature-table.md).

## <a name="remarks"></a>Комментарии

Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Session**](session-object.md)
</dt> <dt>

[**Феатуререкуестстате, свойство**](session-featurerequeststate.md)
</dt> </dl>

 

 




