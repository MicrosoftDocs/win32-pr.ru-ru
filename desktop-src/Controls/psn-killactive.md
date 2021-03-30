---
title: Код уведомления PSN_KILLACTIVE (Пршт. h)
description: Уведомляет страницу о том, что она собирается потерять активацию из-за активации другой страницы или нажатия пользователем кнопки ОК. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988548"
---
# <a name="psn_killactive-notification-code"></a><span data-ttu-id="0a45b-105">\_Код уведомления PSN киллактиве</span><span class="sxs-lookup"><span data-stu-id="0a45b-105">PSN\_KILLACTIVE notification code</span></span>

<span data-ttu-id="0a45b-106">Уведомляет страницу о том, что она собирается потерять активацию из-за активации другой страницы или нажатия пользователем кнопки ОК.</span><span class="sxs-lookup"><span data-stu-id="0a45b-106">Notifies a page that it is about to lose activation either because another page is being activated or the user has clicked the OK button.</span></span> <span data-ttu-id="0a45b-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0a45b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0a45b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a45b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a45b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a45b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a45b-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="0a45b-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="0a45b-111">Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="0a45b-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="0a45b-112">Член **lParam** структуры **пшнотифи** не содержит никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="0a45b-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a45b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a45b-113">Return value</span></span>

<span data-ttu-id="0a45b-114">Возвращает **значение true** , чтобы предотвратить потерю страницы при активации, или **false** , чтобы разрешить ее.</span><span class="sxs-lookup"><span data-stu-id="0a45b-114">Returns **TRUE** to prevent the page from losing the activation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a45b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a45b-115">Remarks</span></span>

<span data-ttu-id="0a45b-116">Приложение обрабатывает этот код уведомления для проверки вводимых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="0a45b-116">An application handles this notification code to validate the information the user has entered.</span></span>

> [!Note]  
> <span data-ttu-id="0a45b-117">Страница свойств находится в процессе управления списком страниц при \_ отправке кода уведомления PSN киллактиве.</span><span class="sxs-lookup"><span data-stu-id="0a45b-117">The property sheet is in the process of manipulating the list of pages when the PSN\_KILLACTIVE notification code is sent.</span></span> <span data-ttu-id="0a45b-118">Не пытайтесь добавлять, удалять или вставлять страницы при обработке этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="0a45b-118">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="0a45b-119">Это приведет к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="0a45b-119">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="0a45b-120">Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна вызвать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с \_ параметром DWL мсгресулт, для которого задано возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="0a45b-120">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a DWL\_MSGRESULT value set to the return value.</span></span> <span data-ttu-id="0a45b-121">Процедура диалогового окна должна возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0a45b-121">The dialog box procedure must return **TRUE**.</span></span>

<span data-ttu-id="0a45b-122">Если процедура диалогового окна устанавливает \_ для DWL Мсгресулт **значение true**, для объяснения проблемы пользователю должно отобразиться окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="0a45b-122">If the dialog box procedure sets DWL\_MSGRESULT to **TRUE**, it should display a message box to explain the problem to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a45b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0a45b-123">Requirements</span></span>



| <span data-ttu-id="0a45b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0a45b-124">Requirement</span></span> | <span data-ttu-id="0a45b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0a45b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a45b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a45b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0a45b-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a45b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0a45b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a45b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0a45b-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a45b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0a45b-130">Header</span><span class="sxs-lookup"><span data-stu-id="0a45b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a45b-131"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a45b-131"><dt>Prsht.h</dt></span></span> </dl> |



 

