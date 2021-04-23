---
title: Системмонитор. Енаблетултипс, свойство
description: Возвращает или задает значение, определяющее, отображается ли всплывающая подсказка при наведении указателя мыши на счетчик в одном из представлений графа (не поддерживается для представления отчета).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Сисмон свойство Енаблетултипс
- Свойство Енаблетултипс Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, свойство Енаблетултипс
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661910"
---
# <a name="systemmonitorenabletooltips-property"></a><span data-ttu-id="fa3fe-106">Системмонитор. Енаблетултипс, свойство</span><span class="sxs-lookup"><span data-stu-id="fa3fe-106">SystemMonitor.EnableToolTips property</span></span>

<span data-ttu-id="fa3fe-107">Возвращает или задает значение, определяющее, отображается ли всплывающая подсказка при наведении указателя мыши на счетчик в одном из представлений графа (не поддерживается для представления отчета).</span><span class="sxs-lookup"><span data-stu-id="fa3fe-107">Retrieves or sets a value that determines if a tool tip is shown when the mouse hovers over a counter in one of the graph views (not supported for report view).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa3fe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa3fe-108">Syntax</span></span>


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a><span data-ttu-id="fa3fe-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fa3fe-109">Property value</span></span>

<span data-ttu-id="fa3fe-110">Значение true показывает всплывающую подсказку со сведениями о счетчике; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-110">True displays a tool tip with the counter information in it; otherwise, False.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa3fe-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa3fe-111">Remarks</span></span>

<span data-ttu-id="fa3fe-112">Для линейных графиков подсказка привязана к точке данных, расположенной ближе всего к мыши.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-112">For line graphs, the tool tip is anchored to the data point that is closest to the mouse.</span></span> <span data-ttu-id="fa3fe-113">Для линейчатых диаграмм и гистограмм подсказка представляет общее значение данных линейки, а не точку внутри линии.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-113">For bar charts and histograms, the tool tip represents the total data value of the bar, not a point within the bar.</span></span>

<span data-ttu-id="fa3fe-114">Всплывающая подсказка содержит различные сведения, основанные на источнике данных.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-114">The tool tip contains different information based upon the data source.</span></span> <span data-ttu-id="fa3fe-115">Для файлов журнала подсказка содержит путь к счетчику, значение счетчика, отметку времени, количество выборок данных, включаемых в точку данных, и минимальное и максимальное значения данных.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-115">For log files, the tool tip contains the counter path, counter value, time stamp, number of data samples included in the data point, and the minimum and maximum data values.</span></span>

<span data-ttu-id="fa3fe-116">Для действий в реальном времени подсказка содержит путь к счетчику, значение счетчика и отметку времени.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-116">For real time activity, the tool tip contains the counter path, counter value, and time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa3fe-117">Требования</span><span class="sxs-lookup"><span data-stu-id="fa3fe-117">Requirements</span></span>



| <span data-ttu-id="fa3fe-118">Требование</span><span class="sxs-lookup"><span data-stu-id="fa3fe-118">Requirement</span></span> | <span data-ttu-id="fa3fe-119">Значение</span><span class="sxs-lookup"><span data-stu-id="fa3fe-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3fe-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa3fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa3fe-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa3fe-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa3fe-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa3fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa3fe-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa3fe-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa3fe-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fa3fe-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa3fe-125"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="fa3fe-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





