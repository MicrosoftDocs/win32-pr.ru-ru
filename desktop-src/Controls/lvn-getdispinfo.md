---
title: Код уведомления LVN_GETDISPINFO (Коммктрл. h)
description: Отправляется элементом управления "представление списка" в его родительское окно. Это запрос к родительскому окну для предоставления сведений, необходимых для отображения или сортировки элемента представления списка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804151"
---
# <a name="lvn_getdispinfo-notification-code"></a><span data-ttu-id="c878d-106">\_Код уведомления ЛВН жетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="c878d-106">LVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="c878d-107">Отправляется элементом управления "представление списка" в его родительское окно.</span><span class="sxs-lookup"><span data-stu-id="c878d-107">Sent by a list-view control to its parent window.</span></span> <span data-ttu-id="c878d-108">Это запрос к родительскому окну для предоставления сведений, необходимых для отображения или сортировки элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="c878d-108">It is a request for the parent window to provide information needed to display or sort a list-view item.</span></span> <span data-ttu-id="c878d-109">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c878d-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="c878d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c878d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c878d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c878d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c878d-112">Указатель на структуру [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="c878d-112">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="c878d-113">Во входных данных структура [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , содержащаяся в этой структуре, указывает тип необходимой информации и определяет нужный элемент или подэлемент.</span><span class="sxs-lookup"><span data-stu-id="c878d-113">On input, the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure contained in this structure specifies the type of information required and identifies the item or subitem of interest.</span></span> <span data-ttu-id="c878d-114">Используйте структуру **лвитем** для возврата запрошенной информации в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="c878d-114">Use the **LVITEM** structure to return the requested information to the control.</span></span> <span data-ttu-id="c878d-115">Если обработчик сообщений устанавливает \_ флаг лвиф di \_ сетитем в элементе **Mask** структуры **лвитем** , то элемент управления "представление списка" сохраняет запрашиваемые сведения и больше не запрашивает их.</span><span class="sxs-lookup"><span data-stu-id="c878d-115">If your message handler sets the LVIF\_DI\_SETITEM flag in the **mask** member of the **LVITEM** structure, the list-view control stores the requested information and will not ask for it again.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c878d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c878d-116">Return value</span></span>

<span data-ttu-id="c878d-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="c878d-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c878d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c878d-118">Remarks</span></span>

<span data-ttu-id="c878d-119">Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="c878d-119">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="c878d-120">Параметр *wParam* содержит код уведомления.</span><span class="sxs-lookup"><span data-stu-id="c878d-120">The *wParam* parameter contains the notification code.</span></span>

<span data-ttu-id="c878d-121">Элемент управления "представление списка" отправляет код уведомления **ЛВН \_ жетдиспинфо** для получения сведений об элементе, который хранится приложением, а не элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c878d-121">A list-view control sends the **LVN\_GETDISPINFO** notification code to retrieve item information that is stored by the application rather than the control.</span></span> <span data-ttu-id="c878d-122">Сведения могут быть сведениями о тексте или значке для элемента.</span><span class="sxs-lookup"><span data-stu-id="c878d-122">The information can be text or icon information for an item.</span></span> <span data-ttu-id="c878d-123">Это также может быть информация о состоянии элемента.</span><span class="sxs-lookup"><span data-stu-id="c878d-123">It can also be item state information.</span></span> <span data-ttu-id="c878d-124">Дополнительные сведения о реализации состояния элемента при обратном вызове см. в сообщении [**LVM \_ сеткаллбаккмаск**](lvm-setcallbackmask.md) .</span><span class="sxs-lookup"><span data-stu-id="c878d-124">See the [**LVM\_SETCALLBACKMASK**](lvm-setcallbackmask.md) message for more information on implementing item state on a callback basis.</span></span>

<span data-ttu-id="c878d-125">Дополнительные сведения о обратных вызовах в представлении списка см. [в разделе элементы обратного вызова и маска обратного вызова](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c878d-125">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c878d-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="c878d-126">Examples</span></span>

<span data-ttu-id="c878d-127">В следующем примере показано, как можно обработать этот код уведомления, чтобы задать текст в столбцах представления списка.</span><span class="sxs-lookup"><span data-stu-id="c878d-127">The following example shows how this notification code might be handled to set the text in the columns of a list view.</span></span> <span data-ttu-id="c878d-128">Данные для каждого элемента хранятся в следующей структуре.</span><span class="sxs-lookup"><span data-stu-id="c878d-128">The data for each item is held in the following structure.</span></span>


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



<span data-ttu-id="c878d-129">Ниже приведен \_ обработчик уведомлений WM в процедуре диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c878d-129">The following is from the WM\_NOTIFY handler in the dialog procedure.</span></span>


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a><span data-ttu-id="c878d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c878d-130">Requirements</span></span>



| <span data-ttu-id="c878d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c878d-131">Requirement</span></span> | <span data-ttu-id="c878d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c878d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c878d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c878d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c878d-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c878d-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c878d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c878d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c878d-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c878d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c878d-137">Header</span><span class="sxs-lookup"><span data-stu-id="c878d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c878d-138"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c878d-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c878d-139">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c878d-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c878d-140">**ЛВН \_ ЖЕТДИСПИНФОВ** (Юникод) и **ЛВН \_ жетдиспинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c878d-140">**LVN\_GETDISPINFOW** (Unicode) and **LVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="c878d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c878d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c878d-142">**ЛВН \_ сетдиспинфо**</span><span class="sxs-lookup"><span data-stu-id="c878d-142">**LVN\_SETDISPINFO**</span></span>](lvn-setdispinfo.md)
</dt> </dl>

 

 





