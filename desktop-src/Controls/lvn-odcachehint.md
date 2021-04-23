---
title: Код уведомления LVN_ODCACHEHINT (Коммктрл. h)
description: Отправляется с помощью виртуального элемента управления "представление списка", когда содержимое его области отображения изменилось.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989445"
---
# <a name="lvn_odcachehint-notification-code"></a><span data-ttu-id="cb583-104">\_Код уведомления ЛВН одкачехинт</span><span class="sxs-lookup"><span data-stu-id="cb583-104">LVN\_ODCACHEHINT notification code</span></span>

<span data-ttu-id="cb583-105">Отправляется с помощью виртуального элемента управления "представление списка", когда содержимое его области отображения изменилось.</span><span class="sxs-lookup"><span data-stu-id="cb583-105">Sent by a virtual list-view control when the contents of its display area have changed.</span></span> <span data-ttu-id="cb583-106">Например, элемент управления "представление списка" отправляет этот код уведомления, когда пользователь прокручивает отображение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cb583-106">For example, a list-view control sends this notification code when the user scrolls the control's display.</span></span> <span data-ttu-id="cb583-107">\_Код уведомления ЛВН одкачехинт отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cb583-107">The LVN\_ODCACHEHINT notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cb583-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb583-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb583-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb583-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb583-110">Указатель на структуру [**нмлвкачехинт**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) , содержащую сведения о диапазоне элементов для кэширования.</span><span class="sxs-lookup"><span data-stu-id="cb583-110">Pointer to an [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) structure containing information about the range of items to be cached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb583-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb583-111">Return value</span></span>

<span data-ttu-id="cb583-112">Приложение, получающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="cb583-112">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb583-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb583-113">Remarks</span></span>

<span data-ttu-id="cb583-114">Обработка этого сообщения позволяет приложению обновлять сведения об элементе в кэше, чтобы они были доступны при отправке кода уведомления [ЛВН \_ жетдиспинфо](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="cb583-114">Handling this message allows the application to update the item information held in cache so that it is readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification code is sent.</span></span>

<span data-ttu-id="cb583-115">Обратите внимание, что этот код уведомления не всегда является точным представлением элементов, которые будут запрошены [ЛВН \_ жетдиспинфо](lvn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="cb583-115">Note that this notification code is not always an exact representation of the items that will be requested by [LVN\_GETDISPINFO](lvn-getdispinfo.md).</span></span> <span data-ttu-id="cb583-116">Таким образом, если запрошенный элемент не кэшируется при обработке ЛВН \_ жетдиспинфо, приложение должно быть подготовлено к предоставлению запрошенной информации из источника за пределами кэша.</span><span class="sxs-lookup"><span data-stu-id="cb583-116">Therefore, if the requested item is not cached while handling LVN\_GETDISPINFO, the application must be prepared to supply the requested information from a source outside the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb583-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cb583-117">Requirements</span></span>



| <span data-ttu-id="cb583-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cb583-118">Requirement</span></span> | <span data-ttu-id="cb583-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cb583-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb583-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb583-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb583-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb583-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb583-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb583-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb583-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb583-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb583-124">Header</span><span class="sxs-lookup"><span data-stu-id="cb583-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb583-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb583-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





