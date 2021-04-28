---
description: SMC_GETOBJECT сообщение — запрашивает указатель на указанный объект.
title: Сообщение SMC_GETOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58741290d741cc18fd788282d0f302ef87bb15dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100442"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="be086-103">\_Сообщение SMC GetObject</span><span class="sxs-lookup"><span data-stu-id="be086-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="be086-104">Запрашивает указатель на указанный объект.</span><span class="sxs-lookup"><span data-stu-id="be086-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="be086-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="be086-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be086-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="be086-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="be086-107">IID, связанный с запрошенным объектом.</span><span class="sxs-lookup"><span data-stu-id="be086-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="be086-108">*PV*</span><span class="sxs-lookup"><span data-stu-id="be086-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="be086-109">Указатель void, получающий указатель на запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="be086-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be086-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be086-110">Return value</span></span>

<span data-ttu-id="be086-111">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="be086-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="be086-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="be086-112">Remarks</span></span>

<span data-ttu-id="be086-113">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="be086-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="be086-114">Создайте запрошенный объект и присвойте указатель на запрашиваемый интерфейс *ПС*.</span><span class="sxs-lookup"><span data-stu-id="be086-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="be086-115">Могут быть запрошены следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="be086-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="be086-116">**ишеллмену**</span><span class="sxs-lookup"><span data-stu-id="be086-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="be086-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="be086-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="be086-118">**ишеллменукаллбакк**</span><span class="sxs-lookup"><span data-stu-id="be086-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="be086-119">**Интерфейс IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="be086-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="be086-120">Требования</span><span class="sxs-lookup"><span data-stu-id="be086-120">Requirements</span></span>



| <span data-ttu-id="be086-121">Требование</span><span class="sxs-lookup"><span data-stu-id="be086-121">Requirement</span></span> | <span data-ttu-id="be086-122">Значение</span><span class="sxs-lookup"><span data-stu-id="be086-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be086-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be086-123">Minimum supported client</span></span><br/> | <span data-ttu-id="be086-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be086-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="be086-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be086-125">Minimum supported server</span></span><br/> | <span data-ttu-id="be086-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be086-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be086-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="be086-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="be086-128"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be086-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="be086-129">IDL</span><span class="sxs-lookup"><span data-stu-id="be086-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be086-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be086-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
