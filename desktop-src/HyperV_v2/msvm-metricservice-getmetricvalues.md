---
description: Возвращает значения метрик.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Метод Жетметриквалуес класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664510"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="b89ea-103">Метод Жетметриквалуес \_ класса Метриксервице мсвм</span><span class="sxs-lookup"><span data-stu-id="b89ea-103">GetMetricValues method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="b89ea-104">Возвращает значения метрик.</span><span class="sxs-lookup"><span data-stu-id="b89ea-104">Gets metric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b89ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b89ea-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="b89ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b89ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b89ea-107">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b89ea-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b89ea-108">Идентифицирует [**\_ басеметрикдефинитион CIM**](cim-basemetricdefinition.md) , для которого будут возвращены метрики.</span><span class="sxs-lookup"><span data-stu-id="b89ea-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="b89ea-109">*Диапазон значений* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b89ea-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b89ea-110">Определяет, как выбираются экземпляры.</span><span class="sxs-lookup"><span data-stu-id="b89ea-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="b89ea-111">Алгоритм упорядочивания экземпляров является специфическим определением метрик.</span><span class="sxs-lookup"><span data-stu-id="b89ea-111">The algorithm for ordering value instances is metric definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="b89ea-112">**Минимум** (2)</span><span class="sxs-lookup"><span data-stu-id="b89ea-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="b89ea-113">**Максимум** (3)</span><span class="sxs-lookup"><span data-stu-id="b89ea-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b89ea-114">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="b89ea-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="b89ea-115">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="b89ea-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b89ea-116">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b89ea-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b89ea-117">Определяет максимальное число экземпляров, возвращаемых методом.</span><span class="sxs-lookup"><span data-stu-id="b89ea-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="b89ea-118">*Значения* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b89ea-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b89ea-119">После успешного завершения метода содержит ссылки на экземпляры [**CIM \_ басеметриквалуе**](cim-basemetricvalue.md), отфильтрованные в соответствии со значениями входных параметров.</span><span class="sxs-lookup"><span data-stu-id="b89ea-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b89ea-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b89ea-120">Return value</span></span>

<span data-ttu-id="b89ea-121">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b89ea-121">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b89ea-122">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="b89ea-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b89ea-123">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b89ea-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b89ea-124">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="b89ea-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b89ea-125">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="b89ea-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b89ea-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="b89ea-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b89ea-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b89ea-127">Requirements</span></span>



| <span data-ttu-id="b89ea-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b89ea-128">Requirement</span></span> | <span data-ttu-id="b89ea-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b89ea-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b89ea-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b89ea-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b89ea-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b89ea-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b89ea-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b89ea-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b89ea-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b89ea-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b89ea-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b89ea-134">Namespace</span></span><br/>                | <span data-ttu-id="b89ea-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b89ea-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b89ea-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b89ea-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b89ea-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b89ea-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b89ea-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b89ea-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b89ea-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b89ea-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b89ea-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b89ea-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89ea-141">**Мсвм \_ метриксервице**</span><span class="sxs-lookup"><span data-stu-id="b89ea-141">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




