---
title: Класс MDM_Policy_Config01_DataProtection02
description: '\_Класс политики MDM \_ Config01 \_ DataProtection02 представляет доступные политики защиты данных.'
ms.assetid: 54750bae-ee5d-4db9-896f-28d9550c4d5d
keywords:
- Класс MDM_Policy_Config01_DataProtection02
- MDM_Policy_Config01_DataProtection02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DataProtection02
- MDM_Policy_Config01_DataProtection02.InstanceID
- MDM_Policy_Config01_DataProtection02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692dfd675c07ddc7eebbfcd75e09cb521126c746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989222"
---
# <a name="mdm_policy_config01_dataprotection02-class"></a><span data-ttu-id="5cabb-105">\_Класс политики MDM \_ Config01 \_ DataProtection02</span><span class="sxs-lookup"><span data-stu-id="5cabb-105">MDM\_Policy\_Config01\_DataProtection02 class</span></span>

<span data-ttu-id="5cabb-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="5cabb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5cabb-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="5cabb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5cabb-108">Класс **\_ политики MDM \_ Config01 \_ DataProtection02** представляет доступные политики защиты данных.</span><span class="sxs-lookup"><span data-stu-id="5cabb-108">The **MDM\_Policy\_Config01\_DataProtection02** class represents the data protection policies available.</span></span>

<span data-ttu-id="5cabb-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5cabb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cabb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cabb-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DataProtection02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDirectMemoryAccess;
  string LegacySelectiveWipeID;
};
```

## <a name="members"></a><span data-ttu-id="5cabb-111">Члены</span><span class="sxs-lookup"><span data-stu-id="5cabb-111">Members</span></span>

<span data-ttu-id="5cabb-112">Класс **\_ политики MDM \_ Config01 \_ DataProtection02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5cabb-112">The **MDM\_Policy\_Config01\_DataProtection02** class has these types of members:</span></span>

-   [<span data-ttu-id="5cabb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5cabb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5cabb-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5cabb-114">Properties</span></span>

<span data-ttu-id="5cabb-115">Класс **\_ политики MDM \_ Config01 \_ DataProtection02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5cabb-115">The **MDM\_Policy\_Config01\_DataProtection02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5cabb-116">алловдиректмеморякцесс</span><span class="sxs-lookup"><span data-stu-id="5cabb-116">AllowDirectMemoryAccess</span></span>](/windows/client-management/mdm/policy-csp-dataprotection#dataprotection-allowdirectmemoryaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cabb-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5cabb-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5cabb-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5cabb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5cabb-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5cabb-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cabb-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5cabb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cabb-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5cabb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cabb-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5cabb-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5cabb-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="5cabb-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="5cabb-124">Для этого класса строка имеет значение "Защита".</span><span class="sxs-lookup"><span data-stu-id="5cabb-124">For this class, the string is "DataProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="5cabb-125">легациселективевипеид</span><span class="sxs-lookup"><span data-stu-id="5cabb-125">LegacySelectiveWipeID</span></span>](/windows/client-management/mdm/policy-csp-dataprotection#dataprotection-legacyselectivewipeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cabb-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5cabb-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cabb-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5cabb-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5cabb-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5cabb-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cabb-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5cabb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cabb-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5cabb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cabb-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5cabb-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5cabb-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="5cabb-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="5cabb-133">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="5cabb-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5cabb-134">Требования</span><span class="sxs-lookup"><span data-stu-id="5cabb-134">Requirements</span></span>



| <span data-ttu-id="5cabb-135">Требование</span><span class="sxs-lookup"><span data-stu-id="5cabb-135">Requirement</span></span> | <span data-ttu-id="5cabb-136">Значение</span><span class="sxs-lookup"><span data-stu-id="5cabb-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cabb-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cabb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5cabb-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5cabb-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5cabb-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5cabb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5cabb-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5cabb-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5cabb-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5cabb-141">Namespace</span></span><br/>                | <span data-ttu-id="5cabb-142">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="5cabb-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5cabb-143">MOF</span><span class="sxs-lookup"><span data-stu-id="5cabb-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cabb-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5cabb-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cabb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5cabb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cabb-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cabb-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cabb-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cabb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cabb-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="5cabb-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

