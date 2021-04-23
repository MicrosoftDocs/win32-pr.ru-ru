---
title: Сообщение TB_SETIMAGELIST (Коммктрл. h)
description: Задает список изображений, используемый панелью инструментов для отображения кнопок, которые находятся в состоянии по умолчанию.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- Элементы управления Windows для TB_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0b7ad631e8b56824ae65a2b262c5478611e75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654599"
---
# <a name="tb_setimagelist-message"></a><span data-ttu-id="b7d7b-104">\_Сообщение СЕТИМАЖЕЛИСТ ТБ</span><span class="sxs-lookup"><span data-stu-id="b7d7b-104">TB\_SETIMAGELIST message</span></span>

<span data-ttu-id="b7d7b-105">Задает список изображений, используемый панелью инструментов для отображения кнопок, которые находятся в состоянии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-105">Sets the image list that the toolbar uses to display buttons that are in their default state.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7d7b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7d7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d7b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7d7b-107">*wParam*</span></span> 
</dt> <dd>

[<span data-ttu-id="b7d7b-108">Версия 5,80.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-108">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="b7d7b-109">Индекс списка.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-109">The index of the list.</span></span> <span data-ttu-id="b7d7b-110">Если используется только один список изображений или более ранняя версия стандартных элементов управления, установите параметр *wParam* в значение 0.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-110">If you use only one image list, or an earlier version of the common controls, set *wParam* to zero.</span></span> <span data-ttu-id="b7d7b-111">Дополнительные сведения об использовании нескольких списков изображений см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-111">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="b7d7b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7d7b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7d7b-113">Обрабатываемый список изображений.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-113">Handle to the image list to set.</span></span> <span data-ttu-id="b7d7b-114">Если этот параметр имеет **значение NULL**, изображения на кнопках не отображаются.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-114">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d7b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7d7b-115">Return value</span></span>

<span data-ttu-id="b7d7b-116">Возвращает маркер списка изображений, который ранее использовался для отображения кнопок в состоянии по умолчанию, или **значение NULL** , если список изображений ранее не был задан.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-116">Returns the handle to the image list previously used to display buttons in their default state, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d7b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7d7b-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7d7b-118">Приложение несет ответственность за освобождение списка образов после уничтожения панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-118">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="b7d7b-119">Сообщение **\_ Сетимажелист в ТБ** не может быть объединено с [**ТБ \_ аддбитмап**](tb-addbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="b7d7b-119">The **TB\_SETIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="b7d7b-120">Его также нельзя использовать с панелями инструментов, созданными с помощью [**креатетулбарекс**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), которая вызывает **ТБ \_ аддбитмап** внутри.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-120">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="b7d7b-121">Когда вы создаете панель инструментов с **креатетулбарекс** или **используете \_ аддбитмап ТБ** для добавления изображений, панель инструментов управляет списком изображений на внутреннем уровне.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-121">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="b7d7b-122">Попытка изменить ее с помощью **ТБ \_ сетимажелист** имеет непредсказуемые последствия.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-122">Attempting to modify it with **TB\_SETIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="b7d7b-123">В [версии 5,80](common-control-versions.md) или более поздних стандартных элементов управления изображения кнопок не должны поступать из одного и того же списка изображений.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-123">With [version 5.80](common-control-versions.md) or later of the common controls, button images need not come from the same image list.</span></span> <span data-ttu-id="b7d7b-124">Чтобы использовать несколько списков изображений для кнопок панели инструментов, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="b7d7b-124">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="b7d7b-125">Включите несколько списков изображений, отправив элемент управления ToolBar [**\_ Сетверсион сообщение CCM**](ccm-setversion.md) с параметром *wParam* (номер версии), равным 5.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-125">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="b7d7b-126">Для каждого списка изображений, который вы хотите использовать, отправляйте панель инструментов с сообщением **\_ сетимажелист ТБ** .</span><span class="sxs-lookup"><span data-stu-id="b7d7b-126">For each image list you want to use, send the toolbar control a **TB\_SETIMAGELIST** message.</span></span> <span data-ttu-id="b7d7b-127">Присвойте параметру *wParam* определенное приложением значение *wParam* , которое будет использоваться для определения списка.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-127">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="b7d7b-128">Задайте параметр *lParam* для обработчика химажелист списка.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-128">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="b7d7b-129">Для каждой кнопки установите для элемента **ибитмап** структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) этой кнопки значение макелонг (*ииндекс*, *иимажеид*).</span><span class="sxs-lookup"><span data-stu-id="b7d7b-129">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="b7d7b-130">Значение *иимажеид* — это идентификатор соответствующего списка изображений, который был определен на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-130">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="b7d7b-131">Значение *ииндекс* — это индекс конкретного изображения в этом списке.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-131">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="b7d7b-132">Добавьте кнопки, отправив элемент управления ToolBar с сообщением [**\_ Аддбуттонс (ТБ**](tb-addbuttons.md) ).</span><span class="sxs-lookup"><span data-stu-id="b7d7b-132">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="b7d7b-133">В следующем фрагменте кода показано, как добавить на панель инструментов пять кнопок с изображениями из трех различных списков изображений.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-133">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="b7d7b-134">Поддержка нескольких списков изображений включается с помощью сообщения [**CCM \_ сетверсион**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b7d7b-134">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="b7d7b-135">Затем в списках изображений задаются и назначаются идентификаторы 0-2.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-135">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="b7d7b-136">Кнопки назначаются изображениям из списков изображений следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b7d7b-136">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="b7d7b-137">Кнопка 0 находится в списке изображений ноль (Ахим \[ 0 \] ) с индексом 1.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-137">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="b7d7b-138">Кнопка 1 находится в списке изображений One (Ахим \[ 1 \] ) с индексом 1.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-138">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="b7d7b-139">Кнопка 2 из списка изображений Two (Ахим \[ 2 \] ) с индексом 1.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-139">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="b7d7b-140">Кнопка 3 из списка изображений ноль (Ахим \[ 0 \] ) с индексом 2.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-140">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="b7d7b-141">Кнопка 4 находится в списке изображений One (Ахим \[ 1 \] ) с индексом 3.</span><span class="sxs-lookup"><span data-stu-id="b7d7b-141">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="b7d7b-142">Наконец, кнопки добавляются в элемент управления ToolBar с сообщением [**\_ аддбуттонс ТБ**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="b7d7b-142">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a><span data-ttu-id="b7d7b-143">Требования</span><span class="sxs-lookup"><span data-stu-id="b7d7b-143">Requirements</span></span>



| <span data-ttu-id="b7d7b-144">Требование</span><span class="sxs-lookup"><span data-stu-id="b7d7b-144">Requirement</span></span> | <span data-ttu-id="b7d7b-145">Значение</span><span class="sxs-lookup"><span data-stu-id="b7d7b-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d7b-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7d7b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d7b-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7d7b-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7d7b-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7d7b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d7b-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7d7b-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7d7b-150">Header</span><span class="sxs-lookup"><span data-stu-id="b7d7b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7d7b-151"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d7b-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d7b-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7d7b-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7d7b-153">[**макелонг**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7d7b-153">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

