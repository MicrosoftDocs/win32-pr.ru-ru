---
title: Класс MDM_Policy_Config01_RemoteShell02
description: '\_Класс политики MDM \_ Config01 \_ RemoteShell02 настраивает политики удаленной оболочки.'
ms.assetid: 7026fadb-ec6a-4696-a24c-1b1e071b94b0
keywords:
- Класс MDM_Policy_Config01_RemoteShell02
- MDM_Policy_Config01_RemoteShell02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteShell02
- MDM_Policy_Config01_RemoteShell02.InstanceID
- MDM_Policy_Config01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c318b0c6f23e92d90091495fdc25993d6958ca56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490827"
---
# <a name="mdm_policy_config01_remoteshell02-class"></a><span data-ttu-id="1b446-105">\_Класс политики MDM \_ Config01 \_ RemoteShell02</span><span class="sxs-lookup"><span data-stu-id="1b446-105">MDM\_Policy\_Config01\_RemoteShell02 class</span></span>

<span data-ttu-id="1b446-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1b446-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1b446-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1b446-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1b446-108">\_Класс политики MDM \_ Config01 \_ RemoteShell02 настраивает политики удаленной оболочки.</span><span class="sxs-lookup"><span data-stu-id="1b446-108">The MDM\_Policy\_Config01\_RemoteShell02 class configures the remote shell policies.</span></span>

<span data-ttu-id="1b446-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1b446-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b446-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b446-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteShell02
{
  string InstanceID;
  string ParentID;
  string AllowRemoteShellAccess;
  string MaxConcurrentUsers;
  string SpecifyIdleTimeout;
  string SpecifyMaxMemory;
  string SpecifyMaxProcesses;
  string SpecifyMaxRemoteShells;
  string SpecifyShellTimeout;
};
```

## <a name="members"></a><span data-ttu-id="1b446-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1b446-111">Members</span></span>

<span data-ttu-id="1b446-112">Класс **\_ политики MDM \_ Config01 \_ RemoteShell02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1b446-112">The **MDM\_Policy\_Config01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="1b446-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b446-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b446-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b446-114">Properties</span></span>

<span data-ttu-id="1b446-115">Класс **\_ политики MDM \_ Config01 \_ RemoteShell02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1b446-115">The **MDM\_Policy\_Config01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1b446-116">алловремотешеллакцесс</span><span class="sxs-lookup"><span data-stu-id="1b446-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b446-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1b446-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1b446-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b446-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b446-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1b446-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1b446-123">максконкуррентусерс</span><span class="sxs-lookup"><span data-stu-id="1b446-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b446-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1b446-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1b446-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b446-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b446-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1b446-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1b446-130">спеЦифидлетимеаут</span><span class="sxs-lookup"><span data-stu-id="1b446-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b446-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1b446-133">спеЦифимаксмемори</span><span class="sxs-lookup"><span data-stu-id="1b446-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b446-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1b446-136">спеЦифимакспроцессес</span><span class="sxs-lookup"><span data-stu-id="1b446-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b446-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1b446-139">спеЦифимаксремотешеллс</span><span class="sxs-lookup"><span data-stu-id="1b446-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b446-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1b446-142">спеЦифишеллтимеаут</span><span class="sxs-lookup"><span data-stu-id="1b446-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b446-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b446-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b446-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b446-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b446-145">Требования</span><span class="sxs-lookup"><span data-stu-id="1b446-145">Requirements</span></span>



| <span data-ttu-id="1b446-146">Требование</span><span class="sxs-lookup"><span data-stu-id="1b446-146">Requirement</span></span> | <span data-ttu-id="1b446-147">Значение</span><span class="sxs-lookup"><span data-stu-id="1b446-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b446-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b446-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1b446-149">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1b446-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1b446-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b446-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1b446-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1b446-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1b446-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1b446-152">Namespace</span></span><br/>                | <span data-ttu-id="1b446-153">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1b446-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1b446-154">MOF</span><span class="sxs-lookup"><span data-stu-id="1b446-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b446-155"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b446-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b446-156">DLL</span><span class="sxs-lookup"><span data-stu-id="1b446-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b446-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b446-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

