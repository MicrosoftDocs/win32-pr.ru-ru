---
title: Системмонитор. Мануалупдате, свойство
description: Возвращает или задает значение, указывающее, будет ли содержимое системного монитора обновляться вручную или автоматически с указанными интервалами.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- Сисмон свойство Мануалупдате
- Мануалупдате Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Мануалупдате
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661889"
---
# <a name="systemmonitormanualupdate-property"></a><span data-ttu-id="cc9c0-106">Системмонитор. Мануалупдате, свойство</span><span class="sxs-lookup"><span data-stu-id="cc9c0-106">SystemMonitor.ManualUpdate property</span></span>

<span data-ttu-id="cc9c0-107">Возвращает или задает значение, указывающее, будет ли содержимое системного монитора обновляться вручную или автоматически с указанными интервалами.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-107">Retrieves or sets a value indicating whether the contents of the System Monitor will be updated manually, or automatically at specified intervals.</span></span>

<span data-ttu-id="cc9c0-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc9c0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc9c0-109">Syntax</span></span>


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="cc9c0-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cc9c0-110">Property value</span></span>

<span data-ttu-id="cc9c0-111">Значение true указывает, что граф обновляется вручную.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-111">True indicates that graph is updated manually.</span></span> <span data-ttu-id="cc9c0-112">Значение false указывает, что граф обновляется автоматически на основе интервала обновления, указанного в [**системмонитор. упдатеинтервал**](systemmonitor-updateinterval.md).</span><span class="sxs-lookup"><span data-stu-id="cc9c0-112">False indicates that the graph is updated automatically based on the update interval specified in [**SystemMonitor.UpdateInterval**](systemmonitor-updateinterval.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc9c0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc9c0-113">Remarks</span></span>

<span data-ttu-id="cc9c0-114">По умолчанию граф обновляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="cc9c0-114">By default, the graph is updated automatically.</span></span>

<span data-ttu-id="cc9c0-115">Чтобы обновить граф вручную, вызовите метод [**системмонитор. коллектсампле**](systemmonitor-collectsample.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9c0-115">To update the graph manually, call the [**SystemMonitor.CollectSample**](systemmonitor-collectsample.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc9c0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cc9c0-116">Requirements</span></span>



| <span data-ttu-id="cc9c0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cc9c0-117">Requirement</span></span> | <span data-ttu-id="cc9c0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cc9c0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9c0-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc9c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cc9c0-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc9c0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cc9c0-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc9c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cc9c0-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc9c0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc9c0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cc9c0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc9c0-124"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cc9c0-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc9c0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc9c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc9c0-126">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="cc9c0-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="cc9c0-127">**Системмонитор. Коллектсампле**</span><span class="sxs-lookup"><span data-stu-id="cc9c0-127">**SystemMonitor.CollectSample**</span></span>](systemmonitor-collectsample.md)
</dt> <dt>

[<span data-ttu-id="cc9c0-128">**Системмонитор. Упдатеграф**</span><span class="sxs-lookup"><span data-stu-id="cc9c0-128">**SystemMonitor.UpdateGraph**</span></span>](systemmonitor-updategraph.md)
</dt> </dl>

 

 





