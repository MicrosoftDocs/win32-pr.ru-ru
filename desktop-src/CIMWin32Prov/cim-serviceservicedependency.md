---
description: Класс CIM \_ сервицесервицедепенденци представляет ассоциацию между двумя службами.
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: Класс CIM_ServiceServiceDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655824"
---
# <a name="cim_serviceservicedependency-class"></a><span data-ttu-id="6753f-103">\_Класс CIM сервицесервицедепенденци</span><span class="sxs-lookup"><span data-stu-id="6753f-103">CIM\_ServiceServiceDependency class</span></span>

<span data-ttu-id="6753f-104">Класс **CIM \_ сервицесервицедепенденци** представляет ассоциацию между двумя службами.</span><span class="sxs-lookup"><span data-stu-id="6753f-104">The **CIM\_ServiceServiceDependency** class represents an association between two services.</span></span> <span data-ttu-id="6753f-105">Связанная служба должна быть установлена, должна быть завершена или должна отсутствовать для функционирования другой службы.</span><span class="sxs-lookup"><span data-stu-id="6753f-105">The associated service must be present, must have completed, or must be absent for the other service to function.</span></span> <span data-ttu-id="6753f-106">Например, службы загрузки могут зависеть от базовых служб BIOS, диска и инициализации.</span><span class="sxs-lookup"><span data-stu-id="6753f-106">For example, boot services can be dependent on underlying BIOS, disk, and initialization services.</span></span> <span data-ttu-id="6753f-107">Для служб инициализации служба загрузки зависит от завершения служб инициализации.</span><span class="sxs-lookup"><span data-stu-id="6753f-107">For initialization services, the boot service is dependent on the initialization services completing.</span></span> <span data-ttu-id="6753f-108">Для дисковых служб службы загрузки могут фактически использовать SAPs этой службы.</span><span class="sxs-lookup"><span data-stu-id="6753f-108">For disk services, boot services can actually use the SAPs of this service.</span></span> <span data-ttu-id="6753f-109">Эта зависимость использования моделируется на ассоциации [**CIM \_ сервицесапдепенденци**](cim-servicesapdependency.md) .</span><span class="sxs-lookup"><span data-stu-id="6753f-109">This usage dependency is modeled on the [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6753f-110">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6753f-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6753f-111">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6753f-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6753f-112">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6753f-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6753f-113">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6753f-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6753f-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6753f-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="6753f-115">Члены</span><span class="sxs-lookup"><span data-stu-id="6753f-115">Members</span></span>

<span data-ttu-id="6753f-116">Класс **CIM \_ сервицесервицедепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6753f-116">The **CIM\_ServiceServiceDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="6753f-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="6753f-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6753f-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="6753f-118">Properties</span></span>

<span data-ttu-id="6753f-119">Класс **CIM \_ сервицесервицедепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6753f-119">The **CIM\_ServiceServiceDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6753f-120">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="6753f-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6753f-121">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="6753f-121">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="6753f-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6753f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6753f-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6753f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6753f-124">[**\_ Служба CIM**](cim-service.md) , которая описывает необходимую службу.</span><span class="sxs-lookup"><span data-stu-id="6753f-124">A [**CIM\_Service**](cim-service.md) that describes the required service.</span></span>

</dd> <dt>

<span data-ttu-id="6753f-125">**Него**</span><span class="sxs-lookup"><span data-stu-id="6753f-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6753f-126">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="6753f-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="6753f-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6753f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6753f-128">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="6753f-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6753f-129">[**\_ Служба CIM**](cim-service.md) , которая описывает службу, зависящую от базовой службы.</span><span class="sxs-lookup"><span data-stu-id="6753f-129">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying service.</span></span>

</dd> <dt>

<span data-ttu-id="6753f-130">**типеофдепенденци**</span><span class="sxs-lookup"><span data-stu-id="6753f-130">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6753f-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6753f-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6753f-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6753f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6753f-133">Природа зависимости между службами.</span><span class="sxs-lookup"><span data-stu-id="6753f-133">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="6753f-134">Это свойство указывает, что связанная служба должна быть завершена, должна быть запущена или не должна запускаться для функционирования службы.</span><span class="sxs-lookup"><span data-stu-id="6753f-134">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6753f-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6753f-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6753f-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6753f-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="6753f-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Служба должна быть завершена** (2)</span><span class="sxs-lookup"><span data-stu-id="6753f-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6753f-138">Служба должна быть завершена.</span><span class="sxs-lookup"><span data-stu-id="6753f-138">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="6753f-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Служба должна быть запущена** (3)</span><span class="sxs-lookup"><span data-stu-id="6753f-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6753f-140">Служба должна быть запущена.</span><span class="sxs-lookup"><span data-stu-id="6753f-140">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="6753f-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Служба не должна запускаться** (4)</span><span class="sxs-lookup"><span data-stu-id="6753f-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6753f-142">Служба не должна быть запущена.</span><span class="sxs-lookup"><span data-stu-id="6753f-142">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6753f-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6753f-143">Remarks</span></span>

<span data-ttu-id="6753f-144">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6753f-144">WMI does not implement this class.</span></span> <span data-ttu-id="6753f-145">Классы WMI, производные от **CIM \_ сервицесервицедепенденци**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6753f-145">For WMI classes derived from **CIM\_ServiceServiceDependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6753f-146">Класс **CIM \_ сервицесервицедепенденци** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="6753f-146">The **CIM\_ServiceServiceDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="6753f-147">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6753f-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6753f-148">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6753f-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6753f-149">Требования</span><span class="sxs-lookup"><span data-stu-id="6753f-149">Requirements</span></span>



| <span data-ttu-id="6753f-150">Требование</span><span class="sxs-lookup"><span data-stu-id="6753f-150">Requirement</span></span> | <span data-ttu-id="6753f-151">Значение</span><span class="sxs-lookup"><span data-stu-id="6753f-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6753f-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6753f-152">Minimum supported client</span></span><br/> | <span data-ttu-id="6753f-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6753f-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6753f-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6753f-154">Minimum supported server</span></span><br/> | <span data-ttu-id="6753f-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6753f-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6753f-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6753f-156">Namespace</span></span><br/>                | <span data-ttu-id="6753f-157">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6753f-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6753f-158">MOF</span><span class="sxs-lookup"><span data-stu-id="6753f-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6753f-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6753f-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6753f-160">DLL</span><span class="sxs-lookup"><span data-stu-id="6753f-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6753f-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6753f-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6753f-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6753f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6753f-163">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="6753f-163">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

