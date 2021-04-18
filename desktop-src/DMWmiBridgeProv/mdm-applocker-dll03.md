---
title: Класс MDM_AppLocker_DLL03
description: Класс MDM \_ AppLocker \_ DLL03 определяет ограничения политики для обработки DLL-файлов.
ms.assetid: 956b2ec0-f8a8-41d1-a571-01e73c4cebf9
keywords:
- Класс MDM_AppLocker_DLL03
- MDM_AppLocker_DLL03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_DLL03
- MDM_AppLocker_DLL03.InstanceID
- MDM_AppLocker_DLL03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c332a7d606b21ed9641c3c25f10a011cf7bea6e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654695"
---
# <a name="mdm_applocker_dll03-class"></a><span data-ttu-id="3dc1e-105">\_Класс MDM AppLocker \_ DLL03</span><span class="sxs-lookup"><span data-stu-id="3dc1e-105">MDM\_AppLocker\_DLL03 class</span></span>

<span data-ttu-id="3dc1e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3dc1e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3dc1e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3dc1e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3dc1e-108">Класс **MDM \_ AppLocker \_ DLL03** определяет ограничения политики для обработки DLL-файлов.</span><span class="sxs-lookup"><span data-stu-id="3dc1e-108">The **MDM\_AppLocker\_DLL03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="3dc1e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3dc1e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc1e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dc1e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_DLL03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="3dc1e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3dc1e-111">Members</span></span>

<span data-ttu-id="3dc1e-112">Класс **MDM \_ AppLocker \_ DLL03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3dc1e-112">The **MDM\_AppLocker\_DLL03** class has these types of members:</span></span>

-   [<span data-ttu-id="3dc1e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3dc1e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3dc1e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3dc1e-114">Properties</span></span>

<span data-ttu-id="3dc1e-115">Класс **MDM \_ AppLocker \_ DLL03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3dc1e-115">The **MDM\_AppLocker\_DLL03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3dc1e-116">**енфорцементмоде**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dc1e-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dc1e-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dc1e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3dc1e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dc1e-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dc1e-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3dc1e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dc1e-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3dc1e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3dc1e-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="3dc1e-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="3dc1e-124">**нонинтерактивепроцессенфорцемент**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dc1e-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dc1e-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dc1e-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3dc1e-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dc1e-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dc1e-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3dc1e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dc1e-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3dc1e-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3dc1e-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="3dc1e-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="3dc1e-132">Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/аппликатионлаунчрестриктионс"</span><span class="sxs-lookup"><span data-stu-id="3dc1e-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="3dc1e-133">**Политика**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dc1e-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3dc1e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dc1e-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dc1e-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3dc1e-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3dc1e-136">Requirements</span></span>



| <span data-ttu-id="3dc1e-137">Требование</span><span class="sxs-lookup"><span data-stu-id="3dc1e-137">Requirement</span></span> | <span data-ttu-id="3dc1e-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3dc1e-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc1e-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dc1e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc1e-140">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3dc1e-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3dc1e-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dc1e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc1e-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3dc1e-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3dc1e-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3dc1e-143">Namespace</span></span><br/>                | <span data-ttu-id="3dc1e-144">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3dc1e-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3dc1e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3dc1e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dc1e-146"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dc1e-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dc1e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3dc1e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dc1e-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dc1e-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dc1e-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dc1e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc1e-150">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="3dc1e-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

