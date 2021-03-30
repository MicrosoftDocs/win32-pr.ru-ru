---
title: Код уведомления HDN_GETDISPINFO (Коммктрл. h)
description: Посылается владельцу элемента управления "заголовок", когда элементу управления требуются сведения об элементе заголовка обратного вызова. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071197"
---
# <a name="hdn_getdispinfo-notification-code"></a><span data-ttu-id="26a8b-105">\_Код уведомления ХДН жетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="26a8b-105">HDN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="26a8b-106">Посылается владельцу элемента управления "заголовок", когда элементу управления требуются сведения об элементе заголовка обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="26a8b-106">Sent to the owner of a header control when the control needs information about a callback header item.</span></span> <span data-ttu-id="26a8b-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="26a8b-107">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="26a8b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="26a8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26a8b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26a8b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26a8b-110">Указатель на структуру [**нмхддиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="26a8b-110">A pointer to an [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure.</span></span> <span data-ttu-id="26a8b-111">В поле входные данные поля структуры указывают требуемые сведения и интересующий элемент.</span><span class="sxs-lookup"><span data-stu-id="26a8b-111">On input, the fields of the structure specify what information is required and the item of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26a8b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26a8b-112">Return value</span></span>

<span data-ttu-id="26a8b-113">Возвращает LRESULT.</span><span class="sxs-lookup"><span data-stu-id="26a8b-113">Returns an LRESULT.</span></span>

## <a name="remarks"></a><span data-ttu-id="26a8b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26a8b-114">Remarks</span></span>

<span data-ttu-id="26a8b-115">Заполните соответствующие члены структуры, чтобы вернуть запрошенные сведения в элемент управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="26a8b-115">Fill the appropriate members of the structure to return the requested information to the header control.</span></span> <span data-ttu-id="26a8b-116">Если обработчик сообщений устанавливает для элемента **маски** структуры [**нмхддиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) значение HDi \_ di \_ сетитем, то элемент управления "заголовок" сохраняет информацию и не запрашивает их снова.</span><span class="sxs-lookup"><span data-stu-id="26a8b-116">If your message handler sets the **mask** member of the [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure to HDI\_DI\_SETITEM, the header control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="26a8b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="26a8b-117">Requirements</span></span>



| <span data-ttu-id="26a8b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="26a8b-118">Requirement</span></span> | <span data-ttu-id="26a8b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="26a8b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26a8b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26a8b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26a8b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26a8b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26a8b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26a8b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26a8b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26a8b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26a8b-124">Header</span><span class="sxs-lookup"><span data-stu-id="26a8b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="26a8b-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="26a8b-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="26a8b-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="26a8b-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="26a8b-127">**ХДН \_ ЖЕТДИСПИНФОВ** (Юникод) и **ХДН \_ жетдиспинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="26a8b-127">**HDN\_GETDISPINFOW** (Unicode) and **HDN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





