---
title: Класс MDM_Policy_Result01_RemoteShell02
description: '\_Класс политики MDM \_ Result01 \_ RemoteShell02 представляет политики удаленной оболочки.'
ms.assetid: d005b2e6-e838-4bda-9ba4-bd49c092f951
keywords:
- Класс MDM_Policy_Result01_RemoteShell02
- MDM_Policy_Result01_RemoteShell02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteShell02
- MDM_Policy_Result01_RemoteShell02.InstanceID
- MDM_Policy_Result01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babd602823d0cc2e98a6855c3803aea240627e37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891589"
---
# <a name="mdm_policy_result01_remoteshell02-class"></a><span data-ttu-id="2c2ac-105">\_Класс политики MDM \_ Result01 \_ RemoteShell02</span><span class="sxs-lookup"><span data-stu-id="2c2ac-105">MDM\_Policy\_Result01\_RemoteShell02 class</span></span>

<span data-ttu-id="2c2ac-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2c2ac-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="2c2ac-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2c2ac-108">\_Класс политики MDM \_ Result01 \_ RemoteShell02 представляет политики удаленной оболочки.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-108">The MDM\_Policy\_Result01\_RemoteShell02 class represents the remote shell policies.</span></span>

<span data-ttu-id="2c2ac-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2ac-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c2ac-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteShell02
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

## <a name="members"></a><span data-ttu-id="2c2ac-111">Члены</span><span class="sxs-lookup"><span data-stu-id="2c2ac-111">Members</span></span>

<span data-ttu-id="2c2ac-112">Класс **\_ политики MDM \_ Result01 \_ RemoteShell02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2c2ac-112">The **MDM\_Policy\_Result01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="2c2ac-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2c2ac-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c2ac-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="2c2ac-114">Properties</span></span>

<span data-ttu-id="2c2ac-115">Класс **\_ политики MDM \_ Result01 \_ RemoteShell02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2c2ac-115">The **MDM\_Policy\_Result01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2c2ac-116">алловремотешеллакцесс</span><span class="sxs-lookup"><span data-stu-id="2c2ac-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c2ac-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c2ac-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c2ac-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c2ac-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c2ac-123">максконкуррентусерс</span><span class="sxs-lookup"><span data-stu-id="2c2ac-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c2ac-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c2ac-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c2ac-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c2ac-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c2ac-130">спеЦифидлетимеаут</span><span class="sxs-lookup"><span data-stu-id="2c2ac-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c2ac-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c2ac-133">спеЦифимаксмемори</span><span class="sxs-lookup"><span data-stu-id="2c2ac-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c2ac-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c2ac-136">спеЦифимакспроцессес</span><span class="sxs-lookup"><span data-stu-id="2c2ac-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c2ac-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c2ac-139">спеЦифимаксремотешеллс</span><span class="sxs-lookup"><span data-stu-id="2c2ac-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c2ac-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c2ac-142">спеЦифишеллтимеаут</span><span class="sxs-lookup"><span data-stu-id="2c2ac-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2ac-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c2ac-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2ac-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c2ac-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c2ac-145">Требования</span><span class="sxs-lookup"><span data-stu-id="2c2ac-145">Requirements</span></span>



| <span data-ttu-id="2c2ac-146">Требование</span><span class="sxs-lookup"><span data-stu-id="2c2ac-146">Requirement</span></span> | <span data-ttu-id="2c2ac-147">Значение</span><span class="sxs-lookup"><span data-stu-id="2c2ac-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2ac-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c2ac-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2c2ac-149">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2c2ac-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c2ac-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c2ac-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2c2ac-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2c2ac-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2c2ac-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2c2ac-152">Namespace</span></span><br/>                | <span data-ttu-id="2c2ac-153">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="2c2ac-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2c2ac-154">MOF</span><span class="sxs-lookup"><span data-stu-id="2c2ac-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c2ac-155"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c2ac-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c2ac-156">DLL</span><span class="sxs-lookup"><span data-stu-id="2c2ac-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c2ac-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c2ac-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

