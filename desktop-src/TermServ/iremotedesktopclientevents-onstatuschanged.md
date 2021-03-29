---
title: Метод Иремотедесктопклиентевентс Онстатусчанжед (Локатионапи. h)
description: Вызывается, когда клиентский элемент управления обновил свое состояние.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онстатусчанжед
- Службы удаленных рабочих столов метода Онстатусчанжед, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онстатусчанжед
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492771"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a><span data-ttu-id="23664-106">Метод Иремотедесктопклиентевентс:: Онстатусчанжед</span><span class="sxs-lookup"><span data-stu-id="23664-106">IRemoteDesktopClientEvents::OnStatusChanged method</span></span>

<span data-ttu-id="23664-107">Вызывается, когда клиентский элемент управления обновил свое состояние.</span><span class="sxs-lookup"><span data-stu-id="23664-107">Called when the client control has updated its status.</span></span>

## <a name="syntax"></a><span data-ttu-id="23664-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23664-108">Syntax</span></span>


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a><span data-ttu-id="23664-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="23664-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23664-110">*statusCode*</span><span class="sxs-lookup"><span data-stu-id="23664-110">*statusCode*</span></span> 
</dt> <dd>

<span data-ttu-id="23664-111">Новый код состояния.</span><span class="sxs-lookup"><span data-stu-id="23664-111">The new status code.</span></span>

</dd> <dt>

<span data-ttu-id="23664-112">*statusMessage*</span><span class="sxs-lookup"><span data-stu-id="23664-112">*statusMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="23664-113">Текст сообщения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="23664-113">The status message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23664-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23664-114">Return value</span></span>

<span data-ttu-id="23664-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="23664-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="23664-116">Требования</span><span class="sxs-lookup"><span data-stu-id="23664-116">Requirements</span></span>



| <span data-ttu-id="23664-117">Требование</span><span class="sxs-lookup"><span data-stu-id="23664-117">Requirement</span></span> | <span data-ttu-id="23664-118">Значение</span><span class="sxs-lookup"><span data-stu-id="23664-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23664-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23664-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23664-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="23664-120">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="23664-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23664-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23664-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23664-122">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="23664-123">Header</span><span class="sxs-lookup"><span data-stu-id="23664-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="23664-124"><dt>Локатионапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="23664-124"><dt>Locationapi.h</dt></span></span> </dl>       |
| <span data-ttu-id="23664-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="23664-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="23664-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23664-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="23664-127">DLL</span><span class="sxs-lookup"><span data-stu-id="23664-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23664-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23664-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="23664-129">IID</span><span class="sxs-lookup"><span data-stu-id="23664-129">IID</span></span><br/>                      | <span data-ttu-id="23664-130">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="23664-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23664-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23664-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23664-132">**иремотедесктопклиентевентс**</span><span class="sxs-lookup"><span data-stu-id="23664-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





