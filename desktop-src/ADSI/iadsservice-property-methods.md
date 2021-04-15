---
title: Методы свойств Иадссервице (iAds. h)
description: Чтение и запись свойств, описанных в этом разделе.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадссервице ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654483"
---
# <a name="iadsservice-property-methods"></a><span data-ttu-id="daf30-104">Методы свойств Иадссервице</span><span class="sxs-lookup"><span data-stu-id="daf30-104">IADsService Property Methods</span></span>

<span data-ttu-id="daf30-105">Методы свойств интерфейса [**иадссервице**](/windows/desktop/api/Iads/nn-iads-iadsservice) считывают и записывают свойства, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="daf30-105">The property methods of the [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="daf30-106">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="daf30-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="daf30-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="daf30-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="daf30-108">**Зависимости**</span><span class="sxs-lookup"><span data-stu-id="daf30-108">**Dependencies**</span></span>
<span data-ttu-id="daf30-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-110">Массив имен **BSTR** служб или групп загрузки, которые должны быть загружены для загрузки этой службы.</span><span class="sxs-lookup"><span data-stu-id="daf30-110">Array of **BSTR** names of services or load groups that must be loaded for this service to load.</span></span> <span data-ttu-id="daf30-111">Для записи используется синтаксис "Service:", за которым следует имя службы или Группа:, за которыми следует имя группы загрузки.</span><span class="sxs-lookup"><span data-stu-id="daf30-111">The syntax for the entry is "Service:" followed by the service name or "Group:" followed by the load group name.</span></span>

<dt>

<span data-ttu-id="daf30-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-113">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="daf30-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-114">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="daf30-114">**DisplayName**</span></span>
<span data-ttu-id="daf30-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-116">Понятное имя службы.</span><span class="sxs-lookup"><span data-stu-id="daf30-116">The friendly name of the service.</span></span>

<dt>

<span data-ttu-id="daf30-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="daf30-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-119">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="daf30-119">**ErrorControl**</span></span>
<span data-ttu-id="daf30-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-121">Действие, выполняемое в случае сбоя службы при запуске.</span><span class="sxs-lookup"><span data-stu-id="daf30-121">The action to be performed if this service fails on startup.</span></span> <span data-ttu-id="daf30-122">Ниже приведены допустимые значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="daf30-122">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="daf30-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\_Ошибка службы ADS — \_ \_ пропуск \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_IGNORE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-124">Программа запуска регистрирует ошибку, но возобновляет операцию запуска.</span><span class="sxs-lookup"><span data-stu-id="daf30-124">The startup program logs the error, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="daf30-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\_ \_ обычная ошибка службы ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_NORMAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-126">Программа запуска записывает в журнал ошибку и отображает окно сообщения, но возобновляет операцию запуска.</span><span class="sxs-lookup"><span data-stu-id="daf30-126">The startup program logs the error and presents a message box, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="daf30-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_Ошибка службы ADS, \_ \_ серьезная \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_SEVERE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-128">Программа запуска регистрирует ошибку.</span><span class="sxs-lookup"><span data-stu-id="daf30-128">The startup program logs the error.</span></span> <span data-ttu-id="daf30-129">При запуске последней удачной конфигурации операция запуска продолжится.</span><span class="sxs-lookup"><span data-stu-id="daf30-129">If the last-known-good configuration is started, the startup operation continues.</span></span> <span data-ttu-id="daf30-130">В противном случае система перезапускается с использованием последней удачной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="daf30-130">Otherwise, the system is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="daf30-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_ \_ критическая ошибка службы ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_CRITICAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-132">Если возможно, программа запуска зарегистрирует ошибку.</span><span class="sxs-lookup"><span data-stu-id="daf30-132">The startup program logs the error, if possible.</span></span> <span data-ttu-id="daf30-133">При запуске последней удачной конфигурации операция запуска завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="daf30-133">If the last-known-good configuration is being started, the startup operation fails.</span></span> <span data-ttu-id="daf30-134">В противном случае система перезапускается с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="daf30-134">Otherwise, the system is restarted with the last-known good configuration.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="daf30-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-136">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="daf30-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-137">**хосткомпутер**</span><span class="sxs-lookup"><span data-stu-id="daf30-137">**HostComputer**</span></span>
<span data-ttu-id="daf30-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-139">Строка ADsPath узла службы.</span><span class="sxs-lookup"><span data-stu-id="daf30-139">The ADsPath string of the host of this service.</span></span>

<dt>

<span data-ttu-id="daf30-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-141">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="daf30-141">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-142">**LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="daf30-142">**LoadOrderGroup**</span></span>
<span data-ttu-id="daf30-143"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-143"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-144">Имя группы порядка загрузки, членом которой является эта служба.</span><span class="sxs-lookup"><span data-stu-id="daf30-144">Name of the load order group that this service is a member.</span></span>

<dt>

<span data-ttu-id="daf30-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-146">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="daf30-146">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-147">**Путь**</span><span class="sxs-lookup"><span data-stu-id="daf30-147">**Path**</span></span>
<span data-ttu-id="daf30-148"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-148"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-149">Путь и имя файла для исполняемого файла этой службы.</span><span class="sxs-lookup"><span data-stu-id="daf30-149">Path and filename to the executable of this service.</span></span>

<dt>

<span data-ttu-id="daf30-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-151">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="daf30-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-152">**ServiceAccountName**</span><span class="sxs-lookup"><span data-stu-id="daf30-152">**ServiceAccountName**</span></span>
<span data-ttu-id="daf30-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-154">Имя учетной записи, используемой этой службой для проверки подлинности при запуске.</span><span class="sxs-lookup"><span data-stu-id="daf30-154">Name of the account that this service uses to authenticate itself on startup.</span></span>

<dt>

<span data-ttu-id="daf30-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-156">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="daf30-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-157">**сервицеаккаунтпас**</span><span class="sxs-lookup"><span data-stu-id="daf30-157">**ServiceAccountPath**</span></span>
<span data-ttu-id="daf30-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-159">Путь к учетной записи, указанной свойством **сервицеаккаунтпас** .</span><span class="sxs-lookup"><span data-stu-id="daf30-159">Path of the account specified by the **ServiceAccountPath** property.</span></span>

<dt>

<span data-ttu-id="daf30-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-161">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="daf30-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-162">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="daf30-162">**ServiceType**</span></span>
<span data-ttu-id="daf30-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-164">Описание того, как служба представляет себя на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="daf30-164">The description of how a service presents itself on the host computer.</span></span> <span data-ttu-id="daf30-165">Это свойство может иметь значение 0 или быть сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="daf30-165">This property can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="daf30-166">\_ \_ Драйвер ядра службы ADS \* \* \* \* \_ (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="daf30-166">\*\*\*\*ADS\_SERVICE\_KERNEL\_DRIVER\*\*\*\* (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="daf30-167">\_ \_ \_ Драйвер файловой системы ADS \_ \* \* \* \* (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="daf30-167">\*\*\*\*ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER\*\*\*\* (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="daf30-168">\_ \_ Собственный процесс службы ADS \_ \* \* \* \* (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="daf30-168">\*\*\*\*ADS\_SERVICE\_OWN\_PROCESS\*\*\*\* (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="daf30-169">\_ \_ Общий процесс службы ADS \_ \* \* \* \* (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="daf30-169">\*\*\*\*ADS\_SERVICE\_SHARE\_PROCESS\*\*\*\* (0x00000020)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="daf30-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-171">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="daf30-171">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-172">**Тип запуска**</span><span class="sxs-lookup"><span data-stu-id="daf30-172">**StartType**</span></span>
<span data-ttu-id="daf30-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-174">Определяет, как запустить службу.</span><span class="sxs-lookup"><span data-stu-id="daf30-174">Determines how to start the service.</span></span> <span data-ttu-id="daf30-175">Ниже приведены допустимые значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="daf30-175">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="daf30-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\_Запуск службы \_ ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\*\*\*\*ADS\_SERVICE\_BOOT\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-177">Служба — это драйвер устройства, запускаемый системным загрузчиком.</span><span class="sxs-lookup"><span data-stu-id="daf30-177">The service is a device driver started by the system loader.</span></span> <span data-ttu-id="daf30-178">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="daf30-178">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="daf30-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_ \_ Запуск системы службы ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\*\*\*\*ADS\_SERVICE\_SYSTEM\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-180">Служба — это драйвер устройства, запускаемый функцией **иоинитсистем** .</span><span class="sxs-lookup"><span data-stu-id="daf30-180">The service is a device driver started by the **IoInitSystem** function.</span></span> <span data-ttu-id="daf30-181">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="daf30-181">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="daf30-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_ \_ Автоматический запуск службы ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\*\*\*\*ADS\_SERVICE\_AUTO\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-183">Служба будет автоматически запущена диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="daf30-183">The service will be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="daf30-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\_ \_ Запуск запроса службы ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\*\*\*\*ADS\_SERVICE\_DEMAND\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-185">Служба будет запущена диспетчером управления службами, когда процесс вызывает функцию [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="daf30-185">The service will be started by the service control manager when a process calls the [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) function.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="daf30-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_служба ADS \_ отключена \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="daf30-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\*\*\*\*ADS\_SERVICE\_DISABLED\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="daf30-187">Запуск службы невозможен.</span><span class="sxs-lookup"><span data-stu-id="daf30-187">The service cannot be started.</span></span> <span data-ttu-id="daf30-188">Попытки запустить результат службы в **службе ошибки кода ошибки \_ \_ отключены**.</span><span class="sxs-lookup"><span data-stu-id="daf30-188">Attempts to start the service result in the error code **ERROR\_SERVICE\_DISABLED**.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="daf30-189">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-189">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-190">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="daf30-190">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-191">**стартуппараметерс**</span><span class="sxs-lookup"><span data-stu-id="daf30-191">**StartupParameters**</span></span>
<span data-ttu-id="daf30-192"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-192"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-193">Параметры, передаваемые в службу при запуске.</span><span class="sxs-lookup"><span data-stu-id="daf30-193">Parameters passed to the service at startup.</span></span>

<dt>

<span data-ttu-id="daf30-194">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-195">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="daf30-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="daf30-196">**Version**</span><span class="sxs-lookup"><span data-stu-id="daf30-196">**Version**</span></span>
<span data-ttu-id="daf30-197"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="daf30-197"></dt> <dd> <dl></span></span>

<span data-ttu-id="daf30-198">Версия службы.</span><span class="sxs-lookup"><span data-stu-id="daf30-198">Version of the service.</span></span>

<dt>

<span data-ttu-id="daf30-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daf30-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="daf30-200">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="daf30-200">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="daf30-201">Примеры</span><span class="sxs-lookup"><span data-stu-id="daf30-201">Examples</span></span>

<span data-ttu-id="daf30-202">В следующем примере кода показано, как получить список всех доступных системных служб, работающих на главном компьютере, "Мойкомпьютер" вместе с расположением для поиска исполняемых файлов служб.</span><span class="sxs-lookup"><span data-stu-id="daf30-202">The following code example shows how to list all the available system services running on the host computer, "myMachine", together with the location to find the executables of the services.</span></span>


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a><span data-ttu-id="daf30-203">Требования</span><span class="sxs-lookup"><span data-stu-id="daf30-203">Requirements</span></span>



| <span data-ttu-id="daf30-204">Требование</span><span class="sxs-lookup"><span data-stu-id="daf30-204">Requirement</span></span> | <span data-ttu-id="daf30-205">Значение</span><span class="sxs-lookup"><span data-stu-id="daf30-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="daf30-206">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="daf30-206">Minimum supported client</span></span><br/> | <span data-ttu-id="daf30-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="daf30-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="daf30-208">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="daf30-208">Minimum supported server</span></span><br/> | <span data-ttu-id="daf30-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="daf30-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="daf30-210">Header</span><span class="sxs-lookup"><span data-stu-id="daf30-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="daf30-211"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="daf30-211"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="daf30-212">DLL</span><span class="sxs-lookup"><span data-stu-id="daf30-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daf30-213"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daf30-213"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="daf30-214">IID</span><span class="sxs-lookup"><span data-stu-id="daf30-214">IID</span></span><br/>                      | <span data-ttu-id="daf30-215">IID \_ иадссервице определен как 68AF66E0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="daf30-215">IID\_IADsService is defined as 68AF66E0-31CA-11CF-A98A-00AA006BC149</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="daf30-216">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="daf30-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf30-217">**иадссервице**</span><span class="sxs-lookup"><span data-stu-id="daf30-217">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="daf30-218">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="daf30-218">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

