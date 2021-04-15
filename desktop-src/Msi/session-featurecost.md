---
description: Свойство Феатурекост объекта Session возвращает общий объем дискового пространства (в единицах 512 байт), требуемый для указанного компонента и его родительских компонентов (вплоть до корня таблицы функций).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Свойство Session. Феатурекост
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651975"
---
# <a name="sessionfeaturecost-property"></a>Свойство Session. Феатурекост

Свойство **феатурекост** объекта [**Session**](session-object.md) возвращает общий объем дискового пространства (в единицах 512 байт), требуемый для указанного компонента и его родительских компонентов (вплоть до корня таблицы функций). Для каждого компонента Общая стоимость состоит из затрат на диск, присоединенных к каждому компоненту, связанному с данной функцией.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




