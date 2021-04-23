---
title: Класс MDM_Policy_Config01_ApplicationDefaults02
description: '\_Класс политики MDM \_ Config01 \_ ApplicationDefaults02 позволяет администратору задавать тип файла и связи протоколов по умолчанию. Если этот параметр задан, для входа на ПК будут применяться связи по умолчанию.'
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- Класс MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489927"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a><span data-ttu-id="1a8bf-106">\_Класс политики MDM \_ Config01 \_ ApplicationDefaults02</span><span class="sxs-lookup"><span data-stu-id="1a8bf-106">MDM\_Policy\_Config01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="1a8bf-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1a8bf-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1a8bf-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1a8bf-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1a8bf-109">\_Класс политики MDM \_ Config01 \_ ApplicationDefaults02 позволяет администратору задавать тип файла и связи протоколов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a8bf-109">The MDM\_Policy\_Config01\_ApplicationDefaults02 class allows an administrator to set default file type and protocol associations.</span></span> <span data-ttu-id="1a8bf-110">Если этот параметр задан, для входа на ПК будут применяться связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a8bf-110">When set, default associations will be applied on sign-in to the PC.</span></span>

<span data-ttu-id="1a8bf-111">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1a8bf-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a8bf-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a8bf-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="1a8bf-113">Члены</span><span class="sxs-lookup"><span data-stu-id="1a8bf-113">Members</span></span>

<span data-ttu-id="1a8bf-114">Класс **\_ политики MDM \_ Config01 \_ ApplicationDefaults02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1a8bf-114">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="1a8bf-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a8bf-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a8bf-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a8bf-116">Properties</span></span>

<span data-ttu-id="1a8bf-117">Класс **\_ политики MDM \_ Config01 \_ ApplicationDefaults02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1a8bf-117">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1a8bf-118">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a8bf-118">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a8bf-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1a8bf-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a8bf-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1a8bf-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a8bf-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1a8bf-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a8bf-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1a8bf-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a8bf-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1a8bf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a8bf-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a8bf-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a8bf-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1a8bf-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a8bf-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1a8bf-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a8bf-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1a8bf-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a8bf-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a8bf-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a8bf-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1a8bf-129">Requirements</span></span>



| <span data-ttu-id="1a8bf-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1a8bf-130">Requirement</span></span> | <span data-ttu-id="1a8bf-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1a8bf-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8bf-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a8bf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1a8bf-133">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1a8bf-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a8bf-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a8bf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1a8bf-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1a8bf-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1a8bf-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1a8bf-136">Namespace</span></span><br/>                | <span data-ttu-id="1a8bf-137">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1a8bf-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1a8bf-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1a8bf-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a8bf-139"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a8bf-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a8bf-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1a8bf-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a8bf-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a8bf-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

