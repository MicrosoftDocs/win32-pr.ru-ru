---
title: Системмонитор. Репортвалуетипе, свойство
description: Возвращает или задает значение, определяющее, отображает ли гистограмма и представления отчетов Последнее значение, заданное в интервале выборки, или вычисленное значение из выборки, например среднее или минимальное значение счетчика.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Сисмон свойство Репортвалуетипе
- Репортвалуетипе Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Репортвалуетипе
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988613"
---
# <a name="systemmonitorreportvaluetype-property"></a><span data-ttu-id="0cbc0-106">Системмонитор. Репортвалуетипе, свойство</span><span class="sxs-lookup"><span data-stu-id="0cbc0-106">SystemMonitor.ReportValueType property</span></span>

<span data-ttu-id="0cbc0-107">Возвращает или задает значение, определяющее, отображает ли гистограмма и представления отчетов Последнее значение, заданное в интервале выборки, или вычисленное значение из выборки, например среднее или минимальное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-107">Retrieves or sets a value that determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling, such as the average or minimum counter value.</span></span>

<span data-ttu-id="0cbc0-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cbc0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cbc0-109">Syntax</span></span>


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="0cbc0-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0cbc0-110">Property value</span></span>

<span data-ttu-id="0cbc0-111">Определяет, отображает ли гистограмма и представления отчетов Последнее значение, выборка которого производилось в интервале выборки, или вычисленное значение из интервала выборки.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-111">Determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling interval.</span></span> <span data-ttu-id="0cbc0-112">Возможные значения см. в разделе [**репортвалуетипеконстантс**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="0cbc0-112">For possible values, see [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span></span>

## <a name="remarks"></a><span data-ttu-id="0cbc0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0cbc0-113">Remarks</span></span>

<span data-ttu-id="0cbc0-114">СИСМОН игнорирует это значение и использует [**ReportValueTypeConstants.sysмондефаултвалуе**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) , если [**системмонитор. Дисплайтипе**](systemmonitor-displaytype.md) не [**DisplayTypeConstants.sysмонхистограм**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) или **DisplayTypeConstants.sysмонрепорт**.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-114">SYSMON ignores this value and uses [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) if [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) or **DisplayTypeConstants.sysmonReport**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cbc0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0cbc0-115">Requirements</span></span>



| <span data-ttu-id="0cbc0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0cbc0-116">Requirement</span></span> | <span data-ttu-id="0cbc0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0cbc0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cbc0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0cbc0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0cbc0-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0cbc0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0cbc0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0cbc0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0cbc0-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0cbc0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cbc0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0cbc0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cbc0-123"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="0cbc0-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cbc0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0cbc0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbc0-125">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="0cbc0-125">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





