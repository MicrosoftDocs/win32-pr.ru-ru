---
title: Класс MDM_Policy_Config01_WindowsLogon02
description: '\_Класс политики MDM \_ Config01 \_ WindowsLogon02 настраивает экран блокировки и пользовательский интерфейс сети при входе.'
ms.assetid: eb155cf8-628d-4325-8b39-f193733d4c87
keywords:
- Класс MDM_Policy_Config01_WindowsLogon02
- MDM_Policy_Config01_WindowsLogon02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsLogon02
- MDM_Policy_Config01_WindowsLogon02.InstanceID
- MDM_Policy_Config01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf723729f8b90974b1ecaf5a0d8ee08eba0a3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891993"
---
# <a name="mdm_policy_config01_windowslogon02-class"></a><span data-ttu-id="38886-105">\_Класс политики MDM \_ Config01 \_ WindowsLogon02</span><span class="sxs-lookup"><span data-stu-id="38886-105">MDM\_Policy\_Config01\_WindowsLogon02 class</span></span>

<span data-ttu-id="38886-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="38886-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="38886-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="38886-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="38886-108">\_Класс политики MDM \_ Config01 \_ WindowsLogon02 настраивает экран блокировки и пользовательский интерфейс сети при входе.</span><span class="sxs-lookup"><span data-stu-id="38886-108">The MDM\_Policy\_Config01\_WindowsLogon02 class configures the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="38886-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="38886-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38886-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38886-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="38886-111">Члены</span><span class="sxs-lookup"><span data-stu-id="38886-111">Members</span></span>

<span data-ttu-id="38886-112">Класс **\_ политики MDM \_ Config01 \_ WindowsLogon02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38886-112">The **MDM\_Policy\_Config01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="38886-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="38886-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38886-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="38886-114">Properties</span></span>

<span data-ttu-id="38886-115">Класс **\_ политики MDM \_ Config01 \_ WindowsLogon02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38886-115">The **MDM\_Policy\_Config01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="38886-116">дисаблелоккскринаппнотификатионс</span><span class="sxs-lookup"><span data-stu-id="38886-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="38886-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38886-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38886-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="38886-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="38886-119">донтдисплайнетворкселектионуи</span><span class="sxs-lookup"><span data-stu-id="38886-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="38886-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38886-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38886-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="38886-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="38886-122">HideFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="38886-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="38886-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="38886-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="38886-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="38886-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="38886-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="38886-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38886-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38886-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38886-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38886-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38886-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="38886-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="38886-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="38886-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38886-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38886-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38886-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38886-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38886-132">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="38886-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38886-133">Требования</span><span class="sxs-lookup"><span data-stu-id="38886-133">Requirements</span></span>



| <span data-ttu-id="38886-134">Требование</span><span class="sxs-lookup"><span data-stu-id="38886-134">Requirement</span></span> | <span data-ttu-id="38886-135">Значение</span><span class="sxs-lookup"><span data-stu-id="38886-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38886-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38886-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38886-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="38886-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38886-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38886-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38886-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="38886-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="38886-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38886-140">Namespace</span></span><br/>                | <span data-ttu-id="38886-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="38886-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="38886-142">MOF</span><span class="sxs-lookup"><span data-stu-id="38886-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38886-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38886-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="38886-144">DLL</span><span class="sxs-lookup"><span data-stu-id="38886-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38886-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38886-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

