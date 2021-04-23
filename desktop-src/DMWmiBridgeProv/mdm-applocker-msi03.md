---
title: Класс MDM_AppLocker_MSI03
description: Класс MDM \_ AppLocker \_ MSI03 определяет ограничения политики для обработки MSI файлов.
ms.assetid: b7b6602d-38b7-46f0-9542-71228ab0c303
keywords:
- Класс MDM_AppLocker_MSI03
- MDM_AppLocker_MSI03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_MSI03
- MDM_AppLocker_MSI03.InstanceID
- MDM_AppLocker_MSI03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5bd17a979ac0e4a6dcbbc07a38ba72bfd50ede4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803826"
---
# <a name="mdm_applocker_msi03-class"></a><span data-ttu-id="0b0bd-105">\_Класс MDM AppLocker \_ MSI03</span><span class="sxs-lookup"><span data-stu-id="0b0bd-105">MDM\_AppLocker\_MSI03 class</span></span>

<span data-ttu-id="0b0bd-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="0b0bd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b0bd-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="0b0bd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b0bd-108">Класс **MDM \_ AppLocker \_ MSI03** определяет ограничения политики для обработки MSI файлов.</span><span class="sxs-lookup"><span data-stu-id="0b0bd-108">The **MDM\_AppLocker\_MSI03** class defines the policy restrictions for processing MSI files.</span></span>

<span data-ttu-id="0b0bd-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0b0bd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0bd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b0bd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_MSI03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="0b0bd-111">Члены</span><span class="sxs-lookup"><span data-stu-id="0b0bd-111">Members</span></span>

<span data-ttu-id="0b0bd-112">Класс **MDM \_ AppLocker \_ MSI03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0b0bd-112">The **MDM\_AppLocker\_MSI03** class has these types of members:</span></span>

-   [<span data-ttu-id="0b0bd-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0b0bd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b0bd-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0b0bd-114">Properties</span></span>

<span data-ttu-id="0b0bd-115">Класс **MDM \_ AppLocker \_ MSI03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0b0bd-115">The **MDM\_AppLocker\_MSI03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0b0bd-116">**енфорцементмоде**</span><span class="sxs-lookup"><span data-stu-id="0b0bd-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0bd-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0b0bd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0bd-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0b0bd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b0bd-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b0bd-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0bd-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0b0bd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0bd-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b0bd-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0bd-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b0bd-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b0bd-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="0b0bd-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="0b0bd-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b0bd-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0bd-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0b0bd-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0bd-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b0bd-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0bd-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b0bd-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b0bd-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="0b0bd-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="0b0bd-129">Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/аппликатионлаунчрестриктионс"</span><span class="sxs-lookup"><span data-stu-id="0b0bd-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="0b0bd-130">**Политика**</span><span class="sxs-lookup"><span data-stu-id="0b0bd-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0bd-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0b0bd-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0bd-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0b0bd-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b0bd-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0b0bd-133">Requirements</span></span>



| <span data-ttu-id="0b0bd-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0b0bd-134">Requirement</span></span> | <span data-ttu-id="0b0bd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0b0bd-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0bd-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b0bd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0b0bd-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0b0bd-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b0bd-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b0bd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0b0bd-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0b0bd-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b0bd-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0b0bd-140">Namespace</span></span><br/>                | <span data-ttu-id="0b0bd-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="0b0bd-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0b0bd-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0b0bd-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b0bd-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b0bd-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b0bd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0b0bd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b0bd-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b0bd-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b0bd-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b0bd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0bd-147">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="0b0bd-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

