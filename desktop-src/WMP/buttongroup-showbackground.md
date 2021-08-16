---
title: BUTTONGROUP. Шовбаккграунд
description: Атрибут Шовбаккграунд указывает или получает значение, указывающее, отображает ли BUTTONGROUP только кнопки, или отображает полный точечный рисунок, указанный в атрибуте Image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP. шовбаккграунд проигрыватель Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb95b707fa7e14b00e86c5a65949ff9fba3ce3db32745116fa65ca4c53ac1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342677"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP. Шовбаккграунд

Атрибут **шовбаккграунд** указывает или получает значение, указывающее, отображает ли **BUTTONGROUP** только кнопки, или отображает полный точечный рисунок, указанный в атрибуте **Image** .

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **логическим значением** для чтения и записи.



| Значение | Описание                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| Да  | Отображаются кнопки, а область, не занятая кнопками, рисуется из растрового изображения. |
| false | По умолчанию. Отображаются только кнопки.                                                   |



 

## <a name="remarks"></a>Remarks

Если **шовбаккграунд** имеет значение true, будет виден весь основной **образ** .

Если **шовбаккграунд** имеет значение false, будут подготавливаться только области, соответствующие назначенным цветам **маппингимаже** . Иными словами, будут видны только **буттонелементс** с назначенными **маппингколор** .

Если указано недопустимое значение, сохраняется предыдущее состояние.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BUTTONGROUP, элемент**](buttongroup-element.md)
</dt> <dt>

[**БУТТОНЕЛЕМЕНТ. Маппингколор**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP. Image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. Маппингимаже**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





