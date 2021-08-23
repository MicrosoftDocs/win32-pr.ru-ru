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
ms.openlocfilehash: 617d1695b8b472952f22737ba3f677d9320f9b4214afc3dea5a9cc5010e2b1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629294"
---
# <a name="sessionfeaturecost-property"></a>Свойство Session. Феатурекост

Свойство **феатурекост** объекта [**Session**](session-object.md) возвращает общий объем дискового пространства (в единицах 512 байт), требуемый для указанного компонента и его родительских компонентов (вплоть до корня таблицы функций). Для каждого компонента Общая стоимость состоит из затрат на диск, присоединенных к каждому компоненту, связанному с данной функцией.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




