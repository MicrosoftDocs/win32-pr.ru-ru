---
title: Класс MDM_Policy_Config01_WindowsInkWorkspace02
description: '\_Класс политики MDM \_ Config01 \_ WindowsInkWorkspace02 представляет доступные политики рукописного ввода.'
ms.assetid: 676a459f-25b0-4cf7-bf64-635ac4a93f59
keywords:
- Класс MDM_Policy_Config01_WindowsInkWorkspace02
- MDM_Policy_Config01_WindowsInkWorkspace02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsInkWorkspace02
- MDM_Policy_Config01_WindowsInkWorkspace02.InstanceID
- MDM_Policy_Config01_WindowsInkWorkspace02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f654326b0a44ed40faa06dfe80d933dc2c52c4f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988718"
---
# <a name="mdm_policy_config01_windowsinkworkspace02-class"></a><span data-ttu-id="855e0-105">\_Класс политики MDM \_ Config01 \_ WindowsInkWorkspace02</span><span class="sxs-lookup"><span data-stu-id="855e0-105">MDM\_Policy\_Config01\_WindowsInkWorkspace02 class</span></span>

<span data-ttu-id="855e0-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="855e0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="855e0-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="855e0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="855e0-108">Класс **\_ политики MDM \_ Config01 \_ WindowsInkWorkspace02** представляет доступные политики рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="855e0-108">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class represents the ink workspace policies available.</span></span>

<span data-ttu-id="855e0-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="855e0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="855e0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="855e0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsInkWorkspace02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsInkWorkspace;
  sint32 AllowSuggestedAppsInWindowsInkWorkspace;
};
```

## <a name="members"></a><span data-ttu-id="855e0-111">Члены</span><span class="sxs-lookup"><span data-stu-id="855e0-111">Members</span></span>

<span data-ttu-id="855e0-112">Класс **\_ политики MDM \_ Config01 \_ WindowsInkWorkspace02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="855e0-112">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class has these types of members:</span></span>

-   [<span data-ttu-id="855e0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="855e0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="855e0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="855e0-114">Properties</span></span>

<span data-ttu-id="855e0-115">Класс **\_ политики MDM \_ Config01 \_ WindowsInkWorkspace02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="855e0-115">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="855e0-116">AllowSuggestedAppsInWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="855e0-116">AllowSuggestedAppsInWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowsuggestedappsinwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="855e0-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="855e0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="855e0-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="855e0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="855e0-119">AllowWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="855e0-119">AllowWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="855e0-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="855e0-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="855e0-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="855e0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="855e0-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="855e0-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="855e0-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="855e0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="855e0-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="855e0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="855e0-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="855e0-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="855e0-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="855e0-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="855e0-127">Для этого класса строка имеет значение "Виндовсинкворкспаце".</span><span class="sxs-lookup"><span data-stu-id="855e0-127">For this class, the string is "WindowsInkWorkspace".</span></span>

</dd> <dt>

<span data-ttu-id="855e0-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="855e0-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="855e0-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="855e0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="855e0-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="855e0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="855e0-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="855e0-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="855e0-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="855e0-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="855e0-133">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="855e0-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="855e0-134">Требования</span><span class="sxs-lookup"><span data-stu-id="855e0-134">Requirements</span></span>



| <span data-ttu-id="855e0-135">Требование</span><span class="sxs-lookup"><span data-stu-id="855e0-135">Requirement</span></span> | <span data-ttu-id="855e0-136">Значение</span><span class="sxs-lookup"><span data-stu-id="855e0-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="855e0-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="855e0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="855e0-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="855e0-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="855e0-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="855e0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="855e0-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="855e0-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="855e0-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="855e0-141">Namespace</span></span><br/>                | <span data-ttu-id="855e0-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="855e0-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="855e0-143">MOF</span><span class="sxs-lookup"><span data-stu-id="855e0-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="855e0-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="855e0-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="855e0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="855e0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="855e0-146"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="855e0-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

