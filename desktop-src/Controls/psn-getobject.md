---
title: Код уведомления PSN_GETOBJECT (Пршт. h)
description: Отправляется странице свойств для запроса целевого объекта Drop, когда курсор передается над одной из кнопок элемента управления Tab. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071328"
---
# <a name="psn_getobject-notification-code"></a><span data-ttu-id="da89a-105">\_Код уведомления PSN GetObject</span><span class="sxs-lookup"><span data-stu-id="da89a-105">PSN\_GETOBJECT notification code</span></span>

<span data-ttu-id="da89a-106">Отправляется странице свойств для запроса целевого объекта Drop, когда курсор передается над одной из кнопок элемента управления Tab.</span><span class="sxs-lookup"><span data-stu-id="da89a-106">Sent by a property sheet to request a drop target object when the cursor passes over one of the tab control's buttons.</span></span> <span data-ttu-id="da89a-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="da89a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="da89a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="da89a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da89a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da89a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da89a-110">Указатель на структуру [**нмобжектнотифи**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) , которая в записи содержит сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="da89a-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that, on entry, contains information about the notification code.</span></span> <span data-ttu-id="da89a-111">Если этот код уведомления обрабатывается, необходимо вставить сведения об объекте в эту структуру.</span><span class="sxs-lookup"><span data-stu-id="da89a-111">If this notification code is processed, you must insert object information into this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da89a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da89a-112">Return value</span></span>

<span data-ttu-id="da89a-113">Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="da89a-113">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="da89a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da89a-114">Remarks</span></span>

<span data-ttu-id="da89a-115">Чтобы предоставить объект, приложение должно задать значения в некоторых членах структуры [**нмобжектнотифи**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) при значении *lParam*.</span><span class="sxs-lookup"><span data-stu-id="da89a-115">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="da89a-116">Элементу **объект** должен быть присвоен допустимый указатель на объект, а элементу **hResult** должен быть присвоен флаг Success.</span><span class="sxs-lookup"><span data-stu-id="da89a-116">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="da89a-117">Для обеспечения соответствия стандартам модели COM всегда увеличивать число ссылок объекта при предоставлении указателя на объект.</span><span class="sxs-lookup"><span data-stu-id="da89a-117">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="da89a-118">Если приложение не предоставляет объект, оно должно установить для **объект** **значение NULL** , а для **hResult** — флаг сбоя.</span><span class="sxs-lookup"><span data-stu-id="da89a-118">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

> [!Note]  
> <span data-ttu-id="da89a-119">Этот код уведомления не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="da89a-119">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da89a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="da89a-120">Requirements</span></span>



| <span data-ttu-id="da89a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="da89a-121">Requirement</span></span> | <span data-ttu-id="da89a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="da89a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da89a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da89a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="da89a-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da89a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="da89a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da89a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="da89a-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da89a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="da89a-127">Header</span><span class="sxs-lookup"><span data-stu-id="da89a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="da89a-128"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="da89a-128"><dt>Prsht.h</dt></span></span> </dl> |



 

 





