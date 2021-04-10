---
title: Класс MDM_Policy_Result01_Cellular02
description: '\_класс политики MDM \_ Result01 \_ Cellular02 представляет политики сотовой сети.'
ms.assetid: df2b2461-5e4e-4b28-87f1-5ca348409192
keywords:
- Класс MDM_Policy_Result01_Cellular02
- MDM_Policy_Result01_Cellular02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Cellular02
- MDM_Policy_Result01_Cellular02.InstanceID
- MDM_Policy_Result01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2a8b9178ecd4d69b0c313eb7fdcb826e944317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135355"
---
# <a name="mdm_policy_result01_cellular02-class"></a><span data-ttu-id="cefcb-105">\_Класс политики MDM \_ Result01 \_ Cellular02</span><span class="sxs-lookup"><span data-stu-id="cefcb-105">MDM\_Policy\_Result01\_Cellular02 class</span></span>

<span data-ttu-id="cefcb-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="cefcb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cefcb-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="cefcb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cefcb-108">\_класс политики MDM \_ Result01 \_ Cellular02 представляет политики сотовой сети.</span><span class="sxs-lookup"><span data-stu-id="cefcb-108">the MDM\_Policy\_Result01\_Cellular02 class represents the cellular policies.</span></span>

<span data-ttu-id="cefcb-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cefcb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cefcb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cefcb-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Cellular02
{
  string InstanceID;
  string ParentID;
  string LetAppsAccessCellularData_UserInControlOfTheseApps;
  string LetAppsAccessCellularData_ForceDenyTheseApps;
  string LetAppsAccessCellularData_ForceAllowTheseApps;
  sint32 LetAppsAccessCellularData;
  string ShowAppCellularAccessUI;
};
```

## <a name="members"></a><span data-ttu-id="cefcb-111">Члены</span><span class="sxs-lookup"><span data-stu-id="cefcb-111">Members</span></span>

<span data-ttu-id="cefcb-112">Класс **\_ политики MDM \_ Result01 \_ Cellular02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cefcb-112">The **MDM\_Policy\_Result01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="cefcb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="cefcb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cefcb-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="cefcb-114">Properties</span></span>

<span data-ttu-id="cefcb-115">Класс **\_ политики MDM \_ Result01 \_ Cellular02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cefcb-115">The **MDM\_Policy\_Result01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cefcb-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cefcb-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cefcb-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cefcb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cefcb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cefcb-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cefcb-120">летаппсакцессцеллулардата</span><span class="sxs-lookup"><span data-stu-id="cefcb-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cefcb-121">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="cefcb-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cefcb-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cefcb-123">Летаппсакцессцеллулардата \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="cefcb-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cefcb-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cefcb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cefcb-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cefcb-126">Летаппсакцессцеллулардата \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="cefcb-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cefcb-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cefcb-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cefcb-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cefcb-129">Летаппсакцессцеллулардата \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="cefcb-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cefcb-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cefcb-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cefcb-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cefcb-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cefcb-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cefcb-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cefcb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cefcb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-135">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cefcb-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cefcb-136">шоваппцеллуларакцессуи</span><span class="sxs-lookup"><span data-stu-id="cefcb-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cefcb-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cefcb-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cefcb-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cefcb-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cefcb-139">Требования</span><span class="sxs-lookup"><span data-stu-id="cefcb-139">Requirements</span></span>



| <span data-ttu-id="cefcb-140">Требование</span><span class="sxs-lookup"><span data-stu-id="cefcb-140">Requirement</span></span> | <span data-ttu-id="cefcb-141">Значение</span><span class="sxs-lookup"><span data-stu-id="cefcb-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cefcb-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cefcb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cefcb-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cefcb-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cefcb-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cefcb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cefcb-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cefcb-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cefcb-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cefcb-146">Namespace</span></span><br/>                | <span data-ttu-id="cefcb-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="cefcb-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cefcb-148">MOF</span><span class="sxs-lookup"><span data-stu-id="cefcb-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cefcb-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cefcb-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cefcb-150">DLL</span><span class="sxs-lookup"><span data-stu-id="cefcb-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cefcb-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cefcb-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

