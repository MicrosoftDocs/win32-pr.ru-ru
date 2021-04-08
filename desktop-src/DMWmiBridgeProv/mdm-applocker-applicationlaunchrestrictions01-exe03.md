---
title: Класс MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
description: Класс MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03 позволяет указать, какие приложения exe разрешено запускать.
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- Класс MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891773"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a><span data-ttu-id="3fa86-105">\_Класс MDM AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03</span><span class="sxs-lookup"><span data-stu-id="3fa86-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03 class</span></span>

<span data-ttu-id="3fa86-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3fa86-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3fa86-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3fa86-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3fa86-108">Класс **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** позволяет указать, какие приложения exe разрешено запускать.</span><span class="sxs-lookup"><span data-stu-id="3fa86-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class allows you to specify which EXE applications are allowed to launch.</span></span>

<span data-ttu-id="3fa86-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3fa86-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa86-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fa86-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="3fa86-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3fa86-111">Members</span></span>

<span data-ttu-id="3fa86-112">Класс **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3fa86-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="3fa86-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3fa86-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fa86-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3fa86-114">Properties</span></span>

<span data-ttu-id="3fa86-115">Класс **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3fa86-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3fa86-116">**енфорцементмоде**</span><span class="sxs-lookup"><span data-stu-id="3fa86-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa86-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fa86-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fa86-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3fa86-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3fa86-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3fa86-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa86-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fa86-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fa86-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fa86-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fa86-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3fa86-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3fa86-123">Определяет ограничения для запуска исполняемых приложений.</span><span class="sxs-lookup"><span data-stu-id="3fa86-123">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

[<span data-ttu-id="3fa86-124">**нонинтерактивепроцессенфорцемент**</span><span class="sxs-lookup"><span data-stu-id="3fa86-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa86-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fa86-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fa86-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3fa86-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3fa86-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3fa86-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa86-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fa86-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fa86-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fa86-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fa86-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3fa86-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3fa86-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="3fa86-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="3fa86-132">Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/аппликатионлаунчрестриктионс/*GROUPING*"</span><span class="sxs-lookup"><span data-stu-id="3fa86-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="3fa86-133">**Политика**</span><span class="sxs-lookup"><span data-stu-id="3fa86-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa86-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fa86-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fa86-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3fa86-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3fa86-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3fa86-136">Requirements</span></span>



| <span data-ttu-id="3fa86-137">Требование</span><span class="sxs-lookup"><span data-stu-id="3fa86-137">Requirement</span></span> | <span data-ttu-id="3fa86-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3fa86-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa86-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fa86-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa86-140">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3fa86-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fa86-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fa86-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa86-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3fa86-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3fa86-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3fa86-143">Namespace</span></span><br/>                | <span data-ttu-id="3fa86-144">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3fa86-144">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3fa86-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3fa86-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fa86-146"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fa86-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fa86-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3fa86-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fa86-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fa86-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa86-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fa86-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa86-150">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="3fa86-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

