---
title: Каунтеритем. Жетдатаат, метод
description: Извлекает указанное значение счетчика из определенной точки диаграммы.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Метод Жетдатаат Сисмон
- Метод Жетдатаат Сисмон, объект Каунтеритем
- Сисмон объекта Каунтеритем, метод Жетдатаат
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534307"
---
# <a name="counteritemgetdataat-method"></a><span data-ttu-id="2ebf4-106">Каунтеритем. Жетдатаат, метод</span><span class="sxs-lookup"><span data-stu-id="2ebf4-106">CounterItem.GetDataAt method</span></span>

<span data-ttu-id="2ebf4-107">Извлекает указанное значение счетчика из определенной точки диаграммы.</span><span class="sxs-lookup"><span data-stu-id="2ebf4-107">Retrieves the specified counter value from a specific point in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebf4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ebf4-108">Syntax</span></span>


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="2ebf4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ebf4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ebf4-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ebf4-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebf4-111">Отсчитываемый от нуля индекс точки графа, значение которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="2ebf4-111">Zero-based index of the graph point whose value you want to retrieve.</span></span> <span data-ttu-id="2ebf4-112">Допустимые значения находятся в диапазоне от 0 до ([**системмонитор. датапоинткаунт**](systemmonitor-datapointcount.md) -1).</span><span class="sxs-lookup"><span data-stu-id="2ebf4-112">Valid values range from 0 to ([**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md) - 1).</span></span>

</dd> <dt>

<span data-ttu-id="2ebf4-113">*который* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ebf4-113">*which* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebf4-114">Тип значения счетчика, которое необходимо получить, например среднее значение счетчика, отображаемое в окне графа.</span><span class="sxs-lookup"><span data-stu-id="2ebf4-114">Type of counter value to retrieve, for example, the average value of the counter as displayed in the graph window.</span></span> <span data-ttu-id="2ebf4-115">Возможные значения см. в разделе [**сисмондататипе**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span><span class="sxs-lookup"><span data-stu-id="2ebf4-115">For possible values, see [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span></span>

</dd> <dt>

<span data-ttu-id="2ebf4-116">*вариант* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ebf4-116">*variant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebf4-117">Полученное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="2ebf4-117">Counter value that was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ebf4-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ebf4-118">Return value</span></span>

<span data-ttu-id="2ebf4-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2ebf4-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ebf4-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ebf4-120">Remarks</span></span>

<span data-ttu-id="2ebf4-121">Этот метод следует использовать только в том случае, если</span><span class="sxs-lookup"><span data-stu-id="2ebf4-121">Use this method only if</span></span>

-   <span data-ttu-id="2ebf4-122">[**Системмонитор. дисплайтипе**](systemmonitor-displaytype.md) имеет значение сисмонлинеграф</span><span class="sxs-lookup"><span data-stu-id="2ebf4-122">[**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is set to sysmonLineGraph</span></span>
-   <span data-ttu-id="2ebf4-123">[**Системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) имеет значение Сисмонлогфилес или сисмонскллог</span><span class="sxs-lookup"><span data-stu-id="2ebf4-123">[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles or sysmonSqlLog</span></span>

## <a name="requirements"></a><span data-ttu-id="2ebf4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2ebf4-124">Requirements</span></span>



| <span data-ttu-id="2ebf4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2ebf4-125">Requirement</span></span> | <span data-ttu-id="2ebf4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2ebf4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebf4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ebf4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2ebf4-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ebf4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ebf4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ebf4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2ebf4-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2ebf4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ebf4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2ebf4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ebf4-132"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2ebf4-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ebf4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ebf4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebf4-134">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="2ebf4-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="2ebf4-135">**Каунтеритем. статистики**</span><span class="sxs-lookup"><span data-stu-id="2ebf4-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="2ebf4-136">**Каунтеритем. GetValue**</span><span class="sxs-lookup"><span data-stu-id="2ebf4-136">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





