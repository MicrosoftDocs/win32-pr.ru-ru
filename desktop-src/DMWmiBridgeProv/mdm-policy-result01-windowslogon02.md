---
title: Класс MDM_Policy_Result01_WindowsLogon02
description: '\_Класс политики MDM \_ Result01 \_ WindowsLogon02 получает параметры экрана блокировки и сетевого интерфейса пользователя при входе.'
ms.assetid: 4c710e3d-e7d5-4e6e-ad99-b3c7d1813599
keywords:
- Класс MDM_Policy_Result01_WindowsLogon02
- MDM_Policy_Result01_WindowsLogon02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsLogon02
- MDM_Policy_Result01_WindowsLogon02.InstanceID
- MDM_Policy_Result01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8e9c0e2ebc2e82d5daef174ce9322b5b4b5ec7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135202"
---
# <a name="mdm_policy_result01_windowslogon02-class"></a><span data-ttu-id="9bc06-105">\_Класс политики MDM \_ Result01 \_ WindowsLogon02</span><span class="sxs-lookup"><span data-stu-id="9bc06-105">MDM\_Policy\_Result01\_WindowsLogon02 class</span></span>

<span data-ttu-id="9bc06-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9bc06-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9bc06-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9bc06-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9bc06-108">\_Класс политики MDM \_ Result01 \_ WindowsLogon02 получает параметры экрана блокировки и сетевого интерфейса пользователя при входе.</span><span class="sxs-lookup"><span data-stu-id="9bc06-108">The MDM\_Policy\_Result01\_WindowsLogon02 class gets the settings of the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="9bc06-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9bc06-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc06-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bc06-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="9bc06-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9bc06-111">Members</span></span>

<span data-ttu-id="9bc06-112">Класс **\_ политики MDM \_ Result01 \_ WindowsLogon02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9bc06-112">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="9bc06-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bc06-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9bc06-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bc06-114">Properties</span></span>

<span data-ttu-id="9bc06-115">Класс **\_ политики MDM \_ Result01 \_ WindowsLogon02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9bc06-115">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9bc06-116">дисаблелоккскринаппнотификатионс</span><span class="sxs-lookup"><span data-stu-id="9bc06-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bc06-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bc06-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bc06-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bc06-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bc06-119">донтдисплайнетворкселектионуи</span><span class="sxs-lookup"><span data-stu-id="9bc06-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bc06-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bc06-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bc06-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bc06-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bc06-122">HideFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="9bc06-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bc06-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9bc06-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bc06-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9bc06-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bc06-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9bc06-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bc06-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bc06-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bc06-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bc06-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bc06-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bc06-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bc06-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9bc06-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bc06-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bc06-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bc06-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bc06-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bc06-132">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bc06-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bc06-133">Требования</span><span class="sxs-lookup"><span data-stu-id="9bc06-133">Requirements</span></span>



| <span data-ttu-id="9bc06-134">Требование</span><span class="sxs-lookup"><span data-stu-id="9bc06-134">Requirement</span></span> | <span data-ttu-id="9bc06-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9bc06-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc06-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bc06-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9bc06-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9bc06-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9bc06-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bc06-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9bc06-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9bc06-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9bc06-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9bc06-140">Namespace</span></span><br/>                | <span data-ttu-id="9bc06-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9bc06-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9bc06-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9bc06-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bc06-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bc06-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bc06-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9bc06-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bc06-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bc06-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

