---
title: Сообщение TB_SETPRESSEDIMAGELIST (Коммктрл. h)
description: Задает список изображений, используемый панелью инструментов для отображения кнопок, которые находятся в состоянии нажатия.
ms.assetid: d0e061ec-3a89-4c2d-b7f7-5f2061098428
keywords:
- Элементы управления Windows для TB_SETPRESSEDIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_SETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a3c6dafed6dbfdf2a654f4f95f1cef636ba762
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535627"
---
# <a name="tb_setpressedimagelist-message"></a><span data-ttu-id="36dd5-104">\_Сообщение СЕТПРЕССЕДИМАЖЕЛИСТ ТБ</span><span class="sxs-lookup"><span data-stu-id="36dd5-104">TB\_SETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="36dd5-105">Задает список изображений, используемый панелью инструментов для отображения кнопок, которые находятся в состоянии нажатия.</span><span class="sxs-lookup"><span data-stu-id="36dd5-105">Sets the image list that the toolbar uses to display buttons that are in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="36dd5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36dd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36dd5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36dd5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36dd5-108">Индекс списка изображений.</span><span class="sxs-lookup"><span data-stu-id="36dd5-108">The index of the image list.</span></span> <span data-ttu-id="36dd5-109">Если используется только один список изображений, присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="36dd5-109">If you use only one image list, set this parameter to zero.</span></span> <span data-ttu-id="36dd5-110">Дополнительные сведения об использовании нескольких списков изображений см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="36dd5-110">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="36dd5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36dd5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36dd5-112">Обрабатываемый список изображений.</span><span class="sxs-lookup"><span data-stu-id="36dd5-112">Handle to the image list to set.</span></span> <span data-ttu-id="36dd5-113">Если этот параметр имеет **значение NULL**, изображения на кнопках не отображаются.</span><span class="sxs-lookup"><span data-stu-id="36dd5-113">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36dd5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36dd5-114">Return value</span></span>

<span data-ttu-id="36dd5-115">Возвращает маркер списка изображений, который ранее использовался для отображения кнопок в состоянии их нажатия, или **значение NULL** , если такой список изображений не был задан ранее.</span><span class="sxs-lookup"><span data-stu-id="36dd5-115">Returns the handle to the image list previously used to display buttons in their pressed state, or **NULL** if no such image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="36dd5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36dd5-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="36dd5-117">Приложение несет ответственность за освобождение списка образов после уничтожения панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="36dd5-117">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="36dd5-118">Сообщение **\_ Сетпресседимажелист в ТБ** не может быть объединено с [**ТБ \_ аддбитмап**](tb-addbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="36dd5-118">The **TB\_SETPRESSEDIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="36dd5-119">Его также нельзя использовать с панелями инструментов, созданными с помощью [**креатетулбарекс**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), которая вызывает **ТБ \_ аддбитмап** внутри.</span><span class="sxs-lookup"><span data-stu-id="36dd5-119">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="36dd5-120">Когда вы создаете панель инструментов с **креатетулбарекс** или **используете \_ аддбитмап ТБ** для добавления изображений, панель инструментов управляет списком изображений на внутреннем уровне.</span><span class="sxs-lookup"><span data-stu-id="36dd5-120">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="36dd5-121">Попытка изменить ее с помощью **ТБ \_ сетпресседимажелист** имеет непредсказуемые последствия.</span><span class="sxs-lookup"><span data-stu-id="36dd5-121">Attempting to modify it with **TB\_SETPRESSEDIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="36dd5-122">Изображения кнопок не должны поступать из одного и того же списка изображений.</span><span class="sxs-lookup"><span data-stu-id="36dd5-122">Button images need not come from the same image list.</span></span> <span data-ttu-id="36dd5-123">Чтобы использовать несколько списков изображений для кнопок панели инструментов, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="36dd5-123">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="36dd5-124">Включите несколько списков изображений, отправив элемент управления ToolBar [**\_ Сетверсион сообщение CCM**](ccm-setversion.md) с параметром *wParam* (номер версии), равным 5.</span><span class="sxs-lookup"><span data-stu-id="36dd5-124">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="36dd5-125">Для каждого списка изображений, который вы хотите использовать, отправляйте панель инструментов с сообщением **\_ сетпресседимажелист ТБ** .</span><span class="sxs-lookup"><span data-stu-id="36dd5-125">For each image list you want to use, send the toolbar control a **TB\_SETPRESSEDIMAGELIST** message.</span></span> <span data-ttu-id="36dd5-126">Присвойте параметру *wParam* определенное приложением значение *wParam* , которое будет использоваться для определения списка.</span><span class="sxs-lookup"><span data-stu-id="36dd5-126">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="36dd5-127">Задайте параметр *lParam* для обработчика химажелист списка.</span><span class="sxs-lookup"><span data-stu-id="36dd5-127">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="36dd5-128">Для каждой кнопки установите для элемента **ибитмап** структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) этой кнопки значение макелонг (*ииндекс*, *иимажеид*).</span><span class="sxs-lookup"><span data-stu-id="36dd5-128">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="36dd5-129">Значение *иимажеид* — это идентификатор соответствующего списка изображений, который был определен на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="36dd5-129">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="36dd5-130">Значение *ииндекс* — это индекс конкретного изображения в этом списке.</span><span class="sxs-lookup"><span data-stu-id="36dd5-130">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="36dd5-131">Добавьте кнопки, отправив элемент управления ToolBar с сообщением [**\_ Аддбуттонс (ТБ**](tb-addbuttons.md) ).</span><span class="sxs-lookup"><span data-stu-id="36dd5-131">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="36dd5-132">В следующем фрагменте кода показано, как добавить на панель инструментов пять кнопок с изображениями из трех различных списков изображений.</span><span class="sxs-lookup"><span data-stu-id="36dd5-132">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="36dd5-133">Поддержка нескольких списков изображений включается с помощью сообщения [**CCM \_ сетверсион**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="36dd5-133">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="36dd5-134">Затем в списках изображений задаются и назначаются идентификаторы 0-2.</span><span class="sxs-lookup"><span data-stu-id="36dd5-134">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="36dd5-135">Кнопки назначаются изображениям из списков изображений следующим образом:</span><span class="sxs-lookup"><span data-stu-id="36dd5-135">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="36dd5-136">Кнопка 0 находится в списке изображений ноль (Ахим \[ 0 \] ) с индексом 1.</span><span class="sxs-lookup"><span data-stu-id="36dd5-136">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="36dd5-137">Кнопка 1 находится в списке изображений One (Ахим \[ 1 \] ) с индексом 1.</span><span class="sxs-lookup"><span data-stu-id="36dd5-137">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="36dd5-138">Кнопка 2 из списка изображений Two (Ахим \[ 2 \] ) с индексом 1.</span><span class="sxs-lookup"><span data-stu-id="36dd5-138">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="36dd5-139">Кнопка 3 из списка изображений ноль (Ахим \[ 0 \] ) с индексом 2.</span><span class="sxs-lookup"><span data-stu-id="36dd5-139">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="36dd5-140">Кнопка 4 находится в списке изображений One (Ахим \[ 1 \] ) с индексом 3.</span><span class="sxs-lookup"><span data-stu-id="36dd5-140">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="36dd5-141">Наконец, кнопки добавляются в элемент управления ToolBar с сообщением [**\_ аддбуттонс ТБ**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="36dd5-141">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
// Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 2, (LPARAM)ahiml[2]);

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



## <a name="requirements"></a><span data-ttu-id="36dd5-142">Требования</span><span class="sxs-lookup"><span data-stu-id="36dd5-142">Requirements</span></span>



| <span data-ttu-id="36dd5-143">Требование</span><span class="sxs-lookup"><span data-stu-id="36dd5-143">Requirement</span></span> | <span data-ttu-id="36dd5-144">Значение</span><span class="sxs-lookup"><span data-stu-id="36dd5-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36dd5-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36dd5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="36dd5-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36dd5-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36dd5-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36dd5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="36dd5-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36dd5-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36dd5-149">Header</span><span class="sxs-lookup"><span data-stu-id="36dd5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="36dd5-150"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="36dd5-150"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36dd5-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36dd5-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="36dd5-152">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="36dd5-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36dd5-153">**\_ЖЕТПРЕССЕДИМАЖЕЛИСТ ТБ**</span><span class="sxs-lookup"><span data-stu-id="36dd5-153">**TB\_GETPRESSEDIMAGELIST**</span></span>](tb-getpressedimagelist.md)
</dt> <dt>

<span data-ttu-id="36dd5-154">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="36dd5-154">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="36dd5-155">[**макелонг**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36dd5-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

