---
title: Класс MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
description: Класс MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02 используется для получения указанного числа журналов из StartTime.
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- Класс MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fcc6e7ed3ccb630b500179d7273bdd09a21477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489168"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a><span data-ttu-id="f2944-105">\_ \_ Класс EnterpriseDataProtection01 RETRIEVEBYCOUNT02 отчетов MDM \_</span><span class="sxs-lookup"><span data-stu-id="f2944-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="f2944-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f2944-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f2944-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f2944-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f2944-108">Класс **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02** используется для получения указанного числа журналов из StartTime.</span><span class="sxs-lookup"><span data-stu-id="f2944-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="f2944-109">Время начала выражается в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="f2944-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="f2944-110">Можно задать количество журналов, необходимых для установки Логкаунт и StartTime.</span><span class="sxs-lookup"><span data-stu-id="f2944-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="f2944-111">Он возвращает указанное число журналов или меньше, если общее число журналов меньше Логкаунт.</span><span class="sxs-lookup"><span data-stu-id="f2944-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="f2944-112">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f2944-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2944-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2944-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="f2944-114">Члены</span><span class="sxs-lookup"><span data-stu-id="f2944-114">Members</span></span>

<span data-ttu-id="f2944-115">Класс **\_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02 для MDM Reporting** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2944-115">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="f2944-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2944-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2944-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2944-117">Properties</span></span>

<span data-ttu-id="f2944-118">Класс **\_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02 для MDM Reporting** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f2944-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2944-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f2944-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2944-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2944-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2944-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2944-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2944-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2944-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2944-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f2944-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="f2944-124">Для этого класса строка имеет значение "Ретриевебикаунт".</span><span class="sxs-lookup"><span data-stu-id="f2944-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="f2944-125">логкаунт</span><span class="sxs-lookup"><span data-stu-id="f2944-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2944-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f2944-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2944-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2944-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2944-128">Журналы</span><span class="sxs-lookup"><span data-stu-id="f2944-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2944-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2944-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2944-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2944-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2944-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f2944-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2944-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2944-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2944-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2944-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2944-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2944-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2944-135">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f2944-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="f2944-136">Для этого класса строка имеет значение "./вендор/мсфт/ентерприседатапротектион"</span><span class="sxs-lookup"><span data-stu-id="f2944-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="f2944-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="f2944-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2944-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2944-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2944-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2944-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2944-140">Тип</span><span class="sxs-lookup"><span data-stu-id="f2944-140">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2944-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f2944-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2944-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2944-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2944-143">Требования</span><span class="sxs-lookup"><span data-stu-id="f2944-143">Requirements</span></span>



| <span data-ttu-id="f2944-144">Требование</span><span class="sxs-lookup"><span data-stu-id="f2944-144">Requirement</span></span> | <span data-ttu-id="f2944-145">Значение</span><span class="sxs-lookup"><span data-stu-id="f2944-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2944-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2944-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f2944-147">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f2944-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f2944-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2944-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f2944-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f2944-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="f2944-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2944-150">Namespace</span></span><br/>                | <span data-ttu-id="f2944-151">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f2944-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="f2944-152">MOF</span><span class="sxs-lookup"><span data-stu-id="f2944-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2944-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2944-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="f2944-154">DLL</span><span class="sxs-lookup"><span data-stu-id="f2944-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2944-155"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2944-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

