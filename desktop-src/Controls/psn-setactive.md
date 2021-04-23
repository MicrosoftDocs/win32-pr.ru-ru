---
title: Код уведомления PSN_SETACTIVE (Пршт. h)
description: Уведомляет страницу о том, что она собирается активироваться. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988903"
---
# <a name="psn_setactive-notification-code"></a><span data-ttu-id="13acb-105">\_Код уведомления PSN сетактиве</span><span class="sxs-lookup"><span data-stu-id="13acb-105">PSN\_SETACTIVE notification code</span></span>

<span data-ttu-id="13acb-106">Уведомляет страницу о том, что она собирается активироваться.</span><span class="sxs-lookup"><span data-stu-id="13acb-106">Notifies a page that it is about to be activated.</span></span> <span data-ttu-id="13acb-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="13acb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="13acb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="13acb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13acb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13acb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13acb-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="13acb-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="13acb-111">Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="13acb-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="13acb-112">Член **lParam** структуры **пшнотифи** не содержит никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="13acb-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13acb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13acb-113">Return value</span></span>

<span data-ttu-id="13acb-114">Возвращает нуль, чтобы принять активацию, или-1, чтобы активировать следующую или предыдущую страницу (в зависимости от того, щелкнул пользователь кнопку " **Далее** " или " **назад** ").</span><span class="sxs-lookup"><span data-stu-id="13acb-114">Returns zero to accept the activation, or -1 to activate the next or the previous page (depending on whether the user clicked the **Next** or **Back** button).</span></span> <span data-ttu-id="13acb-115">Чтобы задать активацию для определенной страницы, возвратите идентификатор ресурса страницы.</span><span class="sxs-lookup"><span data-stu-id="13acb-115">To set the activation to a particular page, return the resource identifier of the page.</span></span>

## <a name="remarks"></a><span data-ttu-id="13acb-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13acb-116">Remarks</span></span>

<span data-ttu-id="13acb-117">\_Код уведомления PSN сетактиве отправляется перед отображением страницы.</span><span class="sxs-lookup"><span data-stu-id="13acb-117">The PSN\_SETACTIVE notification code is sent before the page is visible.</span></span> <span data-ttu-id="13acb-118">Приложение может использовать этот код уведомления для инициализации данных на странице.</span><span class="sxs-lookup"><span data-stu-id="13acb-118">An application can use this notification code to initialize data in the page.</span></span>

> [!Note]  
> <span data-ttu-id="13acb-119">Страница свойств находится в процессе управления списком страниц при \_ отправке кода уведомления PSN сетактиве.</span><span class="sxs-lookup"><span data-stu-id="13acb-119">The property sheet is in the process of manipulating the list of pages when the PSN\_SETACTIVE notification code is sent.</span></span> <span data-ttu-id="13acb-120">Не пытайтесь добавлять, удалять или вставлять страницы при обработке этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="13acb-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="13acb-121">Это приведет к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="13acb-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="13acb-122">Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна использовать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с \_ значением мсгресулт DWL, а процедура диалогового окна должна возвращать значение **true**.</span><span class="sxs-lookup"><span data-stu-id="13acb-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="13acb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="13acb-123">Requirements</span></span>



| <span data-ttu-id="13acb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="13acb-124">Requirement</span></span> | <span data-ttu-id="13acb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="13acb-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13acb-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13acb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="13acb-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13acb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="13acb-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13acb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="13acb-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13acb-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="13acb-130">Header</span><span class="sxs-lookup"><span data-stu-id="13acb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="13acb-131"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="13acb-131"><dt>Prsht.h</dt></span></span> </dl> |



 

