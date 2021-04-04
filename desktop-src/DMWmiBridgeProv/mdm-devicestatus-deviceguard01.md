---
title: Класс MDM_DeviceStatus_DeviceGuard01
description: Класс MDM \_ девицестатус \_ DeviceGuard01 используется предприятием для отслеживания инвентаризации устройств и запроса состояния соответствия этих устройств корпоративным политикам.
ms.assetid: 267129f6-ec37-43ae-bba3-e21917012f27
keywords:
- Класс MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01.InstanceID
- MDM_DeviceStatus_DeviceGuard01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5f4dffa67ad86b5486dce372018efd29e62620
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989055"
---
# <a name="mdm_devicestatus_deviceguard01-class"></a><span data-ttu-id="ab56d-105">\_Класс MDM девицестатус \_ DeviceGuard01</span><span class="sxs-lookup"><span data-stu-id="ab56d-105">MDM\_DeviceStatus\_DeviceGuard01 class</span></span>

<span data-ttu-id="ab56d-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ab56d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ab56d-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="ab56d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ab56d-108">Класс MDM \_ девицестатус \_ DeviceGuard01 используется предприятием для отслеживания инвентаризации устройств и запроса состояния соответствия этих устройств корпоративным политикам.</span><span class="sxs-lookup"><span data-stu-id="ab56d-108">The MDM\_DeviceStatus\_DeviceGuard01 class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="ab56d-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ab56d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab56d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab56d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_DeviceGuard01
{
  string InstanceID;
  string ParentID;
  sint32 VirtualizationBasedSecurityHwReq;
  sint32 VirtualizationBasedSecurityStatus;
  sint32 LsaCfgCredGuardStatus;
};
```

## <a name="members"></a><span data-ttu-id="ab56d-111">Члены</span><span class="sxs-lookup"><span data-stu-id="ab56d-111">Members</span></span>

<span data-ttu-id="ab56d-112">Класс **MDM \_ девицестатус \_ DeviceGuard01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ab56d-112">The **MDM\_DeviceStatus\_DeviceGuard01** class has these types of members:</span></span>

-   [<span data-ttu-id="ab56d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab56d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab56d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab56d-114">Properties</span></span>

<span data-ttu-id="ab56d-115">Класс **MDM \_ девицестатус \_ DeviceGuard01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab56d-115">The **MDM\_DeviceStatus\_DeviceGuard01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab56d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ab56d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab56d-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab56d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab56d-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab56d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab56d-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab56d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ab56d-120">лсакфгкредгуардстатус</span><span class="sxs-lookup"><span data-stu-id="ab56d-120">LsaCfgCredGuardStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-lsacfgcredguardstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab56d-121">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ab56d-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab56d-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ab56d-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ab56d-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ab56d-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab56d-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab56d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab56d-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab56d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab56d-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab56d-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ab56d-127">виртуализатионбаседсекуритихврек</span><span class="sxs-lookup"><span data-stu-id="ab56d-127">VirtualizationBasedSecurityHwReq</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecurityhwreq)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab56d-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ab56d-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab56d-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ab56d-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ab56d-130">VirtualizationBasedSecurityStatus</span><span class="sxs-lookup"><span data-stu-id="ab56d-130">VirtualizationBasedSecurityStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecuritystatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab56d-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ab56d-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab56d-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ab56d-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab56d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ab56d-133">Requirements</span></span>



| <span data-ttu-id="ab56d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ab56d-134">Requirement</span></span> | <span data-ttu-id="ab56d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ab56d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab56d-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab56d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ab56d-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ab56d-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab56d-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab56d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ab56d-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ab56d-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ab56d-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ab56d-140">Namespace</span></span><br/>                | <span data-ttu-id="ab56d-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="ab56d-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ab56d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ab56d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab56d-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab56d-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab56d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ab56d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab56d-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab56d-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

