---
title: Класс MDM_DeviceManageability_Provider01_01
description: Класс MDM \_ девицеманажеабилити \_ Provider01 \_ 01 используется для получения общих сведений о возможностях конфигурации MDM на устройстве.
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- Класс MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1ef064bcffd5303a3ef820dc0b463a3b5e622b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892321"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a><span data-ttu-id="1ec30-105">\_Класс MDM девицеманажеабилити \_ Provider01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="1ec30-105">MDM\_DeviceManageability\_Provider01\_01 class</span></span>

<span data-ttu-id="1ec30-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1ec30-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1ec30-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1ec30-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1ec30-108">Класс MDM \_ девицеманажеабилити \_ Provider01 \_ 01 используется для получения общих сведений о возможностях конфигурации MDM на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1ec30-108">The MDM\_DeviceManageability\_Provider01\_01 class is used retrieve the general information about MDM configuration capabilities on the device.</span></span>

<span data-ttu-id="1ec30-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1ec30-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec30-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ec30-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a><span data-ttu-id="1ec30-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1ec30-111">Members</span></span>

<span data-ttu-id="1ec30-112">Класс **MDM \_ девицеманажеабилити \_ Provider01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1ec30-112">The **MDM\_DeviceManageability\_Provider01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="1ec30-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1ec30-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ec30-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1ec30-114">Properties</span></span>

<span data-ttu-id="1ec30-115">Класс **MDM \_ девицеманажеабилити \_ Provider01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="1ec30-115">The **MDM\_DeviceManageability\_Provider01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1ec30-116">конфигинфо</span><span class="sxs-lookup"><span data-stu-id="1ec30-116">ConfigInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ec30-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1ec30-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ec30-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1ec30-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1ec30-119">Необходимо задать значение для WMI \_ Bridge \_ Server.</span><span class="sxs-lookup"><span data-stu-id="1ec30-119">You must set the value to WMI\_Bridge\_Server.</span></span> <span data-ttu-id="1ec30-120">Вызывающий объект не может динамически задавать идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="1ec30-120">The caller cannot dynamically set the Provider ID.</span></span>

</dd> <dt>

[<span data-ttu-id="1ec30-121">енроллментинфо</span><span class="sxs-lookup"><span data-stu-id="1ec30-121">EnrollmentInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ec30-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1ec30-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ec30-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1ec30-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ec30-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ec30-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ec30-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1ec30-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ec30-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1ec30-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ec30-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ec30-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ec30-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1ec30-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ec30-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1ec30-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ec30-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1ec30-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ec30-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ec30-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ec30-132">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec30-132">Requirements</span></span>



| <span data-ttu-id="1ec30-133">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec30-133">Requirement</span></span> | <span data-ttu-id="1ec30-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec30-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec30-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ec30-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec30-136">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1ec30-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ec30-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ec30-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec30-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1ec30-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="1ec30-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1ec30-139">Namespace</span></span><br/>                | <span data-ttu-id="1ec30-140">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1ec30-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="1ec30-141">MOF</span><span class="sxs-lookup"><span data-stu-id="1ec30-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ec30-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ec30-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ec30-143">DLL</span><span class="sxs-lookup"><span data-stu-id="1ec30-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ec30-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ec30-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

