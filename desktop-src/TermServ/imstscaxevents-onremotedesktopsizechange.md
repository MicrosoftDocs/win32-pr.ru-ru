---
title: Имстскаксевентс Онремотедесктопсизечанже, метод
description: Вызывается для указания того, что размер клиентского элемента управления в удаленном рабочем столе изменился в ответ на операцию клиентского управления.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онремотедесктопсизечанже
- Службы удаленных рабочих столов метода Онремотедесктопсизечанже, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онремотедесктопсизечанже
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534439"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a><span data-ttu-id="436a1-106">Метод Имстскаксевентс:: Онремотедесктопсизечанже</span><span class="sxs-lookup"><span data-stu-id="436a1-106">IMsTscAxEvents::OnRemoteDesktopSizeChange method</span></span>

<span data-ttu-id="436a1-107">Вызывается для указания того, что размер клиентского элемента управления в удаленном рабочем столе изменился в ответ на операцию клиентского управления.</span><span class="sxs-lookup"><span data-stu-id="436a1-107">Called to indicate that the size of the client control on the remote desktop has changed in response to a client control operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="436a1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="436a1-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="436a1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="436a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="436a1-110">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="436a1-110">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="436a1-111">Ширина (в пикселях) удаленного рабочего стола с измененным размером.</span><span class="sxs-lookup"><span data-stu-id="436a1-111">Width, in pixels, of the resized remote desktop.</span></span>

</dd> <dt>

<span data-ttu-id="436a1-112">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="436a1-112">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="436a1-113">Высота (в пикселях) удаленного рабочего стола с измененным размером.</span><span class="sxs-lookup"><span data-stu-id="436a1-113">Height, in pixels, of the resized remote desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="436a1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="436a1-114">Return value</span></span>

<span data-ttu-id="436a1-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="436a1-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="436a1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="436a1-116">Remarks</span></span>

<span data-ttu-id="436a1-117">Это событие позволяет контейнеру определить, должен ли он изменить свой размер в ответ на операцию клиентского управления, что может привести к увеличению объема видимого рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="436a1-117">This event allows the container to determine if it must resize itself in response to a client control operation, which could result in a larger viewable desktop size.</span></span> <span data-ttu-id="436a1-118">Обратите внимание, что элемент управления будет автоматически настраивать полосы прокрутки для нового размера сеанса.</span><span class="sxs-lookup"><span data-stu-id="436a1-118">Note that the control will automatically adjust scroll bars for the new session size.</span></span>

<span data-ttu-id="436a1-119">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="436a1-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="436a1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="436a1-120">Requirements</span></span>



| <span data-ttu-id="436a1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="436a1-121">Requirement</span></span> | <span data-ttu-id="436a1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="436a1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="436a1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="436a1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="436a1-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="436a1-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="436a1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="436a1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="436a1-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="436a1-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="436a1-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="436a1-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="436a1-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="436a1-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="436a1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="436a1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="436a1-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="436a1-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="436a1-131">IID</span><span class="sxs-lookup"><span data-stu-id="436a1-131">IID</span></span><br/>                      | <span data-ttu-id="436a1-132">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="436a1-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="436a1-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="436a1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="436a1-134">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="436a1-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





