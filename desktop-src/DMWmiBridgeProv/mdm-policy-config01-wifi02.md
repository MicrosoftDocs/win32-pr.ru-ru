---
title: Класс MDM_Policy_Config01_WiFi02
description: '\_Класс политики MDM \_ Config01 \_ WiFi02 представляет доступные политики Wi-Fi.'
ms.assetid: 68CFBB5E-F365-4D1A-8EF1-CC070E9A7982
keywords:
- Класс MDM_Policy_Config01_WiFi02
- MDM_Policy_Config01_WiFi02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WiFi02
- MDM_Policy_Config01_WiFi02.InstanceID
- MDM_Policy_Config01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00848613f1f0e9fd4ab6db9dc4afdabe54ce538c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891997"
---
# <a name="mdm_policy_config01_wifi02-class"></a><span data-ttu-id="95b4e-105">\_Класс политики MDM \_ Config01 \_ WiFi02</span><span class="sxs-lookup"><span data-stu-id="95b4e-105">MDM\_Policy\_Config01\_WiFi02 class</span></span>

<span data-ttu-id="95b4e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="95b4e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="95b4e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="95b4e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="95b4e-108">Класс **\_ политики MDM \_ Config01 \_ WiFi02** представляет доступные политики Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="95b4e-108">The **MDM\_Policy\_Config01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="95b4e-109">Эти политики определяют разрешенные Wi-Fi конфигурации.</span><span class="sxs-lookup"><span data-stu-id="95b4e-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="95b4e-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="95b4e-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b4e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95b4e-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WiFi02
{
  string InstanceID;
  string ParentID;
  sint32 AllowInternetSharing;
  sint32 AllowWiFi;
  sint32 AllowWiFiDirect;
  sint32 AllowManualWiFiConfiguration;
  sint32 AllowAutoConnectToWiFiSenseHotspots;
  sint32 WLANScanMode;
};
```

## <a name="members"></a><span data-ttu-id="95b4e-112">Члены</span><span class="sxs-lookup"><span data-stu-id="95b4e-112">Members</span></span>

<span data-ttu-id="95b4e-113">Класс **\_ политики MDM \_ Config01 \_ WiFi02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="95b4e-113">The **MDM\_Policy\_Config01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="95b4e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="95b4e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95b4e-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="95b4e-115">Properties</span></span>

<span data-ttu-id="95b4e-116">Класс **\_ политики MDM \_ Config01 \_ WiFi02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="95b4e-116">The **MDM\_Policy\_Config01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="95b4e-117">AllowAutoConnectToWiFiSenseHotspots</span><span class="sxs-lookup"><span data-stu-id="95b4e-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="95b4e-118">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="95b4e-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="95b4e-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="95b4e-120">AllowInternetSharing</span><span class="sxs-lookup"><span data-stu-id="95b4e-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="95b4e-121">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="95b4e-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="95b4e-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="95b4e-123">AllowManualWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="95b4e-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="95b4e-124">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="95b4e-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="95b4e-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="95b4e-126">AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="95b4e-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="95b4e-127">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="95b4e-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="95b4e-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="95b4e-129">алловвифидирект</span><span class="sxs-lookup"><span data-stu-id="95b4e-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="95b4e-130">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="95b4e-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="95b4e-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="95b4e-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="95b4e-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95b4e-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95b4e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95b4e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-135">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="95b4e-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="95b4e-136">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="95b4e-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="95b4e-137">Для этого класса строка имеет значение Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="95b4e-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="95b4e-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="95b4e-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95b4e-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95b4e-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95b4e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-141">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="95b4e-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="95b4e-142">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="95b4e-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="95b4e-143">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="95b4e-143">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="95b4e-144">WLANScanMode</span><span class="sxs-lookup"><span data-stu-id="95b4e-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="95b4e-145">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="95b4e-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95b4e-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="95b4e-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95b4e-147">Требования</span><span class="sxs-lookup"><span data-stu-id="95b4e-147">Requirements</span></span>



| <span data-ttu-id="95b4e-148">Требование</span><span class="sxs-lookup"><span data-stu-id="95b4e-148">Requirement</span></span> | <span data-ttu-id="95b4e-149">Значение</span><span class="sxs-lookup"><span data-stu-id="95b4e-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b4e-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95b4e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="95b4e-151">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="95b4e-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95b4e-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95b4e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="95b4e-153">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="95b4e-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="95b4e-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="95b4e-154">Namespace</span></span><br/>                | <span data-ttu-id="95b4e-155">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="95b4e-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="95b4e-156">MOF</span><span class="sxs-lookup"><span data-stu-id="95b4e-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95b4e-157"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95b4e-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="95b4e-158">DLL</span><span class="sxs-lookup"><span data-stu-id="95b4e-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95b4e-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b4e-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b4e-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95b4e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b4e-161">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="95b4e-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

