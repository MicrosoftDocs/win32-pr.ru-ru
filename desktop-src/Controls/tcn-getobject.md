---
title: Код уведомления TCN_GETOBJECT (Коммктрл. h)
description: Посылается элементом управления "Вкладка", когда он имеет \_ \_ Расширенный стиль TCS ex регистердроп, и объект перетаскивается над элементом вкладки в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654408"
---
# <a name="tcn_getobject-notification-code"></a><span data-ttu-id="32c59-105">\_Код уведомления ТКН GetObject</span><span class="sxs-lookup"><span data-stu-id="32c59-105">TCN\_GETOBJECT notification code</span></span>

<span data-ttu-id="32c59-106">Посылается элементом управления "Вкладка", когда он имеет расширенный стиль [**TCS \_ ex \_ регистердроп**](tab-control-extended-styles.md) , и объект перетаскивается над элементом вкладки в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="32c59-106">Sent by a tab control when it has the [**TCS\_EX\_REGISTERDROP**](tab-control-extended-styles.md) extended style and an object is dragged over a tab item in the control.</span></span> <span data-ttu-id="32c59-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="32c59-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="32c59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="32c59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32c59-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32c59-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32c59-110">Указатель на структуру [**нмобжектнотифи**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) , содержащую сведения об элементе вкладки, на который перетаскивается объект, и получает данные, возвращаемые приложением в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="32c59-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the tab item the object is dragged over and receives data the application returns in response to this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32c59-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32c59-111">Return value</span></span>

<span data-ttu-id="32c59-112">Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="32c59-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c59-113">Требования</span><span class="sxs-lookup"><span data-stu-id="32c59-113">Requirements</span></span>



| <span data-ttu-id="32c59-114">Требование</span><span class="sxs-lookup"><span data-stu-id="32c59-114">Requirement</span></span> | <span data-ttu-id="32c59-115">Значение</span><span class="sxs-lookup"><span data-stu-id="32c59-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32c59-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32c59-116">Minimum supported client</span></span><br/> | <span data-ttu-id="32c59-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32c59-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32c59-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32c59-118">Minimum supported server</span></span><br/> | <span data-ttu-id="32c59-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32c59-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32c59-120">Header</span><span class="sxs-lookup"><span data-stu-id="32c59-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="32c59-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="32c59-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





