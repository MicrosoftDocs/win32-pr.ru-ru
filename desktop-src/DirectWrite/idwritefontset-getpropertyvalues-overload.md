---
title: Методы Идвритефонтсет GetPropertyValues (Дврите \_ 3. h)
description: Возвращает значения свойств для набора шрифтов.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Методы GetPropertyValues Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cffc669d71bf7f78087fe3c105c182ca86b4ebf5a689bcdb6c2807dfae3c0f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816365"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>Методы Идвритефонтсет:: GetPropertyValues

Возвращает значения свойств для набора шрифтов.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                   | Описание                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues ( \_ \_ идентификатор свойства шрифта Дврите \_ , идвритестринглист \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Возвращает все уникальные значения свойств в наборе, которые можно использовать для таких целей, как отображение списка семейств или пометки в облаке. Все значения возвращаются независимо от языка, включая все локализованные имена. <br/>                                                                                       |
| [**GetPropertyValues ( \_ \_ идентификатор свойства шрифта дврите \_ , const WCHAR \* , идвритестринглист \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Возвращает все уникальные значения свойств в наборе, которые можно использовать для таких целей, как отображение списка семейств или пометки в облаке. Значения возвращаются в порядке приоритета в соответствии со списком языков, так что если шрифт содержит более одного локализованного имени, будет возвращено предпочтительное из них. <br/> |
| [**GetPropertyValues (UINT32, \_ \_ идентификатор свойства шрифта ДВРИТЕ \_ , bool \* , идврителокализедстрингс \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Возвращает значения свойств определенного индекса элемента шрифта.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Дврите \_ 3. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**идвритефонтсет**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
