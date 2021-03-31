---
title: Класс MDM_DeviceStatus_Compliance01
description: Класс MDM \_ девицестатус \_ Compliance01 позволяет запрашивать, соответствует ли устройство политике шифрования предприятия.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- Класс MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136783"
---
# <a name="mdm_devicestatus_compliance01-class"></a><span data-ttu-id="602e6-105">\_Класс MDM девицестатус \_ Compliance01</span><span class="sxs-lookup"><span data-stu-id="602e6-105">MDM\_DeviceStatus\_Compliance01 class</span></span>

<span data-ttu-id="602e6-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="602e6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="602e6-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="602e6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="602e6-108">Класс **MDM \_ девицестатус \_ Compliance01** позволяет запрашивать, соответствует ли устройство политике шифрования предприятия.</span><span class="sxs-lookup"><span data-stu-id="602e6-108">The **MDM\_DeviceStatus\_Compliance01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="602e6-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="602e6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="602e6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="602e6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a><span data-ttu-id="602e6-111">Члены</span><span class="sxs-lookup"><span data-stu-id="602e6-111">Members</span></span>

<span data-ttu-id="602e6-112">Класс **MDM \_ девицестатус \_ Compliance01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="602e6-112">The **MDM\_DeviceStatus\_Compliance01** class has these types of members:</span></span>

-   [<span data-ttu-id="602e6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="602e6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="602e6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="602e6-114">Properties</span></span>

<span data-ttu-id="602e6-115">Класс **MDM \_ девицестатус \_ Compliance01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="602e6-115">The **MDM\_DeviceStatus\_Compliance01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="602e6-116">енкриптионкомплианце</span><span class="sxs-lookup"><span data-stu-id="602e6-116">EncryptionCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="602e6-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="602e6-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="602e6-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="602e6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="602e6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="602e6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="602e6-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="602e6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="602e6-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="602e6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="602e6-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="602e6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="602e6-123">Узел для запросов на соответствие.</span><span class="sxs-lookup"><span data-stu-id="602e6-123">Node for queries on compliance.</span></span>

</dd> <dt>

<span data-ttu-id="602e6-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="602e6-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="602e6-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="602e6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="602e6-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="602e6-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="602e6-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="602e6-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="602e6-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="602e6-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="602e6-129">Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"</span><span class="sxs-lookup"><span data-stu-id="602e6-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="602e6-130">Требования</span><span class="sxs-lookup"><span data-stu-id="602e6-130">Requirements</span></span>



| <span data-ttu-id="602e6-131">Требование</span><span class="sxs-lookup"><span data-stu-id="602e6-131">Requirement</span></span> | <span data-ttu-id="602e6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="602e6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="602e6-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="602e6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="602e6-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="602e6-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="602e6-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="602e6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="602e6-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="602e6-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="602e6-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="602e6-137">Namespace</span></span><br/>                | <span data-ttu-id="602e6-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="602e6-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="602e6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="602e6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="602e6-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="602e6-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="602e6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="602e6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="602e6-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="602e6-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="602e6-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="602e6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="602e6-144">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="602e6-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

