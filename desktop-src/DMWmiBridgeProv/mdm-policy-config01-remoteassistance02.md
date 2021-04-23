---
title: Класс MDM_Policy_Config01_RemoteAssistance02
description: '\_Класс политики MDM \_ Config01 \_ RemoteAssistance02 настраивает политики удаленной помощи.'
ms.assetid: bcc6c570-66d9-4dcd-b7f2-2d03733c0bcb
keywords:
- Класс MDM_Policy_Config01_RemoteAssistance02
- MDM_Policy_Config01_RemoteAssistance02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteAssistance02
- MDM_Policy_Config01_RemoteAssistance02.InstanceID
- MDM_Policy_Config01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceadb2eb784e72e4e332cdd34df44d779c99e97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891893"
---
# <a name="mdm_policy_config01_remoteassistance02-class"></a><span data-ttu-id="df0fa-105">\_Класс политики MDM \_ Config01 \_ RemoteAssistance02</span><span class="sxs-lookup"><span data-stu-id="df0fa-105">MDM\_Policy\_Config01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="df0fa-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="df0fa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="df0fa-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="df0fa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="df0fa-108">\_Класс политики MDM \_ Config01 \_ RemoteAssistance02 настраивает политики удаленной помощи.</span><span class="sxs-lookup"><span data-stu-id="df0fa-108">The MDM\_Policy\_Config01\_RemoteAssistance02 class configures the remote assistance policies.</span></span>

<span data-ttu-id="df0fa-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="df0fa-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0fa-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df0fa-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="df0fa-111">Члены</span><span class="sxs-lookup"><span data-stu-id="df0fa-111">Members</span></span>

<span data-ttu-id="df0fa-112">Класс **\_ политики MDM \_ Config01 \_ RemoteAssistance02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="df0fa-112">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="df0fa-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="df0fa-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df0fa-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="df0fa-114">Properties</span></span>

<span data-ttu-id="df0fa-115">Класс **\_ политики MDM \_ Config01 \_ RemoteAssistance02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="df0fa-115">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="df0fa-116">кустомизеварнингмессажес</span><span class="sxs-lookup"><span data-stu-id="df0fa-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0fa-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="df0fa-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df0fa-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="df0fa-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df0fa-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="df0fa-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0fa-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="df0fa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df0fa-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df0fa-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df0fa-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="df0fa-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df0fa-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="df0fa-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0fa-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="df0fa-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df0fa-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df0fa-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df0fa-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="df0fa-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="df0fa-127">сессионлоггинг</span><span class="sxs-lookup"><span data-stu-id="df0fa-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0fa-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="df0fa-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df0fa-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="df0fa-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="df0fa-130">солиЦитедремотеассистанце</span><span class="sxs-lookup"><span data-stu-id="df0fa-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0fa-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="df0fa-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df0fa-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="df0fa-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="df0fa-133">унсолиЦитедремотеассистанце</span><span class="sxs-lookup"><span data-stu-id="df0fa-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="df0fa-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="df0fa-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df0fa-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="df0fa-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df0fa-136">Требования</span><span class="sxs-lookup"><span data-stu-id="df0fa-136">Requirements</span></span>



| <span data-ttu-id="df0fa-137">Требование</span><span class="sxs-lookup"><span data-stu-id="df0fa-137">Requirement</span></span> | <span data-ttu-id="df0fa-138">Значение</span><span class="sxs-lookup"><span data-stu-id="df0fa-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df0fa-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df0fa-139">Minimum supported client</span></span><br/> | <span data-ttu-id="df0fa-140">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="df0fa-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df0fa-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df0fa-141">Minimum supported server</span></span><br/> | <span data-ttu-id="df0fa-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="df0fa-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="df0fa-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="df0fa-143">Namespace</span></span><br/>                | <span data-ttu-id="df0fa-144">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="df0fa-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="df0fa-145">MOF</span><span class="sxs-lookup"><span data-stu-id="df0fa-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df0fa-146"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df0fa-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="df0fa-147">DLL</span><span class="sxs-lookup"><span data-stu-id="df0fa-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df0fa-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df0fa-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

