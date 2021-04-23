---
title: Системмонитор. Шовтимеаксислабелс, свойство
description: Возвращает или задает значение, определяющее, содержит ли горизонтальная ось (X) представления графа метки.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Сисмон свойство Шовтимеаксислабелс
- Свойство Шовтимеаксислабелс Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, свойство Шовтимеаксислабелс
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661847"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a><span data-ttu-id="0a4b3-106">Системмонитор. Шовтимеаксислабелс, свойство</span><span class="sxs-lookup"><span data-stu-id="0a4b3-106">SystemMonitor.ShowTimeAxisLabels property</span></span>

<span data-ttu-id="0a4b3-107">Возвращает или задает значение, определяющее, содержит ли горизонтальная ось (X) представления графа метки.</span><span class="sxs-lookup"><span data-stu-id="0a4b3-107">Retrieves or sets a value that determines if the horizontal (X) axis of the graph view contains labels.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4b3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a4b3-108">Syntax</span></span>


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a><span data-ttu-id="0a4b3-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0a4b3-109">Property value</span></span>

<span data-ttu-id="0a4b3-110">Значение true будет применять метки к оси x.</span><span class="sxs-lookup"><span data-stu-id="0a4b3-110">A value of True will apply labels to the x-axis.</span></span> <span data-ttu-id="0a4b3-111">Значение false не будет.</span><span class="sxs-lookup"><span data-stu-id="0a4b3-111">A value of False will not.</span></span> <span data-ttu-id="0a4b3-112">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="0a4b3-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a4b3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a4b3-113">Remarks</span></span>

<span data-ttu-id="0a4b3-114">СИСМОН игнорирует это свойство для линейчатых диаграмм, отчетов и гистограмм.</span><span class="sxs-lookup"><span data-stu-id="0a4b3-114">SYSMON ignores this property for bar graphs, reports and histograms.</span></span>

<span data-ttu-id="0a4b3-115">Для линейных графов СИСМОН использует время выборки значения счетчика в качестве метки.</span><span class="sxs-lookup"><span data-stu-id="0a4b3-115">For line graphs, SYSMON uses the time that the counter value was sampled as the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4b3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0a4b3-116">Requirements</span></span>



| <span data-ttu-id="0a4b3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0a4b3-117">Requirement</span></span> | <span data-ttu-id="0a4b3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0a4b3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4b3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a4b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4b3-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a4b3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a4b3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a4b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4b3-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a4b3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a4b3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0a4b3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a4b3-124"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="0a4b3-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





