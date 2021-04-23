---
title: Класс MDM_Policy_Result01_Storage02
description: '\_Класс политики MDM \_ Result01 \_ Storage02 представляет доступные политики хранилища.'
ms.assetid: e0e3b867-38b5-4b10-a13e-6f99b8ff6db3
keywords:
- Класс MDM_Policy_Result01_Storage02
- MDM_Policy_Result01_Storage02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Storage02
- MDM_Policy_Result01_Storage02.InstanceID
- MDM_Policy_Result01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63381b34c88ebc590577eec9a11f603ea5325649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071503"
---
# <a name="mdm_policy_result01_storage02-class"></a><span data-ttu-id="c9460-105">\_Класс политики MDM \_ Result01 \_ Storage02</span><span class="sxs-lookup"><span data-stu-id="c9460-105">MDM\_Policy\_Result01\_Storage02 class</span></span>

<span data-ttu-id="c9460-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c9460-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c9460-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c9460-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c9460-108">\_Класс политики MDM \_ Result01 \_ Storage02 представляет доступные политики хранилища.</span><span class="sxs-lookup"><span data-stu-id="c9460-108">The MDM\_Policy\_Result01\_Storage02 class represents the available storage policies.</span></span>

<span data-ttu-id="c9460-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c9460-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9460-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9460-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="c9460-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c9460-111">Members</span></span>

<span data-ttu-id="c9460-112">Класс **\_ политики MDM \_ Result01 \_ Storage02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c9460-112">The **MDM\_Policy\_Result01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="c9460-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c9460-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9460-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c9460-114">Properties</span></span>

<span data-ttu-id="c9460-115">Класс **\_ политики MDM \_ Result01 \_ Storage02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c9460-115">The **MDM\_Policy\_Result01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c9460-116">алловдискхеалсмоделупдатес</span><span class="sxs-lookup"><span data-stu-id="c9460-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9460-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c9460-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9460-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c9460-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c9460-119">енханцедсторажедевицес</span><span class="sxs-lookup"><span data-stu-id="c9460-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9460-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c9460-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9460-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c9460-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9460-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c9460-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9460-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c9460-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9460-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c9460-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9460-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c9460-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9460-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c9460-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9460-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c9460-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9460-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c9460-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9460-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c9460-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9460-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c9460-130">Requirements</span></span>



| <span data-ttu-id="c9460-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c9460-131">Requirement</span></span> | <span data-ttu-id="c9460-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c9460-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9460-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9460-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c9460-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c9460-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9460-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9460-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c9460-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c9460-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c9460-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9460-137">Namespace</span></span><br/>                | <span data-ttu-id="c9460-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c9460-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c9460-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c9460-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9460-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9460-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9460-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c9460-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9460-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9460-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

