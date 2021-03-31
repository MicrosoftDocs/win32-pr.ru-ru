---
title: Системмонитор. Чартскролл, свойство
description: Возвращает или задает значение, определяющее, прокручивается ли линейный график в представлении.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Сисмон свойство Чартскролл
- Свойство Чартскролл Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, свойство Чартскролл
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988757"
---
# <a name="systemmonitorchartscroll-property"></a><span data-ttu-id="ea530-106">Системмонитор. Чартскролл, свойство</span><span class="sxs-lookup"><span data-stu-id="ea530-106">SystemMonitor.ChartScroll property</span></span>

<span data-ttu-id="ea530-107">Возвращает или задает значение, определяющее, прокручивается ли линейный график в представлении.</span><span class="sxs-lookup"><span data-stu-id="ea530-107">Retrieves or sets a value that determines if the line graph scrolls in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea530-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea530-108">Syntax</span></span>


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ea530-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ea530-109">Property value</span></span>

<span data-ttu-id="ea530-110">Значение true, если линейный график непрерывно прокручивается справа налево; в противном случае значение false, если линейный график рисуется слева направо и заключает себя в представление.</span><span class="sxs-lookup"><span data-stu-id="ea530-110">True if the line graph scrolls continuously from right to left; otherwise, False if the line graph is drawn from left to right and wraps around on itself in the view.</span></span> <span data-ttu-id="ea530-111">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="ea530-111">False is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea530-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea530-112">Remarks</span></span>

<span data-ttu-id="ea530-113">Это значение игнорируется, если [**системмонитор. дисплайтипе**](systemmonitor-displaytype.md) не [**DisplayTypeConstants.sysмонлинеграф**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="ea530-113">This value is ignored if the [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea530-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ea530-114">Requirements</span></span>



| <span data-ttu-id="ea530-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ea530-115">Requirement</span></span> | <span data-ttu-id="ea530-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ea530-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea530-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea530-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ea530-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea530-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea530-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea530-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ea530-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea530-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea530-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ea530-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea530-122"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ea530-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





