---
title: Класс MDM_Policy_Config01_Autoplay02
description: '\_Класс политики MDM \_ Config01 \_ Autoplay02 настраивает доступные политики автозапуска.'
ms.assetid: ef7ccdb6-3f77-4c43-87d9-56acda97be21
keywords:
- Класс MDM_Policy_Config01_Autoplay02
- MDM_Policy_Config01_Autoplay02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Autoplay02
- MDM_Policy_Config01_Autoplay02.InstanceID
- MDM_Policy_Config01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e064d0b0eed457bcafdf4da9bf8e72fbb4916e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071434"
---
# <a name="mdm_policy_config01_autoplay02-class"></a><span data-ttu-id="f7b44-105">\_Класс политики MDM \_ Config01 \_ Autoplay02</span><span class="sxs-lookup"><span data-stu-id="f7b44-105">MDM\_Policy\_Config01\_Autoplay02 class</span></span>

<span data-ttu-id="f7b44-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f7b44-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f7b44-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f7b44-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f7b44-108">\_Класс политики MDM \_ Config01 \_ Autoplay02 настраивает доступные политики автозапуска.</span><span class="sxs-lookup"><span data-stu-id="f7b44-108">The MDM\_Policy\_Config01\_Autoplay02 class configures the available autoplay policies.</span></span>

<span data-ttu-id="f7b44-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f7b44-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b44-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7b44-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="f7b44-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f7b44-111">Members</span></span>

<span data-ttu-id="f7b44-112">Класс **\_ политики MDM \_ Config01 \_ Autoplay02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f7b44-112">The **MDM\_Policy\_Config01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="f7b44-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f7b44-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7b44-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f7b44-114">Properties</span></span>

<span data-ttu-id="f7b44-115">Класс **\_ политики MDM \_ Config01 \_ Autoplay02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f7b44-115">The **MDM\_Policy\_Config01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f7b44-116">дисалловаутоплайфорнонволумедевицес</span><span class="sxs-lookup"><span data-stu-id="f7b44-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7b44-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7b44-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7b44-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7b44-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f7b44-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f7b44-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7b44-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7b44-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7b44-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7b44-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7b44-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7b44-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f7b44-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f7b44-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7b44-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7b44-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7b44-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7b44-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7b44-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7b44-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7b44-127">сетдефаултауторунбехавиор</span><span class="sxs-lookup"><span data-stu-id="f7b44-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7b44-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7b44-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7b44-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7b44-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7b44-130">турноффаутоплай</span><span class="sxs-lookup"><span data-stu-id="f7b44-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7b44-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7b44-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7b44-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7b44-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7b44-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f7b44-133">Requirements</span></span>



| <span data-ttu-id="f7b44-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f7b44-134">Requirement</span></span> | <span data-ttu-id="f7b44-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f7b44-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b44-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7b44-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b44-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f7b44-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7b44-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7b44-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b44-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f7b44-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f7b44-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7b44-140">Namespace</span></span><br/>                | <span data-ttu-id="f7b44-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f7b44-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f7b44-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f7b44-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7b44-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7b44-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7b44-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b44-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b44-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b44-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

