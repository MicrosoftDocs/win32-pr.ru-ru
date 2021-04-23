---
title: Просмотр. размер
description: Метод size изменяет размер представления на указанном крае.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- Просмотр. Размер проигрывателя Windows Media
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704180"
---
# <a name="viewsize"></a><span data-ttu-id="0985c-104">Просмотр. размер</span><span class="sxs-lookup"><span data-stu-id="0985c-104">VIEW.size</span></span>

<span data-ttu-id="0985c-105">Метод **size** изменяет размер **представления** на указанном крае.</span><span class="sxs-lookup"><span data-stu-id="0985c-105">The **size** method resizes the **VIEW** on a specified edge.</span></span>

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a><span data-ttu-id="0985c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0985c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0985c-107"><span id="handle"></span><span id="HANDLE"></span>*справиться*</span><span class="sxs-lookup"><span data-stu-id="0985c-107"><span id="handle"></span><span id="HANDLE"></span>*handle*</span></span>
</dt> <dd>

<span data-ttu-id="0985c-108">Строка, указывающая ребро или угол для перемещения при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="0985c-108">String specifying the edge or corner to move when sizing.</span></span> <span data-ttu-id="0985c-109">Эта строка должна иметь одно из следующих восьми значений.</span><span class="sxs-lookup"><span data-stu-id="0985c-109">This string must have one of the following eight values.</span></span>



| <span data-ttu-id="0985c-110">Edge</span><span class="sxs-lookup"><span data-stu-id="0985c-110">Edge</span></span>   | <span data-ttu-id="0985c-111">Угол</span><span class="sxs-lookup"><span data-stu-id="0985c-111">Corner</span></span>      |
|--------|-------------|
| <span data-ttu-id="0985c-112">top</span><span class="sxs-lookup"><span data-stu-id="0985c-112">top</span></span>    | <span data-ttu-id="0985c-113">верхнем</span><span class="sxs-lookup"><span data-stu-id="0985c-113">topright</span></span>    |
| <span data-ttu-id="0985c-114">right</span><span class="sxs-lookup"><span data-stu-id="0985c-114">right</span></span>  | <span data-ttu-id="0985c-115">боттомригхт</span><span class="sxs-lookup"><span data-stu-id="0985c-115">bottomright</span></span> |
| <span data-ttu-id="0985c-116">снизу</span><span class="sxs-lookup"><span data-stu-id="0985c-116">bottom</span></span> | <span data-ttu-id="0985c-117">боттомлефт</span><span class="sxs-lookup"><span data-stu-id="0985c-117">bottomleft</span></span>  |
| <span data-ttu-id="0985c-118">Левое</span><span class="sxs-lookup"><span data-stu-id="0985c-118">left</span></span>   | <span data-ttu-id="0985c-119">топлефт</span><span class="sxs-lookup"><span data-stu-id="0985c-119">topleft</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0985c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0985c-120">Return Value</span></span>

<span data-ttu-id="0985c-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0985c-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0985c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0985c-122">Remarks</span></span>

<span data-ttu-id="0985c-123">Этот метод обычно вызывается из обработчика **OnMouseDown** .</span><span class="sxs-lookup"><span data-stu-id="0985c-123">This method is typically called from within an **onmousedown** handler.</span></span> <span data-ttu-id="0985c-124">Он занимается изменением размера при перетаскивании мыши и прекращает изменение размера при отпускании кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="0985c-124">It takes care of resizing while the mouse is dragged and stops resizing when the mouse button is released.</span></span> <span data-ttu-id="0985c-125">Если размер **представления** ограничен, нельзя перетаскивать указатель мыши, чтобы изменить размер **представления** за пределами ограниченных границ.</span><span class="sxs-lookup"><span data-stu-id="0985c-125">If the size of the **VIEW** is restricted, you cannot drag the mouse to resize the **View** beyond the restricted bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="0985c-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="0985c-126">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="0985c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0985c-127">Requirements</span></span>



| <span data-ttu-id="0985c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0985c-128">Requirement</span></span> | <span data-ttu-id="0985c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0985c-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0985c-130">Версия</span><span class="sxs-lookup"><span data-stu-id="0985c-130">Version</span></span><br/> | <span data-ttu-id="0985c-131">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="0985c-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0985c-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0985c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0985c-133">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="0985c-133">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





