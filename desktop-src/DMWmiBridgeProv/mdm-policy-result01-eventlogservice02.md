---
title: Класс MDM_Policy_Result01_EventLogService02
description: '\_Класс политики MDM \_ Result01 \_ EventLogService02 представляет поведение журнала событий.'
ms.assetid: 6d4908e9-d283-486a-8309-57d5c5ec83d0
keywords:
- Класс MDM_Policy_Result01_EventLogService02
- MDM_Policy_Result01_EventLogService02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_EventLogService02
- MDM_Policy_Result01_EventLogService02.InstanceID
- MDM_Policy_Result01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914a00c3646490e5d4679579aab7a38474a34f00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490797"
---
# <a name="mdm_policy_result01_eventlogservice02-class"></a><span data-ttu-id="8f389-105">\_Класс политики MDM \_ Result01 \_ EventLogService02</span><span class="sxs-lookup"><span data-stu-id="8f389-105">MDM\_Policy\_Result01\_EventLogService02 class</span></span>

<span data-ttu-id="8f389-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8f389-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8f389-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8f389-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8f389-108">\_Класс политики MDM \_ Result01 \_ EventLogService02 представляет поведение журнала событий.</span><span class="sxs-lookup"><span data-stu-id="8f389-108">The MDM\_Policy\_Result01\_EventLogService02 class represents the event log behavior.</span></span>

<span data-ttu-id="8f389-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8f389-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f389-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f389-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="8f389-111">Члены</span><span class="sxs-lookup"><span data-stu-id="8f389-111">Members</span></span>

<span data-ttu-id="8f389-112">Класс **\_ политики MDM \_ Result01 \_ EventLogService02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8f389-112">The **MDM\_Policy\_Result01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="8f389-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f389-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f389-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f389-114">Properties</span></span>

<span data-ttu-id="8f389-115">Класс **\_ политики MDM \_ Result01 \_ EventLogService02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8f389-115">The **MDM\_Policy\_Result01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8f389-116">контролевентлогбехавиор</span><span class="sxs-lookup"><span data-stu-id="8f389-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f389-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f389-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f389-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8f389-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f389-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8f389-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f389-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f389-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f389-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f389-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f389-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8f389-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f389-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8f389-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f389-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f389-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f389-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f389-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f389-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8f389-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8f389-127">спеЦифимаксимумфилесизеаппликатионлог</span><span class="sxs-lookup"><span data-stu-id="8f389-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f389-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f389-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f389-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8f389-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8f389-130">спеЦифимаксимумфилесизесекуритилог</span><span class="sxs-lookup"><span data-stu-id="8f389-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f389-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f389-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f389-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8f389-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8f389-133">спеЦифимаксимумфилесизесистемлог</span><span class="sxs-lookup"><span data-stu-id="8f389-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f389-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f389-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f389-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8f389-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f389-136">Требования</span><span class="sxs-lookup"><span data-stu-id="8f389-136">Requirements</span></span>



| <span data-ttu-id="8f389-137">Требование</span><span class="sxs-lookup"><span data-stu-id="8f389-137">Requirement</span></span> | <span data-ttu-id="8f389-138">Значение</span><span class="sxs-lookup"><span data-stu-id="8f389-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f389-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f389-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8f389-140">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8f389-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f389-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f389-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8f389-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8f389-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8f389-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8f389-143">Namespace</span></span><br/>                | <span data-ttu-id="8f389-144">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="8f389-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8f389-145">MOF</span><span class="sxs-lookup"><span data-stu-id="8f389-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f389-146"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f389-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f389-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8f389-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f389-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f389-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

