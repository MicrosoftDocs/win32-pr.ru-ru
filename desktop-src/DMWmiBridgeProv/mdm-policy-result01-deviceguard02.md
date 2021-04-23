---
title: Класс MDM_Policy_Result01_DeviceGuard02
description: '\_Класс политики MDM \_ Result01 \_ DeviceGuard02 настраивает политики Device Guard.'
ms.assetid: ba21d324-85dc-4cb5-8123-196413e457eb
keywords:
- Класс MDM_Policy_Result01_DeviceGuard02
- MDM_Policy_Result01_DeviceGuard02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceGuard02
- MDM_Policy_Result01_DeviceGuard02.InstanceID
- MDM_Policy_Result01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e206a732628e442a391cb8b29f7712f5a5ec8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071360"
---
# <a name="mdm_policy_result01_deviceguard02-class"></a><span data-ttu-id="ac277-105">\_Класс политики MDM \_ Result01 \_ DeviceGuard02</span><span class="sxs-lookup"><span data-stu-id="ac277-105">MDM\_Policy\_Result01\_DeviceGuard02 class</span></span>

<span data-ttu-id="ac277-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ac277-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac277-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="ac277-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac277-108">\_Класс политики MDM \_ Result01 \_ DeviceGuard02 настраивает политики Device Guard.</span><span class="sxs-lookup"><span data-stu-id="ac277-108">The MDM\_Policy\_Result01\_DeviceGuard02 class configures the Device Guard policies.</span></span>

<span data-ttu-id="ac277-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ac277-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac277-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac277-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="ac277-111">Члены</span><span class="sxs-lookup"><span data-stu-id="ac277-111">Members</span></span>

<span data-ttu-id="ac277-112">Класс **\_ политики MDM \_ Result01 \_ DeviceGuard02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ac277-112">The **MDM\_Policy\_Result01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="ac277-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac277-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac277-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac277-114">Properties</span></span>

<span data-ttu-id="ac277-115">Класс **\_ политики MDM \_ Result01 \_ DeviceGuard02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ac277-115">The **MDM\_Policy\_Result01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ac277-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="ac277-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac277-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ac277-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac277-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ac277-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac277-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac277-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac277-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac277-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac277-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac277-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac277-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac277-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac277-123">лсакфгфлагс</span><span class="sxs-lookup"><span data-stu-id="ac277-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac277-124">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ac277-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac277-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ac277-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac277-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ac277-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac277-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac277-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac277-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac277-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac277-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac277-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac277-130">рекуиреплатформсекуритифеатурес</span><span class="sxs-lookup"><span data-stu-id="ac277-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac277-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ac277-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac277-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ac277-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac277-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ac277-133">Requirements</span></span>



| <span data-ttu-id="ac277-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ac277-134">Requirement</span></span> | <span data-ttu-id="ac277-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ac277-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac277-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac277-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ac277-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ac277-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac277-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac277-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ac277-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac277-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ac277-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac277-140">Namespace</span></span><br/>                | <span data-ttu-id="ac277-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="ac277-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ac277-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ac277-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac277-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac277-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac277-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ac277-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac277-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac277-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

