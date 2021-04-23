---
title: Класс MDM_Policy_Config01_Display02
description: '\_Класс политики MDM \_ Config01 \_ Display02 настраивает политики экрана.'
ms.assetid: 106eecc5-ede0-4d66-ba51-967a8f7bcb66
keywords:
- Класс MDM_Policy_Config01_Display02
- MDM_Policy_Config01_Display02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Display02
- MDM_Policy_Config01_Display02.InstanceID
- MDM_Policy_Config01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e79861a911d03f1d9174053dc8ec7c62824fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135539"
---
# <a name="mdm_policy_config01_display02-class"></a><span data-ttu-id="59f54-105">\_Класс политики MDM \_ Config01 \_ Display02</span><span class="sxs-lookup"><span data-stu-id="59f54-105">MDM\_Policy\_Config01\_Display02 class</span></span>

<span data-ttu-id="59f54-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="59f54-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="59f54-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="59f54-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="59f54-108">\_Класс политики MDM \_ Config01 \_ Display02 настраивает политики экрана.</span><span class="sxs-lookup"><span data-stu-id="59f54-108">The MDM\_Policy\_Config01\_Display02 class configures the display policies.</span></span>

<span data-ttu-id="59f54-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="59f54-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f54-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59f54-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a><span data-ttu-id="59f54-111">Члены</span><span class="sxs-lookup"><span data-stu-id="59f54-111">Members</span></span>

<span data-ttu-id="59f54-112">Класс **\_ политики MDM \_ Config01 \_ Display02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="59f54-112">The **MDM\_Policy\_Config01\_Display02** class has these types of members:</span></span>

-   [<span data-ttu-id="59f54-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="59f54-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59f54-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="59f54-114">Properties</span></span>

<span data-ttu-id="59f54-115">Класс **\_ политики MDM \_ Config01 \_ Display02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="59f54-115">The **MDM\_Policy\_Config01\_Display02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59f54-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="59f54-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59f54-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="59f54-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59f54-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="59f54-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59f54-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59f54-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="59f54-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="59f54-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59f54-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="59f54-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59f54-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="59f54-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59f54-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59f54-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59f54-124">турноффгдидпискалингфораппс</span><span class="sxs-lookup"><span data-stu-id="59f54-124">TurnOffGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59f54-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="59f54-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59f54-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="59f54-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59f54-127">турнонгдидпискалингфораппс</span><span class="sxs-lookup"><span data-stu-id="59f54-127">TurnOnGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59f54-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="59f54-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59f54-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="59f54-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59f54-130">Требования</span><span class="sxs-lookup"><span data-stu-id="59f54-130">Requirements</span></span>



| <span data-ttu-id="59f54-131">Требование</span><span class="sxs-lookup"><span data-stu-id="59f54-131">Requirement</span></span> | <span data-ttu-id="59f54-132">Значение</span><span class="sxs-lookup"><span data-stu-id="59f54-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f54-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59f54-133">Minimum supported client</span></span><br/> | <span data-ttu-id="59f54-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="59f54-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59f54-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59f54-135">Minimum supported server</span></span><br/> | <span data-ttu-id="59f54-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="59f54-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="59f54-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="59f54-137">Namespace</span></span><br/>                | <span data-ttu-id="59f54-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="59f54-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="59f54-139">MOF</span><span class="sxs-lookup"><span data-stu-id="59f54-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59f54-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59f54-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="59f54-141">DLL</span><span class="sxs-lookup"><span data-stu-id="59f54-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59f54-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59f54-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

