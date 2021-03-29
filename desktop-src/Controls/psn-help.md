---
title: Код уведомления PSN_HELP (Пршт. h)
description: Уведомляет страницу о нажатии пользователем кнопки Справка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- PSN_HELP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654547"
---
# <a name="psn_help-notification-code"></a><span data-ttu-id="e422f-105">\_Код уведомления PSN Help</span><span class="sxs-lookup"><span data-stu-id="e422f-105">PSN\_HELP notification code</span></span>

<span data-ttu-id="e422f-106">Уведомляет страницу о нажатии пользователем кнопки Справка.</span><span class="sxs-lookup"><span data-stu-id="e422f-106">Notifies a page that the user has clicked the Help button.</span></span> <span data-ttu-id="e422f-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e422f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e422f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e422f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e422f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e422f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e422f-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="e422f-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="e422f-111">Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="e422f-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="e422f-112">Член **lParam** структуры **пшнотифи** не содержит никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="e422f-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e422f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e422f-113">Return value</span></span>

<span data-ttu-id="e422f-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e422f-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e422f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e422f-115">Remarks</span></span>

<span data-ttu-id="e422f-116">Приложение должно отображать справочные сведения о странице.</span><span class="sxs-lookup"><span data-stu-id="e422f-116">An application should display Help information for the page.</span></span>

> [!Note]  
> <span data-ttu-id="e422f-117">Этот код уведомления не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="e422f-117">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e422f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e422f-118">Requirements</span></span>



| <span data-ttu-id="e422f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e422f-119">Requirement</span></span> | <span data-ttu-id="e422f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e422f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e422f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e422f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e422f-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e422f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e422f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e422f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e422f-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e422f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e422f-125">Header</span><span class="sxs-lookup"><span data-stu-id="e422f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e422f-126"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="e422f-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





