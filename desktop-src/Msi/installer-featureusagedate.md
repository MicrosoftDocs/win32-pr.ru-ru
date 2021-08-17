---
description: Свойство Феатуреусажедате является свойством только для чтения, которое возвращает дату последнего использования указанного компонента.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Свойство Installer. Феатуреусажедате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 15c628b95f6dab2d671e660c9783e071e1e4385c165363fdf9ad39abd571510e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631071"
---
# <a name="installerfeatureusagedate-property"></a>Свойство Installer. Феатуреусажедате

Свойство **феатуреусажедате** является свойством только для чтения, которое возвращает дату последнего использования указанного компонента.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Это свойство задается с помощью методов [**усефеатуре**](installer-usefeature.md), [**провидекомпонент**](installer-providecomponent.md) или [**ПРОВИДЕКУАЛИФИЕДКОМПОНЕНТ**](installer-providequalifiedcomponent.md) или их эквивалентов API для указанного компонента.

Дата указывается в формате даты MS-DOS, как показано в следующей таблице.



| Bits | Содержимое                                            |
|------|-----------------------------------------------------|
| 0–4  | День месяца (1-31)                             |
| 5-8  | Месяц (1 = Январь, 2 = Февраль и т. д.)        |
| 9-15 | Смещение года от 1980 (Добавление 1980 для получения фактического года) |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсижетфеатуреусаже**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




