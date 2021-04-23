---
title: Класс MDM_DeviceStatus
description: Класс MDM \_ девицестатус используется предприятием для отслеживания инвентаризации устройств и запроса состояния соответствия этих устройств их корпоративными политиками.
ms.assetid: fceaaf36-8f33-410a-89b4-c824b10164d5
keywords:
- Класс MDM_DeviceStatus
- MDM_DeviceStatus класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus
- MDM_DeviceStatus.InstanceID
- MDM_DeviceStatus.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751a33553b4a00ac6719ce6e24c75a03444f0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136775"
---
# <a name="mdm_devicestatus-class"></a><span data-ttu-id="caebb-105">\_Класс MDM девицестатус</span><span class="sxs-lookup"><span data-stu-id="caebb-105">MDM\_DeviceStatus class</span></span>

<span data-ttu-id="caebb-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="caebb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="caebb-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="caebb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="caebb-108">Класс **MDM \_ девицестатус** используется предприятием для отслеживания инвентаризации устройств и запроса состояния соответствия этих устройств их корпоративными политиками.</span><span class="sxs-lookup"><span data-stu-id="caebb-108">The **MDM\_DeviceStatus** class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="caebb-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="caebb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="caebb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="caebb-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus
{
  string InstanceID;
  string ParentID;
  sint32 SecureBootState;
  string DomainName;
};
```

## <a name="members"></a><span data-ttu-id="caebb-111">Члены</span><span class="sxs-lookup"><span data-stu-id="caebb-111">Members</span></span>

<span data-ttu-id="caebb-112">Класс **MDM \_ девицестатус** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="caebb-112">The **MDM\_DeviceStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="caebb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="caebb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="caebb-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="caebb-114">Properties</span></span>

<span data-ttu-id="caebb-115">Класс **MDM \_ девицестатус** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="caebb-115">The **MDM\_DeviceStatus** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="caebb-116">Имя_домена</span><span class="sxs-lookup"><span data-stu-id="caebb-116">DomainName</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="caebb-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="caebb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caebb-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="caebb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="caebb-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="caebb-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caebb-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="caebb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caebb-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="caebb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caebb-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="caebb-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="caebb-123">Корневой узел для поставщика службы настройки Девицестатус.</span><span class="sxs-lookup"><span data-stu-id="caebb-123">The root node for the DeviceStatus configuration service provider.</span></span>

</dd> <dt>

<span data-ttu-id="caebb-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="caebb-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="caebb-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="caebb-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="caebb-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="caebb-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caebb-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="caebb-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="caebb-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="caebb-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="caebb-129">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="caebb-129">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="caebb-130">секуребутстате</span><span class="sxs-lookup"><span data-stu-id="caebb-130">SecureBootState</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-securebootstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="caebb-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="caebb-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="caebb-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="caebb-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="caebb-133">Требования</span><span class="sxs-lookup"><span data-stu-id="caebb-133">Requirements</span></span>



| <span data-ttu-id="caebb-134">Требование</span><span class="sxs-lookup"><span data-stu-id="caebb-134">Requirement</span></span> | <span data-ttu-id="caebb-135">Значение</span><span class="sxs-lookup"><span data-stu-id="caebb-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caebb-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="caebb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="caebb-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="caebb-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="caebb-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="caebb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="caebb-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="caebb-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="caebb-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="caebb-140">Namespace</span></span><br/>                | <span data-ttu-id="caebb-141">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="caebb-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="caebb-142">MOF</span><span class="sxs-lookup"><span data-stu-id="caebb-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="caebb-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="caebb-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="caebb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="caebb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caebb-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caebb-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caebb-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caebb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caebb-147">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="caebb-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

