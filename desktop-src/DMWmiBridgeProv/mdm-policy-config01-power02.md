---
title: Класс MDM_Policy_Config01_Power02
description: '\_Класс политики MDM \_ Config01 \_ Power02 настраивает политики управления питанием.'
ms.assetid: 8913c38c-0d8d-456f-a412-d47c2ccd5d13
keywords:
- Класс MDM_Policy_Config01_Power02
- MDM_Policy_Config01_Power02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Power02
- MDM_Policy_Config01_Power02.InstanceID
- MDM_Policy_Config01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9bdda57bbd85100e8bccb87990d928f448a972
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135850"
---
# <a name="mdm_policy_config01_power02-class"></a><span data-ttu-id="b79e0-105">\_Класс политики MDM \_ Config01 \_ Power02</span><span class="sxs-lookup"><span data-stu-id="b79e0-105">MDM\_Policy\_Config01\_Power02 class</span></span>

<span data-ttu-id="b79e0-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="b79e0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b79e0-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="b79e0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b79e0-108">\_Класс политики MDM \_ Config01 \_ Power02 настраивает политики управления питанием.</span><span class="sxs-lookup"><span data-stu-id="b79e0-108">The MDM\_Policy\_Config01\_Power02 class configures the power policies.</span></span>

<span data-ttu-id="b79e0-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b79e0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79e0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b79e0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a><span data-ttu-id="b79e0-111">Члены</span><span class="sxs-lookup"><span data-stu-id="b79e0-111">Members</span></span>

<span data-ttu-id="b79e0-112">Класс **\_ политики MDM \_ Config01 \_ Power02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b79e0-112">The **MDM\_Policy\_Config01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="b79e0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b79e0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b79e0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b79e0-114">Properties</span></span>

<span data-ttu-id="b79e0-115">Класс **\_ политики MDM \_ Config01 \_ Power02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b79e0-115">The **MDM\_Policy\_Config01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b79e0-116">алловстандбивхенслипингплугжедин</span><span class="sxs-lookup"><span data-stu-id="b79e0-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b79e0-119">дисплайоффтимеаутонбаттери</span><span class="sxs-lookup"><span data-stu-id="b79e0-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b79e0-122">дисплайоффтимеаутплугжедин</span><span class="sxs-lookup"><span data-stu-id="b79e0-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b79e0-125">хибернатетимеаутонбаттери</span><span class="sxs-lookup"><span data-stu-id="b79e0-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b79e0-128">хибернатетимеаутплугжедин</span><span class="sxs-lookup"><span data-stu-id="b79e0-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b79e0-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b79e0-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b79e0-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b79e0-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b79e0-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b79e0-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b79e0-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-138">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b79e0-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b79e0-139">рекуирепассвордвхенкомпутервакесонбаттери</span><span class="sxs-lookup"><span data-stu-id="b79e0-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b79e0-142">рекуирепассвордвхенкомпутервакесплугжедин</span><span class="sxs-lookup"><span data-stu-id="b79e0-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b79e0-145">стандбитимеаутонбаттери</span><span class="sxs-lookup"><span data-stu-id="b79e0-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b79e0-148">стандбитимеаутплугжедин</span><span class="sxs-lookup"><span data-stu-id="b79e0-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79e0-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b79e0-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79e0-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b79e0-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b79e0-151">Требования</span><span class="sxs-lookup"><span data-stu-id="b79e0-151">Requirements</span></span>



| <span data-ttu-id="b79e0-152">Требование</span><span class="sxs-lookup"><span data-stu-id="b79e0-152">Requirement</span></span> | <span data-ttu-id="b79e0-153">Значение</span><span class="sxs-lookup"><span data-stu-id="b79e0-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b79e0-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b79e0-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b79e0-155">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b79e0-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b79e0-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b79e0-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b79e0-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b79e0-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b79e0-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b79e0-158">Namespace</span></span><br/>                | <span data-ttu-id="b79e0-159">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="b79e0-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b79e0-160">MOF</span><span class="sxs-lookup"><span data-stu-id="b79e0-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b79e0-161"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b79e0-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b79e0-162">DLL</span><span class="sxs-lookup"><span data-stu-id="b79e0-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b79e0-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b79e0-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

