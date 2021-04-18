---
description: Предоставляет возможность возвращать отфильтрованный список \_ экземпляров CIM басеметриквалуе.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Метод Жетметриквалуес класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663474"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a><span data-ttu-id="2a315-103">Метод Жетметриквалуес \_ класса CIM метриксервице</span><span class="sxs-lookup"><span data-stu-id="2a315-103">GetMetricValues method of the CIM\_MetricService class</span></span>

<span data-ttu-id="2a315-104">Предоставляет возможность возвращать отфильтрованный список экземпляров [**CIM \_ басеметриквалуе**](cim-basemetricvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="2a315-104">Provides the ability to return a filtered list of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a315-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a315-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="2a315-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a315-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a315-107">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a315-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a315-108">Идентифицирует [**\_ басеметрикдефинитион CIM**](cim-basemetricdefinition.md) , для которого будут возвращены метрики.</span><span class="sxs-lookup"><span data-stu-id="2a315-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="2a315-109">*Диапазон значений* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a315-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a315-110">Определяет, как выбираются экземпляры.</span><span class="sxs-lookup"><span data-stu-id="2a315-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="2a315-111">Алгоритм упорядочивания экземпляров является специфическим для определения метрики.</span><span class="sxs-lookup"><span data-stu-id="2a315-111">The algorithm for ordering value instances is metric-definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="2a315-112">**Минимум** (2)</span><span class="sxs-lookup"><span data-stu-id="2a315-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="2a315-113">**Максимум** (3)</span><span class="sxs-lookup"><span data-stu-id="2a315-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2a315-114">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="2a315-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="2a315-115">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="2a315-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="2a315-116">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a315-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a315-117">Определяет максимальное число экземпляров, возвращаемых методом.</span><span class="sxs-lookup"><span data-stu-id="2a315-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="2a315-118">*Значения* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a315-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a315-119">После успешного завершения метода содержит ссылки на экземпляры [**CIM \_ басеметриквалуе**](cim-basemetricvalue.md), отфильтрованные в соответствии со значениями входных параметров.</span><span class="sxs-lookup"><span data-stu-id="2a315-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a315-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a315-120">Return value</span></span>

<span data-ttu-id="2a315-121">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2a315-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2a315-122">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="2a315-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2a315-123">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="2a315-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2a315-124">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="2a315-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a315-125">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="2a315-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2a315-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="2a315-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2a315-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2a315-127">Requirements</span></span>



| <span data-ttu-id="2a315-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2a315-128">Requirement</span></span> | <span data-ttu-id="2a315-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2a315-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a315-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a315-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2a315-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2a315-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2a315-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a315-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2a315-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2a315-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2a315-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2a315-134">Namespace</span></span><br/>                | <span data-ttu-id="2a315-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2a315-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2a315-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2a315-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a315-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a315-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a315-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2a315-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a315-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a315-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a315-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a315-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a315-141">**\_МЕТРИКСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="2a315-141">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




