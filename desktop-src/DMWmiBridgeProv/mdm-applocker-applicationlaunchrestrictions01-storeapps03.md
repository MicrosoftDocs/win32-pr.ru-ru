---
title: Класс MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
description: Класс MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03 позволяет указать, какие приложения exe разрешены или запрещены для защиты корпоративных данных.
ms.assetid: de5ceaea-589a-4ed7-8dd6-eb9477d68e0e
keywords:
- Класс MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c58610c10e672a6fbc1406b2d022b8ce211871
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654477"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_storeapps03-class"></a><span data-ttu-id="cdcc7-105">\_Класс MDM AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03</span><span class="sxs-lookup"><span data-stu-id="cdcc7-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03 class</span></span>

<span data-ttu-id="cdcc7-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="cdcc7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cdcc7-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="cdcc7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cdcc7-108">Класс **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** позволяет указать, какие приложения exe разрешены или запрещены для защиты корпоративных данных.</span><span class="sxs-lookup"><span data-stu-id="cdcc7-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class allows you to specify which EXE applications are allowed or disallowed for Enterprise Data Protection.</span></span>

<span data-ttu-id="cdcc7-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cdcc7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdcc7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdcc7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="cdcc7-111">Члены</span><span class="sxs-lookup"><span data-stu-id="cdcc7-111">Members</span></span>

<span data-ttu-id="cdcc7-112">Класс **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cdcc7-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="cdcc7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdcc7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdcc7-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdcc7-114">Properties</span></span>

<span data-ttu-id="cdcc7-115">Класс **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cdcc7-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cdcc7-116">**енфорцементмоде**</span><span class="sxs-lookup"><span data-stu-id="cdcc7-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdcc7-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdcc7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdcc7-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cdcc7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cdcc7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cdcc7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdcc7-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdcc7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdcc7-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdcc7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdcc7-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cdcc7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cdcc7-123">Определяет ограничения для запуска приложений из Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="cdcc7-123">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="cdcc7-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cdcc7-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdcc7-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdcc7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdcc7-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdcc7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdcc7-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cdcc7-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cdcc7-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="cdcc7-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="cdcc7-129">Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/аппликатионлаунчрестриктионс/*GROUPING*"</span><span class="sxs-lookup"><span data-stu-id="cdcc7-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="cdcc7-130">**Политика**</span><span class="sxs-lookup"><span data-stu-id="cdcc7-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdcc7-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdcc7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdcc7-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cdcc7-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdcc7-133">Требования</span><span class="sxs-lookup"><span data-stu-id="cdcc7-133">Requirements</span></span>



| <span data-ttu-id="cdcc7-134">Требование</span><span class="sxs-lookup"><span data-stu-id="cdcc7-134">Requirement</span></span> | <span data-ttu-id="cdcc7-135">Значение</span><span class="sxs-lookup"><span data-stu-id="cdcc7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcc7-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdcc7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cdcc7-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cdcc7-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdcc7-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdcc7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cdcc7-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cdcc7-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cdcc7-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cdcc7-140">Namespace</span></span><br/>                | <span data-ttu-id="cdcc7-141">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="cdcc7-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="cdcc7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cdcc7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdcc7-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdcc7-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdcc7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cdcc7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdcc7-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdcc7-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdcc7-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdcc7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdcc7-147">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="cdcc7-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

