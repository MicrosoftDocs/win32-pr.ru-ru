---
title: Системмонитор. Минимумскале, свойство
description: Возвращает или задает минимальное значение вертикальной оси (Y) диаграммы.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Сисмон свойство Минимумскале
- Минимумскале Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Минимумскале
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490467"
---
# <a name="systemmonitorminimumscale-property"></a><span data-ttu-id="5598f-106">Системмонитор. Минимумскале, свойство</span><span class="sxs-lookup"><span data-stu-id="5598f-106">SystemMonitor.MinimumScale property</span></span>

<span data-ttu-id="5598f-107">Возвращает или задает минимальное значение вертикальной оси (Y) диаграммы.</span><span class="sxs-lookup"><span data-stu-id="5598f-107">Retrieves or sets the minimum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="5598f-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5598f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5598f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5598f-109">Syntax</span></span>


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="5598f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5598f-110">Property value</span></span>

<span data-ttu-id="5598f-111">Положительное минимальное значение вертикальной оси графа.</span><span class="sxs-lookup"><span data-stu-id="5598f-111">Positive minimum value of the vertical axis of the graph.</span></span> <span data-ttu-id="5598f-112">По умолчанию минимальное значение вертикального масштаба равно 0.</span><span class="sxs-lookup"><span data-stu-id="5598f-112">The default minimum value of the vertical scale is 0.</span></span> <span data-ttu-id="5598f-113">Наибольшее значение, которое можно установить как минимальное значение, равное значению меньше [**максимумскале**](systemmonitor-maximumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="5598f-113">The highest value that you can set the minimum value to is one less than [**MaximumScale**](systemmonitor-maximumscale.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5598f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5598f-114">Remarks</span></span>

<span data-ttu-id="5598f-115">Элемент управления автоматически корректирует расположение чисел шкалы, отображаемых на вертикальном масштабировании, в соответствии с размером отображаемого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5598f-115">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5598f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5598f-116">Requirements</span></span>



| <span data-ttu-id="5598f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5598f-117">Requirement</span></span> | <span data-ttu-id="5598f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5598f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5598f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5598f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5598f-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5598f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5598f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5598f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5598f-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5598f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5598f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5598f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5598f-124"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5598f-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5598f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5598f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5598f-126">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="5598f-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="5598f-127">**Системмонитор. Максимумскале**</span><span class="sxs-lookup"><span data-stu-id="5598f-127">**SystemMonitor.MaximumScale**</span></span>](systemmonitor-maximumscale.md)
</dt> <dt>

[<span data-ttu-id="5598f-128">**Системмонитор. Шовскалелабелс**</span><span class="sxs-lookup"><span data-stu-id="5598f-128">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





