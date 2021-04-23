---
title: Класс MDM_VPNv2_TrafficFilterList02_App04
description: Класс MDM \_ TrafficFilterList02 \_ App04 предоставляет конфигурацию приложений, которые разрешены через интерфейс VPN.
ms.assetid: a56d004b-8fe3-4187-8aad-962f1cab8f7f
keywords:
- Класс MDM_VPNv2_TrafficFilterList02_App04
- MDM_VPNv2_TrafficFilterList02_App04 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_App04
- MDM_VPNv2_TrafficFilterList02_App04.InstanceID
- MDM_VPNv2_TrafficFilterList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b1cd3edbfec5fa270f8404983af57dba4fad31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136747"
---
# <a name="mdm_vpnv2_trafficfilterlist02_app04-class"></a><span data-ttu-id="1a4a4-105">\_ \_ Класс App04 поддержка VPNV2 TrafficFilterList02 MDM \_</span><span class="sxs-lookup"><span data-stu-id="1a4a4-105">MDM\_VPNv2\_TrafficFilterList02\_App04 class</span></span>

<span data-ttu-id="1a4a4-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1a4a4-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1a4a4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1a4a4-108">Класс **MDM \_ TrafficFilterList02 \_ App04** предоставляет конфигурацию приложений, которые разрешены через интерфейс VPN.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-108">The **MDM\_TrafficFilterList02\_App04** class provides configuration of the apps that are allowed over the VPN interface.</span></span>

<span data-ttu-id="1a4a4-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4a4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a4a4-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="1a4a4-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1a4a4-111">Members</span></span>

<span data-ttu-id="1a4a4-112">Класс **MDM \_ Поддержка vpnv2 \_ TrafficFilterList02 \_ App04** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1a4a4-112">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="1a4a4-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a4a4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a4a4-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a4a4-114">Properties</span></span>

<span data-ttu-id="1a4a4-115">Класс **MDM \_ Поддержка vpnv2 \_ TrafficFilterList02 \_ App04** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-115">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1a4a4-116">Id</span><span class="sxs-lookup"><span data-stu-id="1a4a4-116">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a4a4-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1a4a4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a4a4-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1a4a4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a4a4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1a4a4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a4a4-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1a4a4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a4a4-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1a4a4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a4a4-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a4a4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a4a4-123">Правило VPN для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-123">Per app VPN rule.</span></span> <span data-ttu-id="1a4a4-124">Это позволит разрешить использование только указанных приложений через VPN-интерфейс.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-124">This will allow only the apps specified to be allowed over the VPN interface.</span></span> <span data-ttu-id="1a4a4-125">Для этого класса строка имеет значение "App".</span><span class="sxs-lookup"><span data-stu-id="1a4a4-125">For this class, the string is "App"</span></span>

</dd> <dt>

<span data-ttu-id="1a4a4-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1a4a4-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a4a4-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1a4a4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a4a4-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1a4a4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a4a4-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a4a4-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a4a4-130">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="1a4a4-131">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/траффикфилтерлист/*траффикфилтерлистид*"</span><span class="sxs-lookup"><span data-stu-id="1a4a4-131">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span></span>

</dd> <dt>

[<span data-ttu-id="1a4a4-132">Тип</span><span class="sxs-lookup"><span data-stu-id="1a4a4-132">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a4a4-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1a4a4-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a4a4-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1a4a4-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a4a4-135">Требования</span><span class="sxs-lookup"><span data-stu-id="1a4a4-135">Requirements</span></span>



| <span data-ttu-id="1a4a4-136">Требование</span><span class="sxs-lookup"><span data-stu-id="1a4a4-136">Requirement</span></span> | <span data-ttu-id="1a4a4-137">Значение</span><span class="sxs-lookup"><span data-stu-id="1a4a4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4a4-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a4a4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1a4a4-139">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1a4a4-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a4a4-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a4a4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1a4a4-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1a4a4-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1a4a4-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1a4a4-142">Namespace</span></span><br/>                | <span data-ttu-id="1a4a4-143">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1a4a4-143">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1a4a4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="1a4a4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a4a4-145"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a4a4-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a4a4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1a4a4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a4a4-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a4a4-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a4a4-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a4a4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a4a4-149">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="1a4a4-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

