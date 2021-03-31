---
title: Класс MDM_Reporting_SecurityAuditing01_RetrieveByCount02
description: Класс MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByCount02 используется для получения указанного числа журналов из StartTime.
ms.assetid: dfa50c04-99d6-4f6a-90ff-70a829bd317d
keywords:
- Класс MDM_Reporting_SecurityAuditing01_RetrieveByCount02
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c979d25cdc9887a500307494218a6fc11f98bf86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801199"
---
# <a name="mdm_reporting_securityauditing01_retrievebycount02-class"></a><span data-ttu-id="465a5-105">\_ \_ Класс SecurityAuditing01 RETRIEVEBYCOUNT02 отчетов MDM \_</span><span class="sxs-lookup"><span data-stu-id="465a5-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="465a5-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="465a5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="465a5-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="465a5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="465a5-108">Класс [**MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByCount02**](mdm-reporting-enterprisedataprotection01-retrievebycount02.md) используется для получения указанного числа журналов из StartTime.</span><span class="sxs-lookup"><span data-stu-id="465a5-108">The [**MDM\_Reporting\_SecurityAuditing01\_RetrieveByCount02**](mdm-reporting-enterprisedataprotection01-retrievebycount02.md) class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="465a5-109">Время начала выражается в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="465a5-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="465a5-110">Можно задать количество журналов, необходимых для установки Логкаунт и StartTime.</span><span class="sxs-lookup"><span data-stu-id="465a5-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="465a5-111">Он возвращает указанное число журналов или меньше, если общее число журналов меньше Логкаунт.</span><span class="sxs-lookup"><span data-stu-id="465a5-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="465a5-112">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="465a5-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="465a5-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="465a5-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
};
```

## <a name="members"></a><span data-ttu-id="465a5-114">Члены</span><span class="sxs-lookup"><span data-stu-id="465a5-114">Members</span></span>

<span data-ttu-id="465a5-115">Класс **\_ \_ SecurityAuditing01 \_ RetrieveByCount02 для MDM Reporting** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="465a5-115">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="465a5-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="465a5-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="465a5-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="465a5-117">Properties</span></span>

<span data-ttu-id="465a5-118">Класс **\_ \_ SecurityAuditing01 \_ RetrieveByCount02 для MDM Reporting** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="465a5-118">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="465a5-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="465a5-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="465a5-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="465a5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="465a5-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="465a5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="465a5-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="465a5-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="465a5-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="465a5-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="465a5-124">Для этого класса строка имеет значение "Ретриевебикаунт".</span><span class="sxs-lookup"><span data-stu-id="465a5-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="465a5-125">логкаунт</span><span class="sxs-lookup"><span data-stu-id="465a5-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="465a5-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="465a5-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="465a5-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="465a5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="465a5-128">Журналы</span><span class="sxs-lookup"><span data-stu-id="465a5-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="465a5-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="465a5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="465a5-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="465a5-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="465a5-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="465a5-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="465a5-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="465a5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="465a5-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="465a5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="465a5-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="465a5-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="465a5-135">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="465a5-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="465a5-136">Для этого класса строка имеет значение "./вендор/мсфт/секуритяудитинг"</span><span class="sxs-lookup"><span data-stu-id="465a5-136">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="465a5-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="465a5-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="465a5-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="465a5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="465a5-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="465a5-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="465a5-140">Требования</span><span class="sxs-lookup"><span data-stu-id="465a5-140">Requirements</span></span>



| <span data-ttu-id="465a5-141">Требование</span><span class="sxs-lookup"><span data-stu-id="465a5-141">Requirement</span></span> | <span data-ttu-id="465a5-142">Значение</span><span class="sxs-lookup"><span data-stu-id="465a5-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="465a5-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="465a5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="465a5-144">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="465a5-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="465a5-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="465a5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="465a5-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="465a5-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="465a5-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="465a5-147">Namespace</span></span><br/>                | <span data-ttu-id="465a5-148">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="465a5-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="465a5-149">MOF</span><span class="sxs-lookup"><span data-stu-id="465a5-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="465a5-150"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="465a5-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="465a5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="465a5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="465a5-152"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="465a5-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

