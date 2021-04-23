---
title: Класс MDM_Policy_Config01_RemoteDesktopServices02
description: '\_Класс политики MDM \_ Config01 \_ RemoteDesktopServices02 настраивает политики службы удаленных рабочих столов.'
ms.assetid: d2c53be7-6dec-4603-b851-e9c979475496
keywords:
- Класс MDM_Policy_Config01_RemoteDesktopServices02
- MDM_Policy_Config01_RemoteDesktopServices02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteDesktopServices02
- MDM_Policy_Config01_RemoteDesktopServices02.InstanceID
- MDM_Policy_Config01_RemoteDesktopServices02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a023ae44c7b8ab170d4efe9c38aaacdeca3cc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988633"
---
# <a name="mdm_policy_config01_remotedesktopservices02-class"></a><span data-ttu-id="557c3-105">\_Класс политики MDM \_ Config01 \_ RemoteDesktopServices02</span><span class="sxs-lookup"><span data-stu-id="557c3-105">MDM\_Policy\_Config01\_RemoteDesktopServices02 class</span></span>

<span data-ttu-id="557c3-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="557c3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="557c3-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="557c3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="557c3-108">\_Класс политики MDM \_ Config01 \_ RemoteDesktopServices02 настраивает политики службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="557c3-108">The MDM\_Policy\_Config01\_RemoteDesktopServices02 class configures the remote desktop service policies.</span></span>

<span data-ttu-id="557c3-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="557c3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="557c3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="557c3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteDesktopServices02
{
  string InstanceID;
  string ParentID;
  string AllowUsersToConnectRemotely;
  string ClientConnectionEncryptionLevel;
  string DoNotAllowDriveRedirection;
  string DoNotAllowPasswordSaving;
  string PromptForPasswordUponConnection;
  string RequireSecureRPCCommunication;
};
```

## <a name="members"></a><span data-ttu-id="557c3-111">Члены</span><span class="sxs-lookup"><span data-stu-id="557c3-111">Members</span></span>

<span data-ttu-id="557c3-112">Класс **\_ политики MDM \_ Config01 \_ RemoteDesktopServices02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="557c3-112">The **MDM\_Policy\_Config01\_RemoteDesktopServices02** class has these types of members:</span></span>

-   [<span data-ttu-id="557c3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="557c3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="557c3-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="557c3-114">Properties</span></span>

<span data-ttu-id="557c3-115">Класс **\_ политики MDM \_ Config01 \_ RemoteDesktopServices02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="557c3-115">The **MDM\_Policy\_Config01\_RemoteDesktopServices02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="557c3-116">алловусерстоконнектремотели</span><span class="sxs-lookup"><span data-stu-id="557c3-116">AllowUsersToConnectRemotely</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-allowuserstoconnectremotely)
</dt> <dd> <dl> <dt>

<span data-ttu-id="557c3-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="557c3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557c3-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="557c3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="557c3-119">клиентконнектионенкриптионлевел</span><span class="sxs-lookup"><span data-stu-id="557c3-119">ClientConnectionEncryptionLevel</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-clientconnectionencryptionlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="557c3-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="557c3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557c3-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="557c3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="557c3-122">доноталловдривередиректион</span><span class="sxs-lookup"><span data-stu-id="557c3-122">DoNotAllowDriveRedirection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowdriveredirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="557c3-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="557c3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557c3-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="557c3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="557c3-125">доноталловпассвордсавинг</span><span class="sxs-lookup"><span data-stu-id="557c3-125">DoNotAllowPasswordSaving</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowpasswordsaving)
</dt> <dd> <dl> <dt>

<span data-ttu-id="557c3-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="557c3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557c3-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="557c3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="557c3-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="557c3-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557c3-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="557c3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557c3-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="557c3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="557c3-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="557c3-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="557c3-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="557c3-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="557c3-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="557c3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557c3-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="557c3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="557c3-135">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="557c3-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="557c3-136">промптфорпассвордупонконнектион</span><span class="sxs-lookup"><span data-stu-id="557c3-136">PromptForPasswordUponConnection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-promptforpassworduponconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="557c3-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="557c3-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557c3-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="557c3-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="557c3-139">рекуиресекурерпккоммуникатион</span><span class="sxs-lookup"><span data-stu-id="557c3-139">RequireSecureRPCCommunication</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-requiresecurerpccommunication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="557c3-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="557c3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="557c3-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="557c3-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="557c3-142">Требования</span><span class="sxs-lookup"><span data-stu-id="557c3-142">Requirements</span></span>



| <span data-ttu-id="557c3-143">Требование</span><span class="sxs-lookup"><span data-stu-id="557c3-143">Requirement</span></span> | <span data-ttu-id="557c3-144">Значение</span><span class="sxs-lookup"><span data-stu-id="557c3-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="557c3-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="557c3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="557c3-146">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="557c3-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="557c3-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="557c3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="557c3-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="557c3-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="557c3-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="557c3-149">Namespace</span></span><br/>                | <span data-ttu-id="557c3-150">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="557c3-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="557c3-151">MOF</span><span class="sxs-lookup"><span data-stu-id="557c3-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="557c3-152"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="557c3-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="557c3-153">DLL</span><span class="sxs-lookup"><span data-stu-id="557c3-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="557c3-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="557c3-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

