---
title: Системмонитор. Дисплайтипе, свойство
description: Возвращает или задает тип графа, используемый для отображения данных счетчика производительности.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Сисмон свойство Дисплайтипе
- Дисплайтипе Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Дисплайтипе
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136002"
---
# <a name="systemmonitordisplaytype-property"></a><span data-ttu-id="cc359-106">Системмонитор. Дисплайтипе, свойство</span><span class="sxs-lookup"><span data-stu-id="cc359-106">SystemMonitor.DisplayType property</span></span>

<span data-ttu-id="cc359-107">Возвращает или задает тип графа, используемый для отображения данных счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="cc359-107">Retrieves or sets the type of graph used to graph the performance counter data.</span></span>

<span data-ttu-id="cc359-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cc359-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc359-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc359-109">Syntax</span></span>


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="cc359-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cc359-110">Property value</span></span>

<span data-ttu-id="cc359-111">Тип графа, используемый для отображения данных счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="cc359-111">Type of graph used to graph the performance counter data.</span></span> <span data-ttu-id="cc359-112">Возможные значения см. в разделе [**дисплайтипеконстантс**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="cc359-112">For possible values, see [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="cc359-113">Исключения</span><span class="sxs-lookup"><span data-stu-id="cc359-113">Exceptions</span></span>



| <span data-ttu-id="cc359-114">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="cc359-114">Exception type</span></span>               | <span data-ttu-id="cc359-115">Условие</span><span class="sxs-lookup"><span data-stu-id="cc359-115">Condition</span></span>                                         |
|------------------------------|---------------------------------------------------|
| <span data-ttu-id="cc359-116">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="cc359-116">**System.ArgumentException**</span></span> | <span data-ttu-id="cc359-117">Указано недопустимое значение диаграммы или отчета.</span><span class="sxs-lookup"><span data-stu-id="cc359-117">The specified graph or report value is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="cc359-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cc359-118">Requirements</span></span>



| <span data-ttu-id="cc359-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cc359-119">Requirement</span></span> | <span data-ttu-id="cc359-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cc359-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc359-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc359-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc359-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc359-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cc359-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc359-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc359-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc359-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc359-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cc359-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc359-126"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cc359-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc359-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc359-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc359-128">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="cc359-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





