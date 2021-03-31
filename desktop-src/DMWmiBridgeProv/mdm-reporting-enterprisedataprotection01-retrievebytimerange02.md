---
title: Класс MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
description: Класс MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 используется для получения журналов, существующих в параметрах StartTime и StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- Класс MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071155"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a><span data-ttu-id="4856a-105">\_ \_ Класс EnterpriseDataProtection01 RETRIEVEBYTIMERANGE02 отчетов MDM \_</span><span class="sxs-lookup"><span data-stu-id="4856a-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="4856a-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4856a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4856a-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4856a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4856a-108">Класс **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** используется для получения журналов, существующих в параметрах StartTime и StopTime.</span><span class="sxs-lookup"><span data-stu-id="4856a-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.</span></span> <span data-ttu-id="4856a-109">Время StartTime и StopTime выражаются в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="4856a-109">The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="4856a-110">Если параметры StartTime и StopTime не указаны, то значения будут интерпретированы как первое существующее или последнее существующее время.</span><span class="sxs-lookup"><span data-stu-id="4856a-110">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="4856a-111">Ниже приведены другие возможные сценарии.</span><span class="sxs-lookup"><span data-stu-id="4856a-111">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="4856a-112">Если параметр StartTime и StopTime не указаны, то возвращаются все существующие журналы.</span><span class="sxs-lookup"><span data-stu-id="4856a-112">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="4856a-113">Если указан параметр StopTime, но параметр StartTime не указан, то возвращаются все журналы, которые существовали до StopTime.</span><span class="sxs-lookup"><span data-stu-id="4856a-113">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="4856a-114">Если задан параметр StartTime, но StopTime не указан, возвращаются все журналы, существующие из StartTime.</span><span class="sxs-lookup"><span data-stu-id="4856a-114">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="4856a-115">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4856a-115">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4856a-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4856a-116">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="4856a-117">Члены</span><span class="sxs-lookup"><span data-stu-id="4856a-117">Members</span></span>

<span data-ttu-id="4856a-118">Класс **\_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 для MDM Reporting** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4856a-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="4856a-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="4856a-119">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4856a-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="4856a-120">Properties</span></span>

<span data-ttu-id="4856a-121">Класс **\_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 для MDM Reporting** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4856a-121">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4856a-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4856a-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4856a-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4856a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4856a-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4856a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4856a-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4856a-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4856a-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="4856a-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="4856a-127">Для этого класса строка имеет значение "Ретриевебитимеранже".</span><span class="sxs-lookup"><span data-stu-id="4856a-127">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="4856a-128">Журналы</span><span class="sxs-lookup"><span data-stu-id="4856a-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4856a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4856a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4856a-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4856a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4856a-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4856a-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4856a-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4856a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4856a-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4856a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4856a-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4856a-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4856a-135">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="4856a-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="4856a-136">Для этого класса строка имеет значение "./вендор/мсфт/ентерприседатапротектион"</span><span class="sxs-lookup"><span data-stu-id="4856a-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="4856a-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="4856a-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4856a-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4856a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4856a-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4856a-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4856a-140">StopTime</span><span class="sxs-lookup"><span data-stu-id="4856a-140">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4856a-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4856a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4856a-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4856a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4856a-143">Тип</span><span class="sxs-lookup"><span data-stu-id="4856a-143">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4856a-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4856a-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4856a-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4856a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4856a-146">Требования</span><span class="sxs-lookup"><span data-stu-id="4856a-146">Requirements</span></span>



| <span data-ttu-id="4856a-147">Требование</span><span class="sxs-lookup"><span data-stu-id="4856a-147">Requirement</span></span> | <span data-ttu-id="4856a-148">Значение</span><span class="sxs-lookup"><span data-stu-id="4856a-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4856a-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4856a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4856a-150">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4856a-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4856a-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4856a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4856a-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4856a-152">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="4856a-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4856a-153">Namespace</span></span><br/>                | <span data-ttu-id="4856a-154">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="4856a-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="4856a-155">MOF</span><span class="sxs-lookup"><span data-stu-id="4856a-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4856a-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4856a-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="4856a-157">DLL</span><span class="sxs-lookup"><span data-stu-id="4856a-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4856a-158"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4856a-158"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

