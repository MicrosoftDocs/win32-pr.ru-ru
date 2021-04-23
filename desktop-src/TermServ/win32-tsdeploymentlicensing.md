---
title: Класс Win32_TSDeploymentLicensing
description: Параметры лицензирования для развертывания удаленный рабочий стол Virtualization (RDV).
ms.assetid: 78e95629-6580-4aa1-bcbd-a79af44ddb54
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSDeploymentLicensing службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSDeploymentLicensing, описание
topic_type:
- apiref
api_name:
- Win32_TSDeploymentLicensing
- Win32_TSDeploymentLicensing.Caption
- Win32_TSDeploymentLicensing.Description
- Win32_TSDeploymentLicensing.InstallDate
- Win32_TSDeploymentLicensing.Name
- Win32_TSDeploymentLicensing.Status
- Win32_TSDeploymentLicensing.UseCentralLicensingSettings
- Win32_TSDeploymentLicensing.LicenseServers
- Win32_TSDeploymentLicensing.LicensingType
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 952f58daa8a809e158265aac71b0094c0cd46fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672824"
---
# <a name="win32_tsdeploymentlicensing-class"></a><span data-ttu-id="0ecab-105">\_Класс Win32 тсдеплойментлиценсинг</span><span class="sxs-lookup"><span data-stu-id="0ecab-105">Win32\_TSDeploymentLicensing class</span></span>

<span data-ttu-id="0ecab-106">Параметры лицензирования для развертывания удаленный рабочий стол Virtualization (RDV).</span><span class="sxs-lookup"><span data-stu-id="0ecab-106">Licensing Settings for the Remote Desktop Virtualization (RDV) deployment.</span></span>

<span data-ttu-id="0ecab-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0ecab-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ecab-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ecab-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentLicensing : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  UseCentralLicensingSettings;
  String   LicenseServers[];
  uint32   LicensingType;
};
```

## <a name="members"></a><span data-ttu-id="0ecab-109">Члены</span><span class="sxs-lookup"><span data-stu-id="0ecab-109">Members</span></span>

<span data-ttu-id="0ecab-110">Класс **Win32 \_ тсдеплойментлиценсинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0ecab-110">The **Win32\_TSDeploymentLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="0ecab-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ecab-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ecab-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ecab-112">Properties</span></span>

<span data-ttu-id="0ecab-113">Класс **Win32 \_ тсдеплойментлиценсинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0ecab-113">The **Win32\_TSDeploymentLicensing** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ecab-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0ecab-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ecab-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ecab-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ecab-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0ecab-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0ecab-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="0ecab-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0ecab-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ecab-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ecab-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0ecab-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ecab-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ecab-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ecab-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ecab-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0ecab-123">Description of the object.</span></span>

<span data-ttu-id="0ecab-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ecab-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ecab-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0ecab-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ecab-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0ecab-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ecab-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="0ecab-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0ecab-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="0ecab-129">The date the object was installed.</span></span> <span data-ttu-id="0ecab-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="0ecab-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0ecab-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ecab-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ecab-132">**лиценсесерверс**</span><span class="sxs-lookup"><span data-stu-id="0ecab-132">**LicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ecab-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0ecab-133">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0ecab-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0ecab-135">Указывает используемые серверы лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0ecab-135">Specifies the license servers to use.</span></span>

</dd> <dt>

<span data-ttu-id="0ecab-136">**лиценсингтипе**</span><span class="sxs-lookup"><span data-stu-id="0ecab-136">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ecab-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ecab-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0ecab-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0ecab-139">Режим лицензирования</span><span class="sxs-lookup"><span data-stu-id="0ecab-139">Licensing Mode</span></span>

<dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="0ecab-140">**На устройство** (2)</span><span class="sxs-lookup"><span data-stu-id="0ecab-140">**Per Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="0ecab-141">**На пользователя** (4)</span><span class="sxs-lookup"><span data-stu-id="0ecab-141">**Per User** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Yet_Configured"></span><span id="not_yet_configured"></span><span id="NOT_YET_CONFIGURED"></span>

<span data-ttu-id="0ecab-142">**Еще не настроено** (5)</span><span class="sxs-lookup"><span data-stu-id="0ecab-142">**Not Yet Configured** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ecab-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="0ecab-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ecab-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ecab-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ecab-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ecab-146">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0ecab-146">The name of the object.</span></span>

<span data-ttu-id="0ecab-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ecab-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ecab-148">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0ecab-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ecab-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ecab-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ecab-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-151">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0ecab-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0ecab-152">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0ecab-152">Current status of the object.</span></span> <span data-ttu-id="0ecab-153">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="0ecab-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0ecab-154">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="0ecab-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0ecab-155">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="0ecab-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0ecab-156">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="0ecab-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0ecab-157">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="0ecab-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0ecab-158">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ecab-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0ecab-159">("ОК")</span><span class="sxs-lookup"><span data-stu-id="0ecab-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ecab-160">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="0ecab-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ecab-161">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="0ecab-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ecab-162">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0ecab-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ecab-163">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="0ecab-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ecab-164">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="0ecab-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ecab-165">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="0ecab-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ecab-166">("Служба")</span><span class="sxs-lookup"><span data-stu-id="0ecab-166">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ecab-167">**усецентраллиценсингсеттингс**</span><span class="sxs-lookup"><span data-stu-id="0ecab-167">**UseCentralLicensingSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ecab-168">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0ecab-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ecab-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0ecab-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0ecab-170">Указывает, следует ли использовать параметры лицензирования на уровне развертывания.</span><span class="sxs-lookup"><span data-stu-id="0ecab-170">Specifies whether to use deployment-wide licensing settings.</span></span> <span data-ttu-id="0ecab-171">**Значение true** , чтобы использовать эти параметры для всех серверов в этом развертывании.</span><span class="sxs-lookup"><span data-stu-id="0ecab-171">**True** to use these settings for all servers in this deployment.</span></span> <span data-ttu-id="0ecab-172">**значение false** , чтобы задать их для каждого сервера.</span><span class="sxs-lookup"><span data-stu-id="0ecab-172">**false** to set them per-server.</span></span> <span data-ttu-id="0ecab-173">Если задано значение **false**, все остальные параметры лицензирования игнорируются.</span><span class="sxs-lookup"><span data-stu-id="0ecab-173">If this is set to **false**, all other licensing settings are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ecab-174">Требования</span><span class="sxs-lookup"><span data-stu-id="0ecab-174">Requirements</span></span>



| <span data-ttu-id="0ecab-175">Требование</span><span class="sxs-lookup"><span data-stu-id="0ecab-175">Requirement</span></span> | <span data-ttu-id="0ecab-176">Значение</span><span class="sxs-lookup"><span data-stu-id="0ecab-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ecab-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ecab-177">Minimum supported client</span></span><br/> | <span data-ttu-id="0ecab-178">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0ecab-178">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0ecab-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ecab-179">Minimum supported server</span></span><br/> | <span data-ttu-id="0ecab-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0ecab-180">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="0ecab-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0ecab-181">Namespace</span></span><br/>                | <span data-ttu-id="0ecab-182">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0ecab-182">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0ecab-183">MOF</span><span class="sxs-lookup"><span data-stu-id="0ecab-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ecab-184"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ecab-184"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="0ecab-185">DLL</span><span class="sxs-lookup"><span data-stu-id="0ecab-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ecab-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ecab-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

