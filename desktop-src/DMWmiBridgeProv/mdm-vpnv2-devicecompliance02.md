---
title: Класс MDM_VPNv2_DeviceCompliance02
description: Зарезервировано для будущего использования. | Класс MDM_VPNv2_DeviceCompliance02
ms.assetid: f84f4812-3083-46c4-a60c-919ec92c844f
keywords:
- Класс MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02.InstanceID
- MDM_VPNv2_DeviceCompliance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a454a5cce3a40066c7cf14a60bdeeb81dcabab9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105647793"
---
# <a name="mdm_vpnv2_devicecompliance02-class"></a><span data-ttu-id="fdeb9-106">\_Класс MDM поддержка vpnv2 \_ DeviceCompliance02</span><span class="sxs-lookup"><span data-stu-id="fdeb9-106">MDM\_VPNv2\_DeviceCompliance02 class</span></span>

<span data-ttu-id="fdeb9-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="fdeb9-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fdeb9-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="fdeb9-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fdeb9-109">Зарезервировано для будущего использования</span><span class="sxs-lookup"><span data-stu-id="fdeb9-109">Reserved for Future Use</span></span>

<span data-ttu-id="fdeb9-110">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fdeb9-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdeb9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdeb9-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DeviceCompliance02
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
};
```

## <a name="members"></a><span data-ttu-id="fdeb9-112">Члены</span><span class="sxs-lookup"><span data-stu-id="fdeb9-112">Members</span></span>

<span data-ttu-id="fdeb9-113">Класс **MDM \_ Поддержка vpnv2 \_ DeviceCompliance02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fdeb9-113">The **MDM\_VPNv2\_DeviceCompliance02** class has these types of members:</span></span>

-   [<span data-ttu-id="fdeb9-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="fdeb9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fdeb9-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="fdeb9-115">Properties</span></span>

<span data-ttu-id="fdeb9-116">Класс **MDM \_ Поддержка vpnv2 \_ DeviceCompliance02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fdeb9-116">The **MDM\_VPNv2\_DeviceCompliance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fdeb9-117">Enabled</span><span class="sxs-lookup"><span data-stu-id="fdeb9-117">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdeb9-118">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fdeb9-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fdeb9-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fdeb9-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fdeb9-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fdeb9-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdeb9-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fdeb9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdeb9-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdeb9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdeb9-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fdeb9-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fdeb9-124">Добавлено в Windows 10 версии 1607.</span><span class="sxs-lookup"><span data-stu-id="fdeb9-124">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="fdeb9-125">Узлы в Девицекомплианце можно использовать для включения условного доступа на основе AAD для VPN.</span><span class="sxs-lookup"><span data-stu-id="fdeb9-125">Nodes under DeviceCompliance can be used to enable AAD-based Conditional Access for VPN.</span></span>

</dd> <dt>

<span data-ttu-id="fdeb9-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fdeb9-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdeb9-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fdeb9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdeb9-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdeb9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdeb9-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fdeb9-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fdeb9-130">Добавлено в Windows 10 версии 1607.</span><span class="sxs-lookup"><span data-stu-id="fdeb9-130">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="fdeb9-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="fdeb9-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="fdeb9-132">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*"</span><span class="sxs-lookup"><span data-stu-id="fdeb9-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fdeb9-133">Требования</span><span class="sxs-lookup"><span data-stu-id="fdeb9-133">Requirements</span></span>



| <span data-ttu-id="fdeb9-134">Требование</span><span class="sxs-lookup"><span data-stu-id="fdeb9-134">Requirement</span></span> | <span data-ttu-id="fdeb9-135">Значение</span><span class="sxs-lookup"><span data-stu-id="fdeb9-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdeb9-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdeb9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fdeb9-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fdeb9-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fdeb9-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdeb9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fdeb9-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fdeb9-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fdeb9-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fdeb9-140">Namespace</span></span><br/>                | <span data-ttu-id="fdeb9-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="fdeb9-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fdeb9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fdeb9-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdeb9-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdeb9-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdeb9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fdeb9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdeb9-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdeb9-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdeb9-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdeb9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdeb9-147">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="fdeb9-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

