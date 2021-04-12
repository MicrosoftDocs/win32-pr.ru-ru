---
title: Класс MDM_Policy_User_Result01_Education02
description: '\_ \_ \_ Класс User RESULT01 Education02 политики MDM \_ представляет политики образования.'
ms.assetid: 34dcc478-5f39-4e1a-908b-46cbbf2ff4fd
keywords:
- Класс MDM_Policy_User_Result01_Education02
- MDM_Policy_User_Result01_Education02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Education02
- MDM_Policy_User_Result01_Education02.InstanceID
- MDM_Policy_User_Result01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce82ae1131287ec04c77e084e822609a0e0ab07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415596"
---
# <a name="mdm_policy_user_result01_education02-class"></a><span data-ttu-id="0bdcb-105">\_Класс политики MDM \_ user \_ Result01 \_ Education02</span><span class="sxs-lookup"><span data-stu-id="0bdcb-105">MDM\_Policy\_User\_Result01\_Education02 class</span></span>

<span data-ttu-id="0bdcb-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="0bdcb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0bdcb-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="0bdcb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0bdcb-108">\_ \_ \_ Класс User RESULT01 Education02 политики MDM \_ представляет политики образования.</span><span class="sxs-lookup"><span data-stu-id="0bdcb-108">The MDM\_Policy\_User\_Result01\_Education02 class represents the education policies.</span></span>

<span data-ttu-id="0bdcb-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0bdcb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bdcb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bdcb-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="0bdcb-111">Члены</span><span class="sxs-lookup"><span data-stu-id="0bdcb-111">Members</span></span>

<span data-ttu-id="0bdcb-112">Класс **\_ \_ user \_ Result01 \_ Education02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0bdcb-112">The **MDM\_Policy\_User\_Result01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="0bdcb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0bdcb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bdcb-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0bdcb-114">Properties</span></span>

<span data-ttu-id="0bdcb-115">Класс **\_ \_ user \_ Result01 \_ Education02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="0bdcb-115">The **MDM\_Policy\_User\_Result01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0bdcb-116">дефаултпринтернаме</span><span class="sxs-lookup"><span data-stu-id="0bdcb-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bdcb-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0bdcb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bdcb-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0bdcb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0bdcb-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0bdcb-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bdcb-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0bdcb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bdcb-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0bdcb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bdcb-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0bdcb-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0bdcb-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0bdcb-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bdcb-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0bdcb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bdcb-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0bdcb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bdcb-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0bdcb-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0bdcb-127">превентаддингневпринтерс</span><span class="sxs-lookup"><span data-stu-id="0bdcb-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bdcb-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0bdcb-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bdcb-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0bdcb-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0bdcb-130">принтернамес</span><span class="sxs-lookup"><span data-stu-id="0bdcb-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bdcb-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0bdcb-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bdcb-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0bdcb-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bdcb-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0bdcb-133">Requirements</span></span>



| <span data-ttu-id="0bdcb-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0bdcb-134">Requirement</span></span> | <span data-ttu-id="0bdcb-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0bdcb-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bdcb-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bdcb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0bdcb-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0bdcb-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0bdcb-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bdcb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0bdcb-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0bdcb-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0bdcb-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0bdcb-140">Namespace</span></span><br/>                | <span data-ttu-id="0bdcb-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="0bdcb-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0bdcb-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0bdcb-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bdcb-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bdcb-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bdcb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0bdcb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bdcb-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bdcb-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

