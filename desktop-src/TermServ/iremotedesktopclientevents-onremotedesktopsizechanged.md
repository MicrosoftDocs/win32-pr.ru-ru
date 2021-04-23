---
title: Иремотедесктопклиентевентс Онремотедесктопсизечанжед, метод
description: Вызывается при изменении размера удаленного рабочего стола.
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онремотедесктопсизечанжед
- Службы удаленных рабочих столов метода Онремотедесктопсизечанжед, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онремотедесктопсизечанжед
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802140"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a><span data-ttu-id="f2727-106">Метод Иремотедесктопклиентевентс:: Онремотедесктопсизечанжед</span><span class="sxs-lookup"><span data-stu-id="f2727-106">IRemoteDesktopClientEvents::OnRemoteDesktopSizeChanged method</span></span>

<span data-ttu-id="f2727-107">Вызывается при изменении размера удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="f2727-107">Called when the remote desktop size has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2727-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2727-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="f2727-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2727-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2727-110">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2727-110">*width* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f2727-111">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2727-111">*height* \[in\]</span></span>
<span data-ttu-id="f2727-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f2727-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="f2727-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2727-113">Return value</span></span>

<span data-ttu-id="f2727-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f2727-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2727-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f2727-115">Requirements</span></span>



| <span data-ttu-id="f2727-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f2727-116">Requirement</span></span> | <span data-ttu-id="f2727-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f2727-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2727-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2727-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f2727-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f2727-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="f2727-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2727-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f2727-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2727-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="f2727-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f2727-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2727-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2727-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="f2727-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f2727-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2727-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2727-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="f2727-126">IID</span><span class="sxs-lookup"><span data-stu-id="f2727-126">IID</span></span><br/>                      | <span data-ttu-id="f2727-127">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="f2727-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2727-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2727-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2727-129">**иремотедесктопклиентевентс**</span><span class="sxs-lookup"><span data-stu-id="f2727-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





