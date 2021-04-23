---
title: Класс MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
description: Класс MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02 используется для получения журналов, существующих в параметрах StartTime и StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- Класс MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801198"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a><span data-ttu-id="1588f-105">\_ \_ Класс SecurityAuditing01 RETRIEVEBYTIMERANGE02 отчетов MDM \_</span><span class="sxs-lookup"><span data-stu-id="1588f-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="1588f-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1588f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1588f-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1588f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1588f-108">Класс **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** используется для получения журналов, существующих в параметре StartTime и StopTime. значение StartTime и StopTime выражается в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="1588f-108">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="1588f-109">Если параметры StartTime и StopTime не указаны, то значения будут интерпретированы как первое существующее или последнее существующее время.</span><span class="sxs-lookup"><span data-stu-id="1588f-109">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="1588f-110">Ниже приведены другие возможные сценарии.</span><span class="sxs-lookup"><span data-stu-id="1588f-110">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="1588f-111">Если параметр StartTime и StopTime не указаны, то возвращаются все существующие журналы.</span><span class="sxs-lookup"><span data-stu-id="1588f-111">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="1588f-112">Если указан параметр StopTime, но параметр StartTime не указан, то возвращаются все журналы, которые существовали до StopTime.</span><span class="sxs-lookup"><span data-stu-id="1588f-112">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="1588f-113">Если задан параметр StartTime, но StopTime не указан, возвращаются все журналы, существующие из StartTime.</span><span class="sxs-lookup"><span data-stu-id="1588f-113">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="1588f-114">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1588f-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1588f-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1588f-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a><span data-ttu-id="1588f-116">Члены</span><span class="sxs-lookup"><span data-stu-id="1588f-116">Members</span></span>

<span data-ttu-id="1588f-117">Класс **\_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 для MDM Reporting** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1588f-117">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="1588f-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="1588f-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1588f-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="1588f-119">Properties</span></span>

<span data-ttu-id="1588f-120">Класс **\_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 для MDM Reporting** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1588f-120">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1588f-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1588f-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1588f-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1588f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1588f-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1588f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1588f-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1588f-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1588f-125">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="1588f-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="1588f-126">Для этого класса строка имеет значение "Ретриевебитимеранже".</span><span class="sxs-lookup"><span data-stu-id="1588f-126">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="1588f-127">Журналы</span><span class="sxs-lookup"><span data-stu-id="1588f-127">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1588f-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1588f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1588f-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1588f-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1588f-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1588f-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1588f-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1588f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1588f-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1588f-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1588f-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1588f-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1588f-134">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="1588f-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="1588f-135">Для этого класса строка имеет значение "./вендор/мсфт/секуритяудитинг"</span><span class="sxs-lookup"><span data-stu-id="1588f-135">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="1588f-136">StartTime</span><span class="sxs-lookup"><span data-stu-id="1588f-136">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1588f-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1588f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1588f-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1588f-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1588f-139">StopTime</span><span class="sxs-lookup"><span data-stu-id="1588f-139">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1588f-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1588f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1588f-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1588f-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1588f-142">Требования</span><span class="sxs-lookup"><span data-stu-id="1588f-142">Requirements</span></span>



| <span data-ttu-id="1588f-143">Требование</span><span class="sxs-lookup"><span data-stu-id="1588f-143">Requirement</span></span> | <span data-ttu-id="1588f-144">Значение</span><span class="sxs-lookup"><span data-stu-id="1588f-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1588f-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1588f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1588f-146">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1588f-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1588f-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1588f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1588f-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1588f-148">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="1588f-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1588f-149">Namespace</span></span><br/>                | <span data-ttu-id="1588f-150">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1588f-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="1588f-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1588f-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1588f-152"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1588f-152"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="1588f-153">DLL</span><span class="sxs-lookup"><span data-stu-id="1588f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1588f-154"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1588f-154"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

