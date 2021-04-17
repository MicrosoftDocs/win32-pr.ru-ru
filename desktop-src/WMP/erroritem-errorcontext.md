---
title: Ерроритем. Еррорконтекст
description: Свойство Еррорконтекст извлекает значение, указывающее контекст ошибки.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- Проигрыватель Windows Media Ерроритем. Еррорконтекст
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694535"
---
# <a name="erroritemerrorcontext"></a>Ерроритем. Еррорконтекст

Свойство **еррорконтекст** извлекает значение, указывающее контекст ошибки.

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** только для чтения, которая представляет код контекста ошибки.

## <a name="remarks"></a>Комментарии

Контекст ошибки — это информация, используемая корпорацией Майкрософт для предоставления дополнительных сведений сотрудникам службы технической поддержки.

**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает пустую строку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> </dl>

 

 





