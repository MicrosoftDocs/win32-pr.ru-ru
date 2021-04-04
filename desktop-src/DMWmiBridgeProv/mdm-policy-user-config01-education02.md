---
title: Класс MDM_Policy_User_Config01_Education02
description: '\_Класс политики MDM \_ user \_ Config01 \_ Education02 настраивает политики образования.'
ms.assetid: d9a263c7-ee9c-4857-b9a6-f0efdb373e13
keywords:
- Класс MDM_Policy_User_Config01_Education02
- MDM_Policy_User_Config01_Education02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Education02
- MDM_Policy_User_Config01_Education02.InstanceID
- MDM_Policy_User_Config01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ae8508668b95edce1d4c4a2d0e99cbba2bc6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988362"
---
# <a name="mdm_policy_user_config01_education02-class"></a><span data-ttu-id="217b2-105">\_Класс политики MDM \_ user \_ Config01 \_ Education02</span><span class="sxs-lookup"><span data-stu-id="217b2-105">MDM\_Policy\_User\_Config01\_Education02 class</span></span>

<span data-ttu-id="217b2-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="217b2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="217b2-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="217b2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="217b2-108">\_Класс политики MDM \_ user \_ Config01 \_ Education02 настраивает политики образования.</span><span class="sxs-lookup"><span data-stu-id="217b2-108">The MDM\_Policy\_User\_Config01\_Education02 class configures the education policies.</span></span>

<span data-ttu-id="217b2-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="217b2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="217b2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="217b2-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="217b2-111">Члены</span><span class="sxs-lookup"><span data-stu-id="217b2-111">Members</span></span>

<span data-ttu-id="217b2-112">Класс **\_ \_ user \_ Config01 \_ Education02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="217b2-112">The **MDM\_Policy\_User\_Config01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="217b2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="217b2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="217b2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="217b2-114">Properties</span></span>

<span data-ttu-id="217b2-115">Класс **\_ \_ user \_ Config01 \_ Education02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="217b2-115">The **MDM\_Policy\_User\_Config01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="217b2-116">дефаултпринтернаме</span><span class="sxs-lookup"><span data-stu-id="217b2-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="217b2-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="217b2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="217b2-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="217b2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="217b2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="217b2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="217b2-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="217b2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="217b2-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="217b2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="217b2-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="217b2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="217b2-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="217b2-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="217b2-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="217b2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="217b2-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="217b2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="217b2-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="217b2-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="217b2-127">превентаддингневпринтерс</span><span class="sxs-lookup"><span data-stu-id="217b2-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="217b2-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="217b2-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="217b2-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="217b2-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="217b2-130">принтернамес</span><span class="sxs-lookup"><span data-stu-id="217b2-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="217b2-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="217b2-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="217b2-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="217b2-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="217b2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="217b2-133">Requirements</span></span>



| <span data-ttu-id="217b2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="217b2-134">Requirement</span></span> | <span data-ttu-id="217b2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="217b2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217b2-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="217b2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="217b2-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="217b2-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="217b2-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="217b2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="217b2-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="217b2-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="217b2-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="217b2-140">Namespace</span></span><br/>                | <span data-ttu-id="217b2-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="217b2-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="217b2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="217b2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="217b2-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="217b2-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="217b2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="217b2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="217b2-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="217b2-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

