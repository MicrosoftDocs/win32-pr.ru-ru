---
description: SMC_GETSFOBJECT сообщение — запрашивает указатель на указанный объект.
title: Сообщение SMC_GETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 612b43c193cd1919db4a5cf9dba3a8fdba1c81c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086612"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="7d6d8-103">\_Сообщение SMC жетсфобжект</span><span class="sxs-lookup"><span data-stu-id="7d6d8-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="7d6d8-104">Запрашивает указатель на указанный объект.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="7d6d8-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d6d8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6d8-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="7d6d8-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6d8-107">IID, связанный с запрошенным объектом.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="7d6d8-108">*PV*</span><span class="sxs-lookup"><span data-stu-id="7d6d8-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6d8-109">Указатель void, получающий указатель на запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6d8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d6d8-110">Return value</span></span>

<span data-ttu-id="7d6d8-111">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d6d8-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="7d6d8-112">Remarks</span></span>

<span data-ttu-id="7d6d8-113">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="7d6d8-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="7d6d8-114">Он аналогичен [**SMC \_ GetObject**](smc-getobject.md) , но используется для элементов папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="7d6d8-115">Создайте запрошенный объект и присвойте указатель на запрашиваемый интерфейс *ПС*.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="7d6d8-116">Могут быть запрошены следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="7d6d8-117">**IStream**</span><span class="sxs-lookup"><span data-stu-id="7d6d8-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="7d6d8-118">**ишеллмену**</span><span class="sxs-lookup"><span data-stu-id="7d6d8-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="7d6d8-119">**ишеллменукаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7d6d8-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="7d6d8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7d6d8-120">Requirements</span></span>



| <span data-ttu-id="7d6d8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7d6d8-121">Requirement</span></span> | <span data-ttu-id="7d6d8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7d6d8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6d8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d6d8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7d6d8-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d6d8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7d6d8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d6d8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7d6d8-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d6d8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7d6d8-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7d6d8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d6d8-128"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d6d8-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d6d8-129">IDL</span><span class="sxs-lookup"><span data-stu-id="7d6d8-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7d6d8-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7d6d8-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
