---
title: Константы ДРОПЕФФЕКТ (Олеидл. h)
description: Представляет сведения о влиянии операции перетаскивания.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c9a4fa961b0da2e654d4672392104b95e718bbb176167c7bb715c39f25cfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736956"
---
# <a name="dropeffect-constants"></a>Константы ДРОПЕФФЕКТ

Представляет сведения о влиянии операции перетаскивания. Функция [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) и многие методы в [**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) и [**интерфейс IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) используют значения этого перечисления.



| Константа/значение                                                                                                                                                                                                                            | Описание                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**Дропеффект \_ НЕТ**</dt> <dt>0</dt> </dl>                | Цель перетаскивания не может принять данные.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**Дропеффект \_ КОПИРОВАНИЕ**</dt> <dt>1</dt> </dl>                | Удаление результатов в копии. Исходные данные не затрагиваются источником перетаскивания.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**Дропеффект \_ ПЕРЕМЕСТИТЬ**</dt> <dt>2</dt> </dl>                | Источник перетаскивания должен удалить данные. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**Дропеффект \_ Ссылка**</dt> <dt>4</dt> </dl>                | Источник перетаскивания должен создать ссылку на исходные данные.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**Дропеффект \_ Прокрутить**</dt> <dt>0x80000000</dt> </dl> | Прокрутка выполняется до начала или в данный момент в целевом объекте. Это значение используется в дополнение к другим значениям.<br/> |



## <a name="remarks"></a>Remarks

Приложение всегда должно маскировать значения из перечисления **дропеффект** , чтобы обеспечить совместимость с будущими реализациями. В настоящее время только некоторые позиции в значении **дропеффект** имеют значение. В будущем будут добавлены дополнительные интерпретации для битов. Источники перетаскивания и целевые объекты перетаскивания должны тщательно маскировать эти значения перед сравнением. Они никогда не должны сравнивать **дропеффект** с, скажем, с дропеффект \_ Copy, выполнив следующие действия:

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

Вместо этого приложение должно всегда маскировать в качестве значения или значений, которые используются одним из следующих методов:

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Это позволяет определить новые эффекты перетаскивания, сохраняя обратную совместимость с существующим кодом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Олеидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**Интерфейс IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





