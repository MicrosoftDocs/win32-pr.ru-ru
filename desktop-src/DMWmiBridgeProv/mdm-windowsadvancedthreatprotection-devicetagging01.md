---
title: Класс MDM_WindowsAdvancedThreatProtection_DeviceTagging01
description: Класс MDM \_ виндовсадванцедсреатпротектион \_ DeviceTagging01 используется для подключения, определения состояния конфигурации и работоспособности, а также конечных точек отключение для Advanced Threat Protection в Защитнике Windows.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- Класс MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01 класс, описание
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136742"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a><span data-ttu-id="4d7ea-105">\_Класс MDM виндовсадванцедсреатпротектион \_ DeviceTagging01</span><span class="sxs-lookup"><span data-stu-id="4d7ea-105">MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class</span></span>

<span data-ttu-id="4d7ea-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4d7ea-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4d7ea-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4d7ea-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4d7ea-108">Класс MDM \_ виндовсадванцедсреатпротектион \_ DeviceTagging01 используется для подключения, определения состояния конфигурации и работоспособности, а также конечных точек отключение для Advanced Threat Protection в Защитнике Windows.</span><span class="sxs-lookup"><span data-stu-id="4d7ea-108">The MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class is used to onboard, determine configuration and health status, and offboard endpoints for Windows Defender Advanced Threat Protection.</span></span>

<span data-ttu-id="4d7ea-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4d7ea-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7ea-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d7ea-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a><span data-ttu-id="4d7ea-111">Члены</span><span class="sxs-lookup"><span data-stu-id="4d7ea-111">Members</span></span>

<span data-ttu-id="4d7ea-112">Класс **MDM \_ виндовсадванцедсреатпротектион \_ DeviceTagging01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4d7ea-112">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these types of members:</span></span>

-   [<span data-ttu-id="4d7ea-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4d7ea-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d7ea-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4d7ea-114">Properties</span></span>

<span data-ttu-id="4d7ea-115">Класс **MDM \_ виндовсадванцедсреатпротектион \_ DeviceTagging01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4d7ea-115">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4d7ea-116">Степень важности</span><span class="sxs-lookup"><span data-stu-id="4d7ea-116">Criticality</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d7ea-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4d7ea-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d7ea-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4d7ea-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4d7ea-119">Группа</span><span class="sxs-lookup"><span data-stu-id="4d7ea-119">Group</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d7ea-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4d7ea-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d7ea-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4d7ea-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4d7ea-122">**идмесод**</span><span class="sxs-lookup"><span data-stu-id="4d7ea-122">**IdMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d7ea-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4d7ea-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d7ea-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4d7ea-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d7ea-125">TBD</span><span class="sxs-lookup"><span data-stu-id="4d7ea-125">TBD</span></span>

</dd> <dt>

<span data-ttu-id="4d7ea-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4d7ea-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d7ea-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4d7ea-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d7ea-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4d7ea-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d7ea-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4d7ea-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4d7ea-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4d7ea-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d7ea-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4d7ea-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d7ea-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4d7ea-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d7ea-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4d7ea-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d7ea-134">Требования</span><span class="sxs-lookup"><span data-stu-id="4d7ea-134">Requirements</span></span>



| <span data-ttu-id="4d7ea-135">Требование</span><span class="sxs-lookup"><span data-stu-id="4d7ea-135">Requirement</span></span> | <span data-ttu-id="4d7ea-136">Значение</span><span class="sxs-lookup"><span data-stu-id="4d7ea-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7ea-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d7ea-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4d7ea-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4d7ea-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4d7ea-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d7ea-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4d7ea-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4d7ea-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="4d7ea-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4d7ea-141">Namespace</span></span><br/>                | <span data-ttu-id="4d7ea-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="4d7ea-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="4d7ea-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4d7ea-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d7ea-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ea-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d7ea-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4d7ea-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d7ea-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ea-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

