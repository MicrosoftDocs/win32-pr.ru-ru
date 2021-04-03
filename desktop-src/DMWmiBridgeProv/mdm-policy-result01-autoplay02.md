---
title: Класс MDM_Policy_Result01_Autoplay02
description: '\_Класс политики MDM \_ Result01 \_ Autoplay02 представляет доступные политики автозапуска.'
ms.assetid: f116015d-f10e-4d17-9c0b-7253894e6c0f
keywords:
- Класс MDM_Policy_Result01_Autoplay02
- MDM_Policy_Result01_Autoplay02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Autoplay02
- MDM_Policy_Result01_Autoplay02.InstanceID
- MDM_Policy_Result01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abf48754cff1513d6d373c9addb34b8ec9acc26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137531"
---
# <a name="mdm_policy_result01_autoplay02-class"></a><span data-ttu-id="2fa03-105">\_Класс политики MDM \_ Result01 \_ Autoplay02</span><span class="sxs-lookup"><span data-stu-id="2fa03-105">MDM\_Policy\_Result01\_Autoplay02 class</span></span>

<span data-ttu-id="2fa03-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="2fa03-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2fa03-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="2fa03-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2fa03-108">\_Класс политики MDM \_ Result01 \_ Autoplay02 представляет доступные политики автозапуска.</span><span class="sxs-lookup"><span data-stu-id="2fa03-108">The MDM\_Policy\_Result01\_Autoplay02 class represents the available autoplay policies.</span></span>

<span data-ttu-id="2fa03-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2fa03-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa03-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fa03-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="2fa03-111">Члены</span><span class="sxs-lookup"><span data-stu-id="2fa03-111">Members</span></span>

<span data-ttu-id="2fa03-112">Класс **\_ политики MDM \_ Result01 \_ Autoplay02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2fa03-112">The **MDM\_Policy\_Result01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="2fa03-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2fa03-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fa03-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="2fa03-114">Properties</span></span>

<span data-ttu-id="2fa03-115">Класс **\_ политики MDM \_ Result01 \_ Autoplay02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2fa03-115">The **MDM\_Policy\_Result01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2fa03-116">дисалловаутоплайфорнонволумедевицес</span><span class="sxs-lookup"><span data-stu-id="2fa03-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fa03-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2fa03-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fa03-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2fa03-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2fa03-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2fa03-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fa03-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2fa03-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fa03-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2fa03-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fa03-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fa03-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2fa03-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2fa03-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fa03-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2fa03-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fa03-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2fa03-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fa03-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fa03-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2fa03-127">сетдефаултауторунбехавиор</span><span class="sxs-lookup"><span data-stu-id="2fa03-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fa03-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2fa03-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fa03-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2fa03-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2fa03-130">турноффаутоплай</span><span class="sxs-lookup"><span data-stu-id="2fa03-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fa03-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2fa03-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fa03-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2fa03-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fa03-133">Требования</span><span class="sxs-lookup"><span data-stu-id="2fa03-133">Requirements</span></span>



| <span data-ttu-id="2fa03-134">Требование</span><span class="sxs-lookup"><span data-stu-id="2fa03-134">Requirement</span></span> | <span data-ttu-id="2fa03-135">Значение</span><span class="sxs-lookup"><span data-stu-id="2fa03-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa03-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2fa03-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa03-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2fa03-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2fa03-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2fa03-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa03-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2fa03-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2fa03-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2fa03-140">Namespace</span></span><br/>                | <span data-ttu-id="2fa03-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="2fa03-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2fa03-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2fa03-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fa03-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fa03-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fa03-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2fa03-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fa03-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fa03-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

