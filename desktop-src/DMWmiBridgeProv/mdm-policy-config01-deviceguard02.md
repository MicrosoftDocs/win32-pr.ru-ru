---
title: Класс MDM_Policy_Config01_DeviceGuard02
description: Политика MDM \_ \_ Config01 \_ DeviceGuard02 настраивает политики Device Guard.
ms.assetid: b8edf906-2486-4d8d-9410-d216bacf1728
keywords:
- Класс MDM_Policy_Config01_DeviceGuard02
- MDM_Policy_Config01_DeviceGuard02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceGuard02
- MDM_Policy_Config01_DeviceGuard02.InstanceID
- MDM_Policy_Config01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebcc8f3d929708cdff3ada8fe440f49a1aeb1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071171"
---
# <a name="mdm_policy_config01_deviceguard02-class"></a><span data-ttu-id="c1f73-105">\_Класс политики MDM \_ Config01 \_ DeviceGuard02</span><span class="sxs-lookup"><span data-stu-id="c1f73-105">MDM\_Policy\_Config01\_DeviceGuard02 class</span></span>

<span data-ttu-id="c1f73-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c1f73-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c1f73-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c1f73-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c1f73-108">Политика MDM \_ \_ Config01 \_ DeviceGuard02 настраивает политики Device Guard.</span><span class="sxs-lookup"><span data-stu-id="c1f73-108">The MDM\_Policy\_Config01\_DeviceGuard02 configures the Device Guard policies.</span></span>

<span data-ttu-id="c1f73-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c1f73-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1f73-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1f73-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="c1f73-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c1f73-111">Members</span></span>

<span data-ttu-id="c1f73-112">Класс **\_ политики MDM \_ Config01 \_ DeviceGuard02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c1f73-112">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="c1f73-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c1f73-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1f73-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c1f73-114">Properties</span></span>

<span data-ttu-id="c1f73-115">Класс **\_ политики MDM \_ Config01 \_ DeviceGuard02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c1f73-115">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c1f73-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="c1f73-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f73-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f73-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f73-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c1f73-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1f73-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c1f73-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f73-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1f73-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1f73-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1f73-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1f73-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1f73-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1f73-123">лсакфгфлагс</span><span class="sxs-lookup"><span data-stu-id="c1f73-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f73-124">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f73-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f73-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c1f73-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1f73-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c1f73-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f73-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1f73-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1f73-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1f73-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1f73-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1f73-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1f73-130">рекуиреплатформсекуритифеатурес</span><span class="sxs-lookup"><span data-stu-id="c1f73-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f73-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f73-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f73-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c1f73-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1f73-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c1f73-133">Requirements</span></span>



| <span data-ttu-id="c1f73-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c1f73-134">Requirement</span></span> | <span data-ttu-id="c1f73-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c1f73-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f73-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1f73-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c1f73-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c1f73-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1f73-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1f73-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c1f73-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c1f73-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c1f73-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c1f73-140">Namespace</span></span><br/>                | <span data-ttu-id="c1f73-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c1f73-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c1f73-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c1f73-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1f73-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1f73-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1f73-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c1f73-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1f73-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1f73-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

