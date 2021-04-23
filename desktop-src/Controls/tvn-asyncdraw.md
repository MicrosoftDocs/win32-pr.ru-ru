---
title: Код уведомления TVN_ASYNCDRAW (Коммктрл. h)
description: Посылается элементом управления иерархического представления родительскому элементу, когда произошел сбой при рисовании значка или оверлея. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654679"
---
# <a name="tvn_asyncdraw-notification-code"></a><span data-ttu-id="0160d-105">\_Код уведомления ТВН асинкдрав</span><span class="sxs-lookup"><span data-stu-id="0160d-105">TVN\_ASYNCDRAW notification code</span></span>

<span data-ttu-id="0160d-106">Посылается элементом управления иерархического представления родительскому элементу, когда произошел сбой при рисовании значка или оверлея.</span><span class="sxs-lookup"><span data-stu-id="0160d-106">Sent by a tree-view control to its parent when the drawing of a icon or overlay has failed.</span></span> <span data-ttu-id="0160d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0160d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0160d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0160d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0160d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0160d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0160d-110">Указатель на структуру [**нмтвасинкдрав**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="0160d-110">Pointer to an [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="0160d-111">Структура **нмтвасинкдрав** содержит причину сбоя рисования.</span><span class="sxs-lookup"><span data-stu-id="0160d-111">The **NMTVASYNCDRAW** structure contains the reason the draw failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0160d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0160d-112">Return value</span></span>

<span data-ttu-id="0160d-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0160d-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0160d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0160d-114">Remarks</span></span>

<span data-ttu-id="0160d-115">Элемент управления "представление дерева" должен иметь расширенный стиль " [**телевизоры \_ \_ дравимажеасинк**](tree-view-control-window-extended-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="0160d-115">The tree-view control must have the [**TVS\_EX\_DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="0160d-116">Обратите внимание, что это эквивалентно флагу ЛВН асинкдравн в виде списка \_ и соответствующему стилю.</span><span class="sxs-lookup"><span data-stu-id="0160d-116">Note that this is equivalent to list-view's LVN\_ASYNCDRAWN flag and its corresponding style.</span></span>

<span data-ttu-id="0160d-117">Этот элемент управления не рисуется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="0160d-117">This control does not draw asynchronously.</span></span> <span data-ttu-id="0160d-118">Асинхронный используется в контексте, который элемент управления "представление дерева" не выполняет синхронный Извлечение изображения, если оно недоступно.</span><span class="sxs-lookup"><span data-stu-id="0160d-118">Asynchronous is used in the context that the tree-view control does not synchronously extract an image if it is not available.</span></span> <span data-ttu-id="0160d-119">(Например, изображение может быть недоступно, если элемент управления "представление дерева" использует список разреженных изображений, так как изображение может быть выгружено.) Вместо этого, если изображение недоступно, элемент управления синхронно запрашивает у родительского элемента, какое действие следует предпринять, отправив родительское \_ уведомление ТВН асинкдрав с структурой [**нмтвасинкдрав**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="0160d-119">(For instance, the image may not be available if the tree-view control uses a sparse image list, since the image may be unloaded.) Instead, when an image is not available, the control synchronously asks the parent what action to take by sending the parent an TVN\_ASYNCDRAW notification with a [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="0160d-120">Элемент **HR** этой структуры описывает причину сбоя рисования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0160d-120">The **hr** member of this structure describes the reason the control's draw failed.</span></span> <span data-ttu-id="0160d-121">Результат «ч», полученный в результате **HR** \_ , означает, что изображение отсутствует (изображение необходимо извлечь).</span><span class="sxs-lookup"><span data-stu-id="0160d-121">An **hr** result of E\_PENDING means the image is not present at all (the image needs to be extracted).</span></span> <span data-ttu-id="0160d-122">Успешно указывает, что изображение имеется, но не соответствует требуемому качеству изображения.</span><span class="sxs-lookup"><span data-stu-id="0160d-122">Success indicates that the image is present but not at the required image quality.</span></span>

<span data-ttu-id="0160d-123">Родитель задает элемент **двретфлагс** структуры для информирования элемента управления о том, как продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="0160d-123">The parent sets the **dwRetFlags** member of the structure to inform the control how to proceed.</span></span> <span data-ttu-id="0160d-124">Например, родитель может вернуть другое изображение в элементе **иретимажеиндекс** для рисования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0160d-124">For instance, the parent may return another image, in the **iRetImageIndex** member, for the control to draw.</span></span> <span data-ttu-id="0160d-125">В этом случае родительский элемент устанавливает для элемента **двретфлагс** значение \_ DRAWIMAGE адрф.</span><span class="sxs-lookup"><span data-stu-id="0160d-125">In this case, the parent sets the **dwRetFlags** member to ADRF\_DRAWIMAGE.</span></span> <span data-ttu-id="0160d-126">Если элемент управления обнаруживает возвращенное изображение, он не был извлечен, но \_ элемент управления может отправить другое уведомление ТВН асинкдрав.</span><span class="sxs-lookup"><span data-stu-id="0160d-126">If the control finds the returned image has not been extracted, yet another TVN\_ASYNCDRAW notification may be sent by the control.</span></span>

<span data-ttu-id="0160d-127">Если изображение недоступно, идея асинхронного процесса заключается в том, чтобы разрешить родительскому приложению выполнять извлечение в фоновом режиме, чтобы извлечение не блокировало поток пользовательского интерфейса, то есть поток, на котором находится элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0160d-127">If an image is not available, the idea behind asynchronous is to allow the parent do the extraction in the background so that extraction does not block the UI thread, that is, the thread the control is on.</span></span> <span data-ttu-id="0160d-128">Родитель может вернуть \_ элемент управления адрф дравносинг, а затем запустить фоновый поток для извлечения значка.</span><span class="sxs-lookup"><span data-stu-id="0160d-128">The parent may return ADRF\_DRAWNOTHING to the control, then launch a background thread to extract the icon.</span></span> <span data-ttu-id="0160d-129">После извлечения родительский элемент может установить значок в элементе управления TreeView с помощью макроса [**TreeView \_ сетитем**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span><span class="sxs-lookup"><span data-stu-id="0160d-129">Once extracted, the parent may set the icon in the treeview control with macro [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span></span> <span data-ttu-id="0160d-130">Это приводит к тому, что представление дерева делает элемент недействительным и, в конечном итоге, перерисовывает его извлеченным изображением из списка изображений.</span><span class="sxs-lookup"><span data-stu-id="0160d-130">This causes tree-view to invalidate the item and eventually repaint it with the extracted image in the image list.</span></span>

<span data-ttu-id="0160d-131">В следующем примере кода, который будет использоваться как часть более крупной программы, показано, как родительский элемент может обрабатывать два возможных кода возврата в этом уведомлении с помощью элемента управления и решать, какие действия должен предпринять элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0160d-131">The following code example, to be used as part of a larger program, shows how a parent may process two possible return codes in this notification by a control, and decide what action the control should take.</span></span> <span data-ttu-id="0160d-132">Параметр **двретфлагс** не отображается.</span><span class="sxs-lookup"><span data-stu-id="0160d-132">Setting **dwRetFlags** is not shown.</span></span>


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a><span data-ttu-id="0160d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0160d-133">Requirements</span></span>



| <span data-ttu-id="0160d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0160d-134">Requirement</span></span> | <span data-ttu-id="0160d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0160d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0160d-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0160d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0160d-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0160d-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0160d-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0160d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0160d-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0160d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0160d-140">Header</span><span class="sxs-lookup"><span data-stu-id="0160d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0160d-141"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0160d-141"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





