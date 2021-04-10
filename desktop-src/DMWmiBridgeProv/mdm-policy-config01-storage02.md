---
title: Класс MDM_Policy_Config01_Storage02
description: '\_Класс политики MDM \_ Config01 \_ Storage02 настраивает политики хранения.'
ms.assetid: 5c58e6d4-dfc6-4467-9a86-08eb31ccf28d
keywords:
- Класс MDM_Policy_Config01_Storage02
- MDM_Policy_Config01_Storage02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Storage02
- MDM_Policy_Config01_Storage02.InstanceID
- MDM_Policy_Config01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445c73158e032d888b5b1d0ec4496d2fd49c1ae1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136042"
---
# <a name="mdm_policy_config01_storage02-class"></a><span data-ttu-id="8a593-105">\_Класс политики MDM \_ Config01 \_ Storage02</span><span class="sxs-lookup"><span data-stu-id="8a593-105">MDM\_Policy\_Config01\_Storage02 class</span></span>

<span data-ttu-id="8a593-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8a593-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8a593-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8a593-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8a593-108">\_Класс политики MDM \_ Config01 \_ Storage02 настраивает политики хранения.</span><span class="sxs-lookup"><span data-stu-id="8a593-108">The MDM\_Policy\_Config01\_Storage02 class configures the storage policies.</span></span>

<span data-ttu-id="8a593-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8a593-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a593-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a593-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="8a593-111">Члены</span><span class="sxs-lookup"><span data-stu-id="8a593-111">Members</span></span>

<span data-ttu-id="8a593-112">Класс **\_ политики MDM \_ Config01 \_ Storage02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8a593-112">The **MDM\_Policy\_Config01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="8a593-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8a593-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a593-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="8a593-114">Properties</span></span>

<span data-ttu-id="8a593-115">Класс **\_ политики MDM \_ Config01 \_ Storage02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8a593-115">The **MDM\_Policy\_Config01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8a593-116">алловдискхеалсмоделупдатес</span><span class="sxs-lookup"><span data-stu-id="8a593-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a593-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8a593-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a593-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8a593-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a593-119">енханцедсторажедевицес</span><span class="sxs-lookup"><span data-stu-id="8a593-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a593-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a593-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a593-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8a593-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a593-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8a593-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a593-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a593-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a593-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a593-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a593-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8a593-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a593-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8a593-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a593-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a593-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a593-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a593-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a593-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8a593-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a593-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8a593-130">Requirements</span></span>



| <span data-ttu-id="8a593-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8a593-131">Requirement</span></span> | <span data-ttu-id="8a593-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8a593-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a593-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a593-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8a593-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8a593-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a593-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a593-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8a593-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a593-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8a593-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8a593-137">Namespace</span></span><br/>                | <span data-ttu-id="8a593-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="8a593-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8a593-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8a593-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a593-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a593-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a593-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8a593-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a593-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a593-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

