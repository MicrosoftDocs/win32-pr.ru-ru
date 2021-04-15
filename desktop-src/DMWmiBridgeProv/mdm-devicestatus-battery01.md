---
title: Класс MDM_DeviceStatus_Battery01
description: Класс MDM \_ девицестатус \_ Battery01 используется предприятием для запроса состояния совместимости устройств со своими корпоративными политиками.
ms.assetid: f4e92e2a-e267-467a-9905-2539dcaf8d8c
keywords:
- Класс MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01.InstanceID
- MDM_DeviceStatus_Battery01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b89cd709c4d0d3d5ad3490114bc82d36aa4ef0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654595"
---
# <a name="mdm_devicestatus_battery01-class"></a><span data-ttu-id="e0a4d-105">\_Класс MDM девицестатус \_ Battery01</span><span class="sxs-lookup"><span data-stu-id="e0a4d-105">MDM\_DeviceStatus\_Battery01 class</span></span>

<span data-ttu-id="e0a4d-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e0a4d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e0a4d-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e0a4d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e0a4d-108">Класс **MDM \_ девицестатус \_ Battery01** используется предприятием для запроса состояния совместимости устройств со своими корпоративными политиками.</span><span class="sxs-lookup"><span data-stu-id="e0a4d-108">The **MDM\_DeviceStatus\_Battery01** class is used by the enterprise to query the state of battery compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="e0a4d-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e0a4d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a4d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0a4d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Battery01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  sint32 EstimatedChargeRemaining;
  sint32 EstimatedRuntime;
};
```

## <a name="members"></a><span data-ttu-id="e0a4d-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e0a4d-111">Members</span></span>

<span data-ttu-id="e0a4d-112">Класс **MDM \_ девицестатус \_ Battery01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e0a4d-112">The **MDM\_DeviceStatus\_Battery01** class has these types of members:</span></span>

-   [<span data-ttu-id="e0a4d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0a4d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0a4d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0a4d-114">Properties</span></span>

<span data-ttu-id="e0a4d-115">Класс **MDM \_ девицестатус \_ Battery01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e0a4d-115">The **MDM\_DeviceStatus\_Battery01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e0a4d-116">естиматедчаржеремаининг</span><span class="sxs-lookup"><span data-stu-id="e0a4d-116">EstimatedChargeRemaining</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedchargeremaining)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a4d-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a4d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a4d-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e0a4d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a4d-119">EstimatedRuntime</span><span class="sxs-lookup"><span data-stu-id="e0a4d-119">EstimatedRuntime</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedruntime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a4d-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a4d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a4d-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e0a4d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e0a4d-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e0a4d-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a4d-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0a4d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0a4d-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0a4d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0a4d-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e0a4d-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e0a4d-126">Узел для запроса батареи.</span><span class="sxs-lookup"><span data-stu-id="e0a4d-126">Node for the battery query.</span></span>

</dd> <dt>

<span data-ttu-id="e0a4d-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e0a4d-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a4d-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0a4d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0a4d-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0a4d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0a4d-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e0a4d-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e0a4d-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="e0a4d-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="e0a4d-132">Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"</span><span class="sxs-lookup"><span data-stu-id="e0a4d-132">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="e0a4d-133">Состояние</span><span class="sxs-lookup"><span data-stu-id="e0a4d-133">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a4d-134">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a4d-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a4d-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e0a4d-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0a4d-136">Требования</span><span class="sxs-lookup"><span data-stu-id="e0a4d-136">Requirements</span></span>



| <span data-ttu-id="e0a4d-137">Требование</span><span class="sxs-lookup"><span data-stu-id="e0a4d-137">Requirement</span></span> | <span data-ttu-id="e0a4d-138">Значение</span><span class="sxs-lookup"><span data-stu-id="e0a4d-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a4d-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0a4d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e0a4d-140">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e0a4d-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0a4d-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0a4d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e0a4d-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e0a4d-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e0a4d-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e0a4d-143">Namespace</span></span><br/>                | <span data-ttu-id="e0a4d-144">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e0a4d-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e0a4d-145">MOF</span><span class="sxs-lookup"><span data-stu-id="e0a4d-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0a4d-146"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0a4d-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0a4d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e0a4d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0a4d-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0a4d-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

