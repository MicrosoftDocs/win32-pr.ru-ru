---
title: Класс MDM_WindowsAdvancedThreatProtection
description: Класс MDM \_ виндовсадванцедсреатпротектион используется для подключения и отключение конечных точек для Advanced Threat Protection в Защитнике Windows (WDATP).
ms.assetid: 7a95253e-6d13-4c1b-b78d-c56c6378f7c3
keywords:
- Класс MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection класс, описание
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection.InstanceID
- MDM_WindowsAdvancedThreatProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369406a3c8bcf982aeb18b4bbb53c1af4983e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654585"
---
# <a name="mdm_windowsadvancedthreatprotection-class"></a><span data-ttu-id="adb1e-105">\_Класс MDM виндовсадванцедсреатпротектион</span><span class="sxs-lookup"><span data-stu-id="adb1e-105">MDM\_WindowsAdvancedThreatProtection class</span></span>

<span data-ttu-id="adb1e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="adb1e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="adb1e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="adb1e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="adb1e-108">Класс **MDM \_ виндовсадванцедсреатпротектион** используется для подключения и отключение конечных точек для Advanced Threat Protection в Защитнике Windows (WDATP).</span><span class="sxs-lookup"><span data-stu-id="adb1e-108">The **MDM\_WindowsAdvancedThreatProtection** class is used to onboard and offboard endpoints for Windows Defender Advanced Threat Protection (WDATP).</span></span>

<span data-ttu-id="adb1e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="adb1e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb1e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adb1e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection
{
  string InstanceID;
  string ParentID;
  string Onboarding;
  string Offboarding;
};
```

## <a name="members"></a><span data-ttu-id="adb1e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="adb1e-111">Members</span></span>

<span data-ttu-id="adb1e-112">Класс **MDM \_ виндовсадванцедсреатпротектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="adb1e-112">The **MDM\_WindowsAdvancedThreatProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="adb1e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="adb1e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="adb1e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="adb1e-114">Properties</span></span>

<span data-ttu-id="adb1e-115">Класс **MDM \_ виндовсадванцедсреатпротектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="adb1e-115">The **MDM\_WindowsAdvancedThreatProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="adb1e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="adb1e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adb1e-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="adb1e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adb1e-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="adb1e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adb1e-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="adb1e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="adb1e-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="adb1e-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="adb1e-121">Для этого класса строка имеет значение "Виндовсадванцедсреатпротектион".</span><span class="sxs-lookup"><span data-stu-id="adb1e-121">For this class, the string is "WindowsAdvancedThreatProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="adb1e-122">Отключение</span><span class="sxs-lookup"><span data-stu-id="adb1e-122">Offboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#offboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="adb1e-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="adb1e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adb1e-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="adb1e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="adb1e-125">[Подключение](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding).</span><span class="sxs-lookup"><span data-stu-id="adb1e-125">[Onboarding](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding)</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adb1e-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="adb1e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adb1e-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="adb1e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="adb1e-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="adb1e-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adb1e-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="adb1e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adb1e-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="adb1e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adb1e-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="adb1e-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="adb1e-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="adb1e-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="adb1e-133">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="adb1e-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adb1e-134">Требования</span><span class="sxs-lookup"><span data-stu-id="adb1e-134">Requirements</span></span>



| <span data-ttu-id="adb1e-135">Требование</span><span class="sxs-lookup"><span data-stu-id="adb1e-135">Requirement</span></span> | <span data-ttu-id="adb1e-136">Значение</span><span class="sxs-lookup"><span data-stu-id="adb1e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adb1e-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adb1e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="adb1e-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="adb1e-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="adb1e-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adb1e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="adb1e-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="adb1e-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="adb1e-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="adb1e-141">Namespace</span></span><br/>                | <span data-ttu-id="adb1e-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="adb1e-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="adb1e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="adb1e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adb1e-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="adb1e-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="adb1e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="adb1e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adb1e-146"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adb1e-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adb1e-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adb1e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb1e-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="adb1e-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

