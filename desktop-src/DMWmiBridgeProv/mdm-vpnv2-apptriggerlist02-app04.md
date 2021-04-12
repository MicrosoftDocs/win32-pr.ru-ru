---
title: Класс MDM_VPNv2_AppTriggerList02_App04
description: Класс MDM \_ VPNv2AppTriggerList02 \_ App04 описывает список приложений, настроенных для активации VPN.
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- Класс MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62685ea94b99e843625e87e7c653a2ff19ab737d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136223"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a><span data-ttu-id="9c4e1-105">\_ \_ Класс App04 поддержка VPNV2 AppTriggerList02 MDM \_</span><span class="sxs-lookup"><span data-stu-id="9c4e1-105">MDM\_VPNv2\_AppTriggerList02\_App04 class</span></span>

<span data-ttu-id="9c4e1-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9c4e1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9c4e1-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9c4e1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9c4e1-108">Класс **MDM \_ VPNv2AppTriggerList02 \_ App04** описывает список приложений, настроенных для активации VPN.</span><span class="sxs-lookup"><span data-stu-id="9c4e1-108">The **MDM\_VPNv2AppTriggerList02\_App04** class describes a list of applications set to trigger the VPN.</span></span>

<span data-ttu-id="9c4e1-109">Если какое-либо из этих приложений запущено и профиль VPN в настоящее время является активным, этот профиль VPN будет активирован для подключения.</span><span class="sxs-lookup"><span data-stu-id="9c4e1-109">If any of these apps are launched and the VPN profile is currently the active profile, this VPN profile will be triggered to connect.</span></span>

<span data-ttu-id="9c4e1-110">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9c4e1-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c4e1-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c4e1-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="9c4e1-112">Члены</span><span class="sxs-lookup"><span data-stu-id="9c4e1-112">Members</span></span>

<span data-ttu-id="9c4e1-113">Класс **MDM \_ Поддержка vpnv2 \_ AppTriggerList02 \_ App04** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c4e1-113">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="9c4e1-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c4e1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c4e1-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c4e1-115">Properties</span></span>

<span data-ttu-id="9c4e1-116">Класс **MDM \_ Поддержка vpnv2 \_ AppTriggerList02 \_ App04** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9c4e1-116">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9c4e1-117">Id</span><span class="sxs-lookup"><span data-stu-id="9c4e1-117">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c4e1-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c4e1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c4e1-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9c4e1-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c4e1-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9c4e1-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c4e1-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c4e1-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c4e1-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c4e1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c4e1-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c4e1-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9c4e1-124">Узел приложения под идентификатором строки.</span><span class="sxs-lookup"><span data-stu-id="9c4e1-124">App Node under the Row Id.</span></span>

</dd> <dt>

<span data-ttu-id="9c4e1-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9c4e1-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c4e1-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c4e1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c4e1-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c4e1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c4e1-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c4e1-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9c4e1-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="9c4e1-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="9c4e1-130">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/апптригжерлист/*апптригжерровид*"</span><span class="sxs-lookup"><span data-stu-id="9c4e1-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span></span>

</dd> <dt>

[<span data-ttu-id="9c4e1-131">Тип</span><span class="sxs-lookup"><span data-stu-id="9c4e1-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c4e1-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c4e1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c4e1-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9c4e1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c4e1-134">Требования</span><span class="sxs-lookup"><span data-stu-id="9c4e1-134">Requirements</span></span>



| <span data-ttu-id="9c4e1-135">Требование</span><span class="sxs-lookup"><span data-stu-id="9c4e1-135">Requirement</span></span> | <span data-ttu-id="9c4e1-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9c4e1-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c4e1-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c4e1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9c4e1-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9c4e1-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c4e1-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c4e1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9c4e1-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9c4e1-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9c4e1-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9c4e1-141">Namespace</span></span><br/>                | <span data-ttu-id="9c4e1-142">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9c4e1-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9c4e1-143">MOF</span><span class="sxs-lookup"><span data-stu-id="9c4e1-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c4e1-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c4e1-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c4e1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9c4e1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c4e1-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c4e1-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c4e1-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c4e1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c4e1-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="9c4e1-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

