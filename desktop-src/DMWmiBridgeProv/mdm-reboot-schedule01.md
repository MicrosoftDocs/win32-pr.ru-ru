---
title: Класс MDM_Reboot_Schedule01
description: '\_Schedule01class rereboot MDM \_ используется для настройки определенного времени для перезагрузки устройства.'
ms.assetid: d865609a-9f17-4256-9c69-4fea75011c1f
keywords:
- Класс MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01 класс, описание
topic_type:
- apiref
api_name:
- MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01.InstanceID
- MDM_Reboot_Schedule01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229aca469ee83d9ac2e4b29f6d6b7c54875120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489183"
---
# <a name="mdm_reboot_schedule01-class"></a><span data-ttu-id="54def-105">\_Класс Schedule01 rereboot MDM \_</span><span class="sxs-lookup"><span data-stu-id="54def-105">MDM\_Reboot\_Schedule01 class</span></span>

<span data-ttu-id="54def-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="54def-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="54def-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="54def-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="54def-108">Класс **\_ \_ Schedule01 rereboot MDM** используется для настройки определенного времени для перезагрузки устройства.</span><span class="sxs-lookup"><span data-stu-id="54def-108">The **MDM\_Reboot\_Schedule01** class is used to configure a specific time for the reboot of a device.</span></span>

<span data-ttu-id="54def-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="54def-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="54def-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54def-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot_Schedule01
{
  string InstanceID;
  string ParentID;
  string Single;
  string DailyRecurrent;
};
```

## <a name="members"></a><span data-ttu-id="54def-111">Члены</span><span class="sxs-lookup"><span data-stu-id="54def-111">Members</span></span>

<span data-ttu-id="54def-112">Класс **\_ \_ Schedule01 rereboot MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="54def-112">The **MDM\_Reboot\_Schedule01** class has these types of members:</span></span>

-   [<span data-ttu-id="54def-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="54def-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54def-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="54def-114">Properties</span></span>

<span data-ttu-id="54def-115">Класс **\_ \_ Schedule01 rereboot MDM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="54def-115">The **MDM\_Reboot\_Schedule01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="54def-116">даилирекуррент</span><span class="sxs-lookup"><span data-stu-id="54def-116">DailyRecurrent</span></span>](/windows/client-management/mdm/reboot-csp#schedule-dailyrecurrent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54def-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54def-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54def-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="54def-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="54def-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="54def-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54def-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54def-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54def-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54def-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54def-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54def-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54def-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="54def-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="54def-124">Для этого класса строка имеет значение "Schedule".</span><span class="sxs-lookup"><span data-stu-id="54def-124">For this class, the string is "Schedule".</span></span>

</dd> <dt>

<span data-ttu-id="54def-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="54def-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54def-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54def-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54def-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54def-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54def-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54def-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54def-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="54def-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="54def-130">Для этого класса строка имеет значение "./вендор/мсфт/ребут"</span><span class="sxs-lookup"><span data-stu-id="54def-130">For this class, the string is "./Vendor/MSFT/Reboot"</span></span>

</dd> <dt>

[<span data-ttu-id="54def-131">Single</span><span class="sxs-lookup"><span data-stu-id="54def-131">Single</span></span>](/windows/client-management/mdm/reboot-csp#schedule-single)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54def-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54def-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54def-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="54def-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54def-134">Требования</span><span class="sxs-lookup"><span data-stu-id="54def-134">Requirements</span></span>



| <span data-ttu-id="54def-135">Требование</span><span class="sxs-lookup"><span data-stu-id="54def-135">Requirement</span></span> | <span data-ttu-id="54def-136">Значение</span><span class="sxs-lookup"><span data-stu-id="54def-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54def-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54def-137">Minimum supported client</span></span><br/> | <span data-ttu-id="54def-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="54def-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="54def-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54def-139">Minimum supported server</span></span><br/> | <span data-ttu-id="54def-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="54def-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="54def-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="54def-141">Namespace</span></span><br/>                | <span data-ttu-id="54def-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="54def-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="54def-143">MOF</span><span class="sxs-lookup"><span data-stu-id="54def-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54def-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54def-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="54def-145">DLL</span><span class="sxs-lookup"><span data-stu-id="54def-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54def-146"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54def-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

