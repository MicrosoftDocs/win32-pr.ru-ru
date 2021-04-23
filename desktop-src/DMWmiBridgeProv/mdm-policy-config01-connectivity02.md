---
title: Класс MDM_Policy_Config01_Connectivity02
description: '\_Класс политики MDM \_ Config01 \_ Connectivity02 представляет доступные политики подключения.'
ms.assetid: 670e48c2-1af1-45e9-81c6-cdf3a310240f
keywords:
- Класс MDM_Policy_Config01_Connectivity02
- MDM_Policy_Config01_Connectivity02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Connectivity02
- MDM_Policy_Config01_Connectivity02.InstanceID
- MDM_Policy_Config01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b39b897998bf47c5f5411456ccae7fcb6927aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801876"
---
# <a name="mdm_policy_config01_connectivity02-class"></a><span data-ttu-id="803e5-105">\_Класс политики MDM \_ Config01 \_ Connectivity02</span><span class="sxs-lookup"><span data-stu-id="803e5-105">MDM\_Policy\_Config01\_Connectivity02 class</span></span>

<span data-ttu-id="803e5-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="803e5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="803e5-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="803e5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="803e5-108">Класс **\_ политики MDM \_ Config01 \_ Connectivity02** представляет доступные политики подключения.</span><span class="sxs-lookup"><span data-stu-id="803e5-108">The **MDM\_Policy\_Config01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="803e5-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="803e5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="803e5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="803e5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Connectivity02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBluetooth;
  sint32 AllowCellularData;
  sint32 AllowCellularDataRoaming;
  sint32 AllowVPNOverCellular;
  sint32 AllowVPNRoamingOverCellular;
  string DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards;
  string DisableDownloadingOfPrintDriversOverHTTP;
  string DiablePrintingOverHTTP;
  string HardenedUNCPaths;
  string ProhibitInstallationAndConfigurationOfNetworkBridge;
  sint32 DisallowNetworkConnectivityActiveTests;
  sint32 AllowConnectedDevices;
};
```

## <a name="members"></a><span data-ttu-id="803e5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="803e5-111">Members</span></span>

<span data-ttu-id="803e5-112">Класс **\_ политики MDM \_ Config01 \_ Connectivity02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="803e5-112">The **MDM\_Policy\_Config01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="803e5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="803e5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="803e5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="803e5-114">Properties</span></span>

<span data-ttu-id="803e5-115">Класс **\_ политики MDM \_ Config01 \_ Connectivity02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="803e5-115">The **MDM\_Policy\_Config01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="803e5-116">AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="803e5-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="803e5-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-119">AllowCellularData</span><span class="sxs-lookup"><span data-stu-id="803e5-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="803e5-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-122">AllowCellularDataRoaming</span><span class="sxs-lookup"><span data-stu-id="803e5-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="803e5-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-125">AllowConnectedDevices</span><span class="sxs-lookup"><span data-stu-id="803e5-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="803e5-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="803e5-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="803e5-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-131">AllowVPNRoamingOverCellular</span><span class="sxs-lookup"><span data-stu-id="803e5-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="803e5-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-134">диаблепринтинговерхттп</span><span class="sxs-lookup"><span data-stu-id="803e5-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="803e5-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-137">дисабледовнлоадингофпринтдриверсоверхттп</span><span class="sxs-lookup"><span data-stu-id="803e5-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="803e5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-140">дисаблеинтернетдовнлоадфорвебпублишингандонлинеордерингвизардс</span><span class="sxs-lookup"><span data-stu-id="803e5-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="803e5-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-143">дисалловнетворкконнективитяктиветестс</span><span class="sxs-lookup"><span data-stu-id="803e5-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="803e5-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="803e5-146">харденедункпасс</span><span class="sxs-lookup"><span data-stu-id="803e5-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="803e5-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="803e5-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="803e5-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="803e5-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="803e5-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="803e5-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="803e5-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="803e5-153">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="803e5-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="803e5-154">Для этого класса строка имеет значение "подключение".</span><span class="sxs-lookup"><span data-stu-id="803e5-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="803e5-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="803e5-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="803e5-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="803e5-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="803e5-158">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="803e5-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="803e5-159">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="803e5-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="803e5-160">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="803e5-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="803e5-161">прохибитинсталлатионандконфигуратионофнетворкбридже</span><span class="sxs-lookup"><span data-stu-id="803e5-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="803e5-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="803e5-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="803e5-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="803e5-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="803e5-164">Требования</span><span class="sxs-lookup"><span data-stu-id="803e5-164">Requirements</span></span>



| <span data-ttu-id="803e5-165">Требование</span><span class="sxs-lookup"><span data-stu-id="803e5-165">Requirement</span></span> | <span data-ttu-id="803e5-166">Значение</span><span class="sxs-lookup"><span data-stu-id="803e5-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="803e5-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="803e5-167">Minimum supported client</span></span><br/> | <span data-ttu-id="803e5-168">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="803e5-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="803e5-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="803e5-169">Minimum supported server</span></span><br/> | <span data-ttu-id="803e5-170">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="803e5-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="803e5-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="803e5-171">Namespace</span></span><br/>                | <span data-ttu-id="803e5-172">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="803e5-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="803e5-173">MOF</span><span class="sxs-lookup"><span data-stu-id="803e5-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="803e5-174"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="803e5-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="803e5-175">DLL</span><span class="sxs-lookup"><span data-stu-id="803e5-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="803e5-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="803e5-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803e5-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="803e5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803e5-178">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="803e5-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

