---
title: Ерроритем. Condition
description: Свойство Condition извлекает значение, указывающее условие для ошибки.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ерроритем. condition проигрыватель Windows Media
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
ms.openlocfilehash: a5f4bfe2c4b2b517b0fd300a0c6465ae9f10147518937822212b621d808f0ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996644"
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

## <a name="remarks"></a>Remarks

Код условия — это значение, которое используется корпорацией Майкрософт для предоставления дополнительных сведений сотрудникам службы технической поддержки.

**проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> </dl>

 

 





