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
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691954"
---
# <a name="dropeffect-constants"></a><span data-ttu-id="830b0-103">Константы ДРОПЕФФЕКТ</span><span class="sxs-lookup"><span data-stu-id="830b0-103">DROPEFFECT Constants</span></span>

<span data-ttu-id="830b0-104">Представляет сведения о влиянии операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="830b0-104">Represents information about the effects of a drag-and-drop operation.</span></span> <span data-ttu-id="830b0-105">Функция [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) и многие методы в [**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) и [**интерфейс IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) используют значения этого перечисления.</span><span class="sxs-lookup"><span data-stu-id="830b0-105">The [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function and many of the methods in the [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) use the values of this enumeration.</span></span>



| <span data-ttu-id="830b0-106">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="830b0-106">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="830b0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="830b0-107">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <span data-ttu-id="830b0-108"><dt>**Дропеффект \_ НЕТ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="830b0-108"><dt>**DROPEFFECT\_NONE**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="830b0-109">Цель перетаскивания не может принять данные.</span><span class="sxs-lookup"><span data-stu-id="830b0-109">Drop target cannot accept the data.</span></span><br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <span data-ttu-id="830b0-110"><dt>**Дропеффект \_ КОПИРОВАНИЕ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="830b0-110"><dt>**DROPEFFECT\_COPY**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="830b0-111">Удаление результатов в копии.</span><span class="sxs-lookup"><span data-stu-id="830b0-111">Drop results in a copy.</span></span> <span data-ttu-id="830b0-112">Исходные данные не затрагиваются источником перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="830b0-112">The original data is untouched by the drag source.</span></span><br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <span data-ttu-id="830b0-113"><dt>**Дропеффект \_ ПЕРЕМЕСТИТЬ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="830b0-113"><dt>**DROPEFFECT\_MOVE**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="830b0-114">Источник перетаскивания должен удалить данные.</span><span class="sxs-lookup"><span data-stu-id="830b0-114">Drag source should remove the data.</span></span> <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <span data-ttu-id="830b0-115"><dt>**Дропеффект \_ Ссылка**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="830b0-115"><dt>**DROPEFFECT\_LINK**</dt> <dt>4</dt></span></span> </dl>                | <span data-ttu-id="830b0-116">Источник перетаскивания должен создать ссылку на исходные данные.</span><span class="sxs-lookup"><span data-stu-id="830b0-116">Drag source should create a link to the original data.</span></span><br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <span data-ttu-id="830b0-117"><dt>**Дропеффект \_ Прокрутить**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="830b0-117"><dt>**DROPEFFECT\_SCROLL**</dt> <dt>0x80000000</dt></span></span> </dl> | <span data-ttu-id="830b0-118">Прокрутка выполняется до начала или в данный момент в целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="830b0-118">Scrolling is about to start or is currently occurring in the target.</span></span> <span data-ttu-id="830b0-119">Это значение используется в дополнение к другим значениям.</span><span class="sxs-lookup"><span data-stu-id="830b0-119">This value is used in addition to the other values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="830b0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="830b0-120">Remarks</span></span>

<span data-ttu-id="830b0-121">Приложение всегда должно маскировать значения из перечисления **дропеффект** , чтобы обеспечить совместимость с будущими реализациями.</span><span class="sxs-lookup"><span data-stu-id="830b0-121">Your application should always mask values from the **DROPEFFECT** enumeration to ensure compatibility with future implementations.</span></span> <span data-ttu-id="830b0-122">В настоящее время только некоторые позиции в значении **дропеффект** имеют значение.</span><span class="sxs-lookup"><span data-stu-id="830b0-122">Presently, only some of the positions in a **DROPEFFECT** value have meaning.</span></span> <span data-ttu-id="830b0-123">В будущем будут добавлены дополнительные интерпретации для битов.</span><span class="sxs-lookup"><span data-stu-id="830b0-123">In the future, more interpretations for the bits will be added.</span></span> <span data-ttu-id="830b0-124">Источники перетаскивания и целевые объекты перетаскивания должны тщательно маскировать эти значения перед сравнением.</span><span class="sxs-lookup"><span data-stu-id="830b0-124">Drag sources and drop targets should carefully mask these values appropriately before comparing.</span></span> <span data-ttu-id="830b0-125">Они никогда не должны сравнивать **дропеффект** с, скажем, с дропеффект \_ Copy, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="830b0-125">They should never compare a **DROPEFFECT** against, say, DROPEFFECT\_COPY by doing the following:</span></span>

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

<span data-ttu-id="830b0-126">Вместо этого приложение должно всегда маскировать в качестве значения или значений, которые используются одним из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="830b0-126">Instead, the application should always mask for the value or values being sought as using one of the following techniques:</span></span>

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

<span data-ttu-id="830b0-127">Это позволяет определить новые эффекты перетаскивания, сохраняя обратную совместимость с существующим кодом.</span><span class="sxs-lookup"><span data-stu-id="830b0-127">This allows for the definition of new drop effects, while preserving backward compatibility with existing code.</span></span>

## <a name="requirements"></a><span data-ttu-id="830b0-128">Требования</span><span class="sxs-lookup"><span data-stu-id="830b0-128">Requirements</span></span>



| <span data-ttu-id="830b0-129">Требование</span><span class="sxs-lookup"><span data-stu-id="830b0-129">Requirement</span></span> | <span data-ttu-id="830b0-130">Значение</span><span class="sxs-lookup"><span data-stu-id="830b0-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="830b0-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="830b0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="830b0-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="830b0-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="830b0-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="830b0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="830b0-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="830b0-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="830b0-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="830b0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="830b0-136"><dt>Олеидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="830b0-136"><dt>OleIdl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="830b0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="830b0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="830b0-138">**DoDragDrop**</span><span class="sxs-lookup"><span data-stu-id="830b0-138">**DoDragDrop**</span></span>](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[<span data-ttu-id="830b0-139">**идропсаурце**</span><span class="sxs-lookup"><span data-stu-id="830b0-139">**IDropSource**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[<span data-ttu-id="830b0-140">**Интерфейс IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="830b0-140">**IDropTarget**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





