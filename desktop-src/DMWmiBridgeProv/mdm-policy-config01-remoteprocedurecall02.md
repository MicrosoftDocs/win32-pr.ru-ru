---
title: Класс MDM_Policy_Config01_RemoteProcedureCall02
description: '\_Класс политики MDM \_ Config01 \_ RemoteProcedureCall02 настраивает политики удаленного вызова процедур.'
ms.assetid: d844c59d-c71e-4a8f-ad1e-955a918a36b8
keywords:
- Класс MDM_Policy_Config01_RemoteProcedureCall02
- MDM_Policy_Config01_RemoteProcedureCall02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteProcedureCall02
- MDM_Policy_Config01_RemoteProcedureCall02.InstanceID
- MDM_Policy_Config01_RemoteProcedureCall02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1c1a188afd3694273080c6c369a8dc37abb22a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490497"
---
# <a name="mdm_policy_config01_remoteprocedurecall02-class"></a><span data-ttu-id="daaab-105">\_Класс политики MDM \_ Config01 \_ RemoteProcedureCall02</span><span class="sxs-lookup"><span data-stu-id="daaab-105">MDM\_Policy\_Config01\_RemoteProcedureCall02 class</span></span>

<span data-ttu-id="daaab-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="daaab-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="daaab-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="daaab-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="daaab-108">\_Класс политики MDM \_ Config01 \_ RemoteProcedureCall02 настраивает политики удаленного вызова процедур.</span><span class="sxs-lookup"><span data-stu-id="daaab-108">The MDM\_Policy\_Config01\_RemoteProcedureCall02 class configures the remote procedure call policies.</span></span>

<span data-ttu-id="daaab-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="daaab-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="daaab-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daaab-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteProcedureCall02
{
  string InstanceID;
  string ParentID;
  string RestrictUnauthenticatedRPCClients;
  string RPCEndpointMapperClientAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="daaab-111">Члены</span><span class="sxs-lookup"><span data-stu-id="daaab-111">Members</span></span>

<span data-ttu-id="daaab-112">Класс **\_ политики MDM \_ Config01 \_ RemoteProcedureCall02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="daaab-112">The **MDM\_Policy\_Config01\_RemoteProcedureCall02** class has these types of members:</span></span>

-   [<span data-ttu-id="daaab-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="daaab-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="daaab-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="daaab-114">Properties</span></span>

<span data-ttu-id="daaab-115">Класс **\_ политики MDM \_ Config01 \_ RemoteProcedureCall02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="daaab-115">The **MDM\_Policy\_Config01\_RemoteProcedureCall02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="daaab-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="daaab-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daaab-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="daaab-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daaab-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="daaab-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="daaab-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="daaab-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="daaab-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="daaab-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="daaab-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="daaab-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daaab-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="daaab-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="daaab-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="daaab-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="daaab-124">рестриктунаусентикатедрпкклиентс</span><span class="sxs-lookup"><span data-stu-id="daaab-124">RestrictUnauthenticatedRPCClients</span></span>](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-restrictunauthenticatedrpcclients)
</dt> <dd> <dl> <dt>

<span data-ttu-id="daaab-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="daaab-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daaab-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daaab-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="daaab-127">рпцендпоинтмапперклиентаусентикатион</span><span class="sxs-lookup"><span data-stu-id="daaab-127">RPCEndpointMapperClientAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-rpcendpointmapperclientauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="daaab-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="daaab-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="daaab-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="daaab-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="daaab-130">Требования</span><span class="sxs-lookup"><span data-stu-id="daaab-130">Requirements</span></span>



| <span data-ttu-id="daaab-131">Требование</span><span class="sxs-lookup"><span data-stu-id="daaab-131">Requirement</span></span> | <span data-ttu-id="daaab-132">Значение</span><span class="sxs-lookup"><span data-stu-id="daaab-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daaab-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="daaab-133">Minimum supported client</span></span><br/> | <span data-ttu-id="daaab-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="daaab-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="daaab-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="daaab-135">Minimum supported server</span></span><br/> | <span data-ttu-id="daaab-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="daaab-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="daaab-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="daaab-137">Namespace</span></span><br/>                | <span data-ttu-id="daaab-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="daaab-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="daaab-139">MOF</span><span class="sxs-lookup"><span data-stu-id="daaab-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="daaab-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="daaab-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="daaab-141">DLL</span><span class="sxs-lookup"><span data-stu-id="daaab-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daaab-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daaab-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

