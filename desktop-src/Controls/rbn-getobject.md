---
title: Код уведомления RBN_GETOBJECT (Коммктрл. h)
description: Посылается элементом управления "Главная панель", созданным с помощью \_ стиля RBS регистердроп, при перетаскивании объекта на полосу в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136630"
---
# <a name="rbn_getobject-notification-code"></a><span data-ttu-id="d8735-105">\_Код уведомления РБН GetObject</span><span class="sxs-lookup"><span data-stu-id="d8735-105">RBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="d8735-106">Посылается элементом управления "Главная панель", созданным с помощью стиля [**RBS \_ регистердроп**](rebar-control-styles.md) , при перетаскивании объекта на полосу в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="d8735-106">Sent by a rebar control created with the [**RBS\_REGISTERDROP**](rebar-control-styles.md) style when an object is dragged over a band in the control.</span></span> <span data-ttu-id="d8735-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8735-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d8735-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8735-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8735-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8735-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8735-110">Указатель на структуру [**нмобжектнотифи**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) , содержащую сведения о полосе, на которую перетаскивается объект, а также данные, предоставленные принимающим приложением в ответ на этот код уведомления.</span><span class="sxs-lookup"><span data-stu-id="d8735-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the band that the object is dragged over and also receives the data provided by the receiving application in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8735-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8735-111">Return value</span></span>

<span data-ttu-id="d8735-112">Возвращаемое значение для этого кода уведомления должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d8735-112">The return value for this notification code must be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8735-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8735-113">Remarks</span></span>

<span data-ttu-id="d8735-114">Чтобы получить \_ код уведомления РБН GetObject, инициализируйте OLE с помощью вызова [**Олеинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) или [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="d8735-114">To receive the RBN\_GETOBJECT notification code, initialize OLE with a call to [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) or [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8735-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d8735-115">Requirements</span></span>



| <span data-ttu-id="d8735-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d8735-116">Requirement</span></span> | <span data-ttu-id="d8735-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d8735-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8735-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8735-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d8735-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8735-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8735-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8735-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d8735-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8735-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8735-122">Header</span><span class="sxs-lookup"><span data-stu-id="d8735-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8735-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8735-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

