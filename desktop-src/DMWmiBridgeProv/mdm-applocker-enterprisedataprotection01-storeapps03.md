---
title: Класс MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
description: Класс MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03 фиксирует список приложений Windows, которым разрешено работать с корпоративными данными. Следует использовать в сочетании с параметрами в./вендор/мсфт/Полици/конфигсаурце/датапротектион.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- Класс MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240f641e542bbbe0c71fd686e2d9df3908b9bab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989332"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a><span data-ttu-id="26bb1-106">\_Класс MDM AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03</span><span class="sxs-lookup"><span data-stu-id="26bb1-106">MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03 class</span></span>

<span data-ttu-id="26bb1-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="26bb1-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26bb1-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="26bb1-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="26bb1-109">Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** фиксирует список приложений Windows, которым разрешено работать с корпоративными данными.</span><span class="sxs-lookup"><span data-stu-id="26bb1-109">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class captures the list of Windows apps that are allowed to handle enterprise data.</span></span> <span data-ttu-id="26bb1-110">Следует использовать в сочетании с параметрами в./вендор/мсфт/Полици/конфигсаурце/датапротектион.</span><span class="sxs-lookup"><span data-stu-id="26bb1-110">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="26bb1-111">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="26bb1-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26bb1-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26bb1-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="26bb1-113">Члены</span><span class="sxs-lookup"><span data-stu-id="26bb1-113">Members</span></span>

<span data-ttu-id="26bb1-114">Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="26bb1-114">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="26bb1-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="26bb1-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26bb1-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="26bb1-116">Properties</span></span>

<span data-ttu-id="26bb1-117">Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="26bb1-117">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26bb1-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26bb1-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26bb1-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26bb1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-121">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26bb1-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26bb1-122">Определяет ограничения для запуска приложений из Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="26bb1-122">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="26bb1-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="26bb1-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26bb1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26bb1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26bb1-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26bb1-127">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="26bb1-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="26bb1-128">Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/ентерприседатапротектион/*GROUPING*"</span><span class="sxs-lookup"><span data-stu-id="26bb1-128">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="26bb1-129">**Политика**</span><span class="sxs-lookup"><span data-stu-id="26bb1-129">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26bb1-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26bb1-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26bb1-132">Требования</span><span class="sxs-lookup"><span data-stu-id="26bb1-132">Requirements</span></span>



| <span data-ttu-id="26bb1-133">Требование</span><span class="sxs-lookup"><span data-stu-id="26bb1-133">Requirement</span></span> | <span data-ttu-id="26bb1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="26bb1-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bb1-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26bb1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="26bb1-136">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="26bb1-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26bb1-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26bb1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="26bb1-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="26bb1-138">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="26bb1-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26bb1-139">Namespace</span></span><br/>                | <span data-ttu-id="26bb1-140">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="26bb1-140">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="26bb1-141">MOF</span><span class="sxs-lookup"><span data-stu-id="26bb1-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26bb1-142"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26bb1-142"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="26bb1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="26bb1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26bb1-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26bb1-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26bb1-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26bb1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26bb1-146">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="26bb1-146">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

