---
title: Ерроритем. Condition
description: Свойство Condition извлекает значение, указывающее условие для ошибки.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- Проигрыватель Windows Media Ерроритем. Condition
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698968"
---
# <a name="erroritemcondition"></a>Ерроритем. Condition

Свойство **Condition** извлекает значение, указывающее условие для ошибки.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное**), представляющим код условия.

## <a name="remarks"></a>Комментарии

Код условия — это значение, которое используется корпорацией Майкрософт для предоставления дополнительных сведений сотрудникам службы технической поддержки.

**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> </dl>

 

 





