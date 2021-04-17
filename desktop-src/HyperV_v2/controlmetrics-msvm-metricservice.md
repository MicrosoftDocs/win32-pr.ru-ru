---
description: Используется для управления сбором метрик для управляемого элемента или элементов.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Метод Контролметрикс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663744"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="cd0c3-103">Метод Контролметрикс \_ класса Метриксервице мсвм</span><span class="sxs-lookup"><span data-stu-id="cd0c3-103">ControlMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="cd0c3-104">Используется для управления сбором метрик для управляемого элемента или элементов.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-104">Used to control the collection of metrics for a managed element or elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd0c3-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cd0c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd0c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd0c3-107">*Тема* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd0c3-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0c3-108">Экземпляр [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , определяющий управляемые элементы, для которых будут собираться метрики.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-108">A [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) instance that identifies the managed elements for which metrics will be collected.</span></span> <span data-ttu-id="cd0c3-109">Если этот параметр имеет **значение NULL**, будут собираться метрики для всех управляемых элементов, связанных с параметром *определения* .</span><span class="sxs-lookup"><span data-stu-id="cd0c3-109">If this parameter is **Null**, the metrics for all the managed elements associated with the *Definition* parameter will be collected.</span></span>

</dd> <dt>

<span data-ttu-id="cd0c3-110">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd0c3-110">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0c3-111">Экземпляр [**\_ басеметрикдефинитион мсвм**](msvm-basemetricdefinition.md) , указывающий метрики, которые будут собраны.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-111">An [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance that specifies which metrics will be collected.</span></span> <span data-ttu-id="cd0c3-112">Если этот параметр имеет **значение NULL**, будут собираться метрики для всех определений, связанных с управляемым элементом, идентифицируемым параметром *subject* .</span><span class="sxs-lookup"><span data-stu-id="cd0c3-112">If this parameter is **Null**, the metrics for all the definitions associated with the managed element identified by the *Subject* parameter will be collected</span></span>

</dd> <dt>

<span data-ttu-id="cd0c3-113">*Метрикколлектионенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd0c3-113">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0c3-114">Указывает операцию для выполнения в коллекции метрик.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-114">Specifies the operation to perform on the metrics collection.</span></span> <span data-ttu-id="cd0c3-115">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-115">This must be one of the following values.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="cd0c3-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Включить** (2)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cd0c3-117">Включите сбор метрик.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-117">Enable metrics collection.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="cd0c3-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** (3)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cd0c3-119">Отключение сбора метрик.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-119">Disable metrics collection.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="cd0c3-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (4)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cd0c3-121">Сбросьте значения метрик.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-121">Reset metrics values.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cd0c3-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cd0c3-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="cd0c3-124"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cd0c3-124"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="cd0c3-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd0c3-125">Return value</span></span>

<span data-ttu-id="cd0c3-126">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cd0c3-127">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd0c3-128">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd0c3-129">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd0c3-130">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-130">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd0c3-131">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="cd0c3-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cd0c3-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd0c3-132">Remarks</span></span>

<span data-ttu-id="cd0c3-133">Этот метод завершится со сбоем в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="cd0c3-133">This method will fail in the following instances:</span></span>

-   <span data-ttu-id="cd0c3-134">Параметры *subject* и *definition* равны **null**.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-134">The *Subject* and *Definition* parameters are both **Null**.</span></span>
-   <span data-ttu-id="cd0c3-135">Параметры *subject* и *definition* не равны **null** и не имеют экземпляра [**мсвм \_ метрикдефформе**](msvm-metricdefforme.md) , связывающего два экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cd0c3-135">The *Subject* and *Definition* parameters are both non-**Null** and there is not an instance of [**Msvm\_MetricDefForME**](msvm-metricdefforme.md) that associates the two instances.</span></span>
-   <span data-ttu-id="cd0c3-136">Параметр *определения* является ссылкой на экземпляр [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md) , который не связан с [**мсвм \_ метриксервице**](msvm-metricservice.md) до [**мсвм \_ сервицеаффектселемент**](msvm-serviceaffectselement.md).</span><span class="sxs-lookup"><span data-stu-id="cd0c3-136">The *Definition* parameter is a reference to an instance of [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) that is not associated with the [**Msvm\_MetricService**](msvm-metricservice.md) through [**Msvm\_ServiceAffectsElement**](msvm-serviceaffectselement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd0c3-137">Требования</span><span class="sxs-lookup"><span data-stu-id="cd0c3-137">Requirements</span></span>



| <span data-ttu-id="cd0c3-138">Требование</span><span class="sxs-lookup"><span data-stu-id="cd0c3-138">Requirement</span></span> | <span data-ttu-id="cd0c3-139">Значение</span><span class="sxs-lookup"><span data-stu-id="cd0c3-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0c3-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd0c3-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cd0c3-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cd0c3-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd0c3-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd0c3-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cd0c3-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cd0c3-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd0c3-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cd0c3-144">Namespace</span></span><br/>                | <span data-ttu-id="cd0c3-145">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cd0c3-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd0c3-146">MOF</span><span class="sxs-lookup"><span data-stu-id="cd0c3-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd0c3-147"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd0c3-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd0c3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="cd0c3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd0c3-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd0c3-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd0c3-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd0c3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0c3-151">**Мсвм \_ метриксервице**</span><span class="sxs-lookup"><span data-stu-id="cd0c3-151">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

