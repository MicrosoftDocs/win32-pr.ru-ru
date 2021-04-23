---
title: Класс MDM_Policy_Config01_SmartScreen02
description: '\_Класс политики MDM \_ Config01 \_ SmartScreen02 настраивает политики интеллектуального экрана.'
ms.assetid: e5ad04a1-afa9-4887-a4c1-c92c574a5398
keywords:
- Класс MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02.InstanceID
- MDM_Policy_Config01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e0b8ca0c1e53005ab2a2ab80cce3f18dec40b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071676"
---
# <a name="mdm_policy_config01_smartscreen02-class"></a><span data-ttu-id="1c366-105">\_Класс политики MDM \_ Config01 \_ SmartScreen02</span><span class="sxs-lookup"><span data-stu-id="1c366-105">MDM\_Policy\_Config01\_SmartScreen02 class</span></span>

<span data-ttu-id="1c366-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1c366-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1c366-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1c366-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1c366-108">\_Класс политики MDM \_ Config01 \_ SmartScreen02 настраивает политики интеллектуального экрана.</span><span class="sxs-lookup"><span data-stu-id="1c366-108">The MDM\_Policy\_Config01\_SmartScreen02 class configures the smart screen policies.</span></span>

<span data-ttu-id="1c366-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1c366-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c366-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c366-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a><span data-ttu-id="1c366-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1c366-111">Members</span></span>

<span data-ttu-id="1c366-112">Класс **\_ политики MDM \_ Config01 \_ SmartScreen02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c366-112">The **MDM\_Policy\_Config01\_SmartScreen02** class has these types of members:</span></span>

-   [<span data-ttu-id="1c366-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c366-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c366-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c366-114">Properties</span></span>

<span data-ttu-id="1c366-115">Класс **\_ политики MDM \_ Config01 \_ SmartScreen02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c366-115">The **MDM\_Policy\_Config01\_SmartScreen02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1c366-116">EnableAppInstallControl</span><span class="sxs-lookup"><span data-stu-id="1c366-116">EnableAppInstallControl</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c366-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1c366-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c366-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1c366-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c366-119">EnableSmartScreenInShell</span><span class="sxs-lookup"><span data-stu-id="1c366-119">EnableSmartScreenInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c366-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1c366-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c366-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1c366-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c366-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1c366-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c366-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c366-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c366-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c366-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c366-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c366-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c366-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1c366-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c366-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c366-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c366-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c366-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c366-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c366-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c366-130">PreventOverrideForFilesInShell</span><span class="sxs-lookup"><span data-stu-id="1c366-130">PreventOverrideForFilesInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c366-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1c366-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c366-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1c366-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c366-133">Требования</span><span class="sxs-lookup"><span data-stu-id="1c366-133">Requirements</span></span>



| <span data-ttu-id="1c366-134">Требование</span><span class="sxs-lookup"><span data-stu-id="1c366-134">Requirement</span></span> | <span data-ttu-id="1c366-135">Значение</span><span class="sxs-lookup"><span data-stu-id="1c366-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c366-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c366-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1c366-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1c366-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c366-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c366-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1c366-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c366-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1c366-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c366-140">Namespace</span></span><br/>                | <span data-ttu-id="1c366-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1c366-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1c366-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1c366-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c366-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c366-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c366-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1c366-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c366-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c366-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

