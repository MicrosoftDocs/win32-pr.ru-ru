---
title: THEME. Опенвиеврелативе
description: Метод Опенвиеврелативе открывает представление в новом окне с указанной начальной позицией относительно левого верхнего угла обложки.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- Проигрыватель Windows Media THEME. Опенвиеврелативе
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675559"
---
# <a name="themeopenviewrelative"></a><span data-ttu-id="5c5fb-104">THEME. Опенвиеврелативе</span><span class="sxs-lookup"><span data-stu-id="5c5fb-104">THEME.openViewRelative</span></span>

<span data-ttu-id="5c5fb-105">Метод **опенвиеврелативе** открывает **представление** в новом окне с указанной начальной позицией относительно левого верхнего угла обложки.</span><span class="sxs-lookup"><span data-stu-id="5c5fb-105">The **openViewRelative** method opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span>

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a><span data-ttu-id="5c5fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c5fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c5fb-107"><span id="view"></span><span id="VIEW"></span>*режиме*</span><span class="sxs-lookup"><span data-stu-id="5c5fb-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="5c5fb-108">**Строка** , указывающая **идентификатор** открываемого **представления** .</span><span class="sxs-lookup"><span data-stu-id="5c5fb-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fb-109"><span id="left"></span><span id="LEFT"></span>*слева*</span><span class="sxs-lookup"><span data-stu-id="5c5fb-109"><span id="left"></span><span id="LEFT"></span>*left*</span></span>
</dt> <dd>

<span data-ttu-id="5c5fb-110">**Число** (**длинное**), определяющее начальное расстояние в пикселях от левой границы **представления** до левого края обложки.</span><span class="sxs-lookup"><span data-stu-id="5c5fb-110">A **Number** (**long**) specifying the initial distance in pixels of the left border of the **VIEW** from the left border of the skin.</span></span> <span data-ttu-id="5c5fb-111">Отрицательное значение указывает на начальную точку слева от границы обложки.</span><span class="sxs-lookup"><span data-stu-id="5c5fb-111">A negative value indicates an initial position to the left of the skin border.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fb-112"><span id="top"></span><span id="TOP"></span>*Вверх*</span><span class="sxs-lookup"><span data-stu-id="5c5fb-112"><span id="top"></span><span id="TOP"></span>*top*</span></span>
</dt> <dd>

<span data-ttu-id="5c5fb-113">**Число** (**длинное**), указывающее начальное расположение верхней границы **представления** относительно верхней границы обложки.</span><span class="sxs-lookup"><span data-stu-id="5c5fb-113">A **Number** (**long**) specifying the initial position of the top border of the **VIEW** relative to the top border of the skin.</span></span> <span data-ttu-id="5c5fb-114">Отрицательные значения указывают начальную точку над границей обложки.</span><span class="sxs-lookup"><span data-stu-id="5c5fb-114">A negative values indicates an initial position above the skin border.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c5fb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c5fb-115">Return Value</span></span>

<span data-ttu-id="5c5fb-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5c5fb-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c5fb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c5fb-117">Remarks</span></span>

<span data-ttu-id="5c5fb-118">Позиция, указанная для **представления** , используется при первом вызове этого метода, после чего пользователь может перетащить **представление** в другое место.</span><span class="sxs-lookup"><span data-stu-id="5c5fb-118">The position specified for the **VIEW** is used the first time this method is called, after which the user can drag the **VIEW** to another location.</span></span> <span data-ttu-id="5c5fb-119">Новая заданная позицией сохраняется, и при последующих вызовах используется самая последняя.</span><span class="sxs-lookup"><span data-stu-id="5c5fb-119">The new position is saved, and on subsequent calls, the most recent position is used.</span></span>

## <a name="examples"></a><span data-ttu-id="5c5fb-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="5c5fb-120">Examples</span></span>


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="5c5fb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5c5fb-121">Requirements</span></span>



| <span data-ttu-id="5c5fb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5c5fb-122">Requirement</span></span> | <span data-ttu-id="5c5fb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5c5fb-123">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="5c5fb-124">Версия</span><span class="sxs-lookup"><span data-stu-id="5c5fb-124">Version</span></span><br/> | <span data-ttu-id="5c5fb-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5c5fb-125">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c5fb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c5fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5fb-127">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="5c5fb-127">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="5c5fb-128">**THEME. closeView**</span><span class="sxs-lookup"><span data-stu-id="5c5fb-128">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="5c5fb-129">**THEME. openView**</span><span class="sxs-lookup"><span data-stu-id="5c5fb-129">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





