---
title: Класс MDM_DeviceStatus_NetworkIdentifiers01_01
description: Класс MDM \_ девицестатус \_ NetworkIdentifiers01 \_ 01 позволяет запрашивать свойства сети на устройстве.
ms.assetid: 2439010e-62fa-4482-b280-b9f98d1fbb7b
keywords:
- Класс MDM_DeviceStatus_NetworkIdentifiers01_01
- MDM_DeviceStatus_NetworkIdentifiers01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_NetworkIdentifiers01_01
- MDM_DeviceStatus_NetworkIdentifiers01_01.InstanceID
- MDM_DeviceStatus_NetworkIdentifiers01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530c301894d957c9a9a2db374f35cf7c1bcb5063
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071851"
---
# <a name="mdm_devicestatus_networkidentifiers01_01-class"></a><span data-ttu-id="1c9c2-105">\_Класс MDM девицестатус \_ NetworkIdentifiers01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="1c9c2-105">MDM\_DeviceStatus\_NetworkIdentifiers01\_01 class</span></span>

<span data-ttu-id="1c9c2-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1c9c2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1c9c2-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1c9c2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1c9c2-108">Класс **MDM \_ девицестатус \_ NetworkIdentifiers01 \_ 01** позволяет запрашивать свойства сети на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1c9c2-108">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class allows you to query a device for network properties.</span></span>

<span data-ttu-id="1c9c2-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1c9c2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9c2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c9c2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_NetworkIdentifiers01_01
{
  string  InstanceID;
  string  ParentID;
  string  IPAddressV4;
  string  IPAddressV6;
  boolean IsConnected;
  sint32  Type;
};
```

## <a name="members"></a><span data-ttu-id="1c9c2-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1c9c2-111">Members</span></span>

<span data-ttu-id="1c9c2-112">Класс **MDM \_ девицестатус \_ NetworkIdentifiers01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c9c2-112">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="1c9c2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c9c2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c9c2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c9c2-114">Properties</span></span>

<span data-ttu-id="1c9c2-115">Класс **MDM \_ девицестатус \_ NetworkIdentifiers01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="1c9c2-115">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c9c2-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1c9c2-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9c2-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c9c2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c9c2-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c9c2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c9c2-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c9c2-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c9c2-120">Узел для запросов к свойствам сети и устройства.</span><span class="sxs-lookup"><span data-stu-id="1c9c2-120">Node for queries on network and device properties.</span></span>

</dd> <dt>

[<span data-ttu-id="1c9c2-121">IPAddressV4</span><span class="sxs-lookup"><span data-stu-id="1c9c2-121">IPAddressV4</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9c2-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c9c2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c9c2-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1c9c2-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c9c2-124">IPAddressV6</span><span class="sxs-lookup"><span data-stu-id="1c9c2-124">IPAddressV6</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv6)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9c2-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c9c2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c9c2-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1c9c2-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c9c2-127">Подсоединено</span><span class="sxs-lookup"><span data-stu-id="1c9c2-127">IsConnected</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-isconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9c2-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1c9c2-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c9c2-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1c9c2-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c9c2-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1c9c2-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9c2-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c9c2-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c9c2-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c9c2-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c9c2-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c9c2-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c9c2-134">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="1c9c2-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="1c9c2-135">Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"</span><span class="sxs-lookup"><span data-stu-id="1c9c2-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="1c9c2-136">Тип</span><span class="sxs-lookup"><span data-stu-id="1c9c2-136">Type</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9c2-137">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1c9c2-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c9c2-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1c9c2-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c9c2-139">Требования</span><span class="sxs-lookup"><span data-stu-id="1c9c2-139">Requirements</span></span>



| <span data-ttu-id="1c9c2-140">Требование</span><span class="sxs-lookup"><span data-stu-id="1c9c2-140">Requirement</span></span> | <span data-ttu-id="1c9c2-141">Значение</span><span class="sxs-lookup"><span data-stu-id="1c9c2-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9c2-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c9c2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1c9c2-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1c9c2-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c9c2-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c9c2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1c9c2-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c9c2-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1c9c2-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c9c2-146">Namespace</span></span><br/>                | <span data-ttu-id="1c9c2-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1c9c2-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1c9c2-148">MOF</span><span class="sxs-lookup"><span data-stu-id="1c9c2-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c9c2-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c9c2-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c9c2-150">DLL</span><span class="sxs-lookup"><span data-stu-id="1c9c2-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c9c2-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c9c2-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c9c2-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c9c2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c9c2-153">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="1c9c2-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

