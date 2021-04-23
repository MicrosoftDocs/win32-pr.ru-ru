---
title: Класс MDM_DeviceStatus_UAC01
description: Класс MDM \_ девицестатус \_ UAC01 используется предприятием для запроса состояния UAC на устройствах с их политиками предприятия.
ms.assetid: fb1ca1bb-229e-4eaa-a1e3-e790c1dab760
keywords:
- Класс MDM_DeviceStatus_UAC01
- MDM_DeviceStatus_UAC01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_UAC01
- MDM_DeviceStatus_UAC01.InstanceID
- MDM_DeviceStatus_UAC01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eecba42cd97bee660f66570e7f96c1ab2799f85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803113"
---
# <a name="mdm_devicestatus_uac01-class"></a><span data-ttu-id="44a08-105">\_Класс MDM девицестатус \_ UAC01</span><span class="sxs-lookup"><span data-stu-id="44a08-105">MDM\_DeviceStatus\_UAC01 class</span></span>

<span data-ttu-id="44a08-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="44a08-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="44a08-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="44a08-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="44a08-108">Класс **MDM \_ девицестатус \_ UAC01** используется предприятием для запроса состояния UAC на устройствах с их политиками предприятия.</span><span class="sxs-lookup"><span data-stu-id="44a08-108">The **MDM\_DeviceStatus\_UAC01** class is used by the enterprise to query the UAC status of devices with their enterprise policies.</span></span>

<span data-ttu-id="44a08-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="44a08-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a08-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44a08-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_UAC01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="44a08-111">Члены</span><span class="sxs-lookup"><span data-stu-id="44a08-111">Members</span></span>

<span data-ttu-id="44a08-112">Класс **MDM \_ девицестатус \_ UAC01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="44a08-112">The **MDM\_DeviceStatus\_UAC01** class has these types of members:</span></span>

-   [<span data-ttu-id="44a08-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="44a08-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44a08-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="44a08-114">Properties</span></span>

<span data-ttu-id="44a08-115">Класс **MDM \_ девицестатус \_ UAC01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44a08-115">The **MDM\_DeviceStatus\_UAC01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44a08-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="44a08-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a08-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44a08-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44a08-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44a08-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a08-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44a08-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44a08-120">Узел для запроса UAC.</span><span class="sxs-lookup"><span data-stu-id="44a08-120">Node for the UAC query.</span></span>

</dd> <dt>

<span data-ttu-id="44a08-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="44a08-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a08-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44a08-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44a08-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44a08-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a08-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44a08-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44a08-125">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="44a08-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="44a08-126">Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"</span><span class="sxs-lookup"><span data-stu-id="44a08-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="44a08-127">Состояние</span><span class="sxs-lookup"><span data-stu-id="44a08-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a08-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="44a08-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="44a08-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="44a08-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44a08-130">Требования</span><span class="sxs-lookup"><span data-stu-id="44a08-130">Requirements</span></span>



| <span data-ttu-id="44a08-131">Требование</span><span class="sxs-lookup"><span data-stu-id="44a08-131">Requirement</span></span> | <span data-ttu-id="44a08-132">Значение</span><span class="sxs-lookup"><span data-stu-id="44a08-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a08-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44a08-133">Minimum supported client</span></span><br/> | <span data-ttu-id="44a08-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="44a08-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44a08-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44a08-135">Minimum supported server</span></span><br/> | <span data-ttu-id="44a08-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="44a08-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="44a08-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="44a08-137">Namespace</span></span><br/>                | <span data-ttu-id="44a08-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="44a08-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="44a08-139">MOF</span><span class="sxs-lookup"><span data-stu-id="44a08-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44a08-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44a08-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="44a08-141">DLL</span><span class="sxs-lookup"><span data-stu-id="44a08-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44a08-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44a08-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

