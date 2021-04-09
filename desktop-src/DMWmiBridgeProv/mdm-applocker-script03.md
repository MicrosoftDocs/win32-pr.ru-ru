---
title: Класс MDM_AppLocker_Script03
description: Класс MDM \_ AppLocker \_ Script03 определяет ограничения политики для обработки DLL-файлов.
ms.assetid: 61fada02-7245-4825-945c-b41e9eff8e74
keywords:
- Класс MDM_AppLocker_Script03
- MDM_AppLocker_Script03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_Script03
- MDM_AppLocker_Script03.InstanceID
- MDM_AppLocker_Script03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402efedb1e15a0ea0df3dea654328de4ba0ddd86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071994"
---
# <a name="mdm_applocker_script03-class"></a><span data-ttu-id="200c2-105">\_Класс MDM AppLocker \_ Script03</span><span class="sxs-lookup"><span data-stu-id="200c2-105">MDM\_AppLocker\_Script03 class</span></span>

<span data-ttu-id="200c2-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="200c2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="200c2-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="200c2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="200c2-108">Класс **MDM \_ AppLocker \_ Script03** определяет ограничения политики для обработки DLL-файлов.</span><span class="sxs-lookup"><span data-stu-id="200c2-108">The **MDM\_AppLocker\_Script03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="200c2-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="200c2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="200c2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="200c2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_Script03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="200c2-111">Члены</span><span class="sxs-lookup"><span data-stu-id="200c2-111">Members</span></span>

<span data-ttu-id="200c2-112">Класс **MDM \_ AppLocker \_ Script03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="200c2-112">The **MDM\_AppLocker\_Script03** class has these types of members:</span></span>

-   [<span data-ttu-id="200c2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="200c2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="200c2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="200c2-114">Properties</span></span>

<span data-ttu-id="200c2-115">Класс **MDM \_ AppLocker \_ Script03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="200c2-115">The **MDM\_AppLocker\_Script03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="200c2-116">**енфорцементмоде**</span><span class="sxs-lookup"><span data-stu-id="200c2-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="200c2-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="200c2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="200c2-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="200c2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="200c2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="200c2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="200c2-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="200c2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="200c2-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="200c2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="200c2-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="200c2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="200c2-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="200c2-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="200c2-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="200c2-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="200c2-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="200c2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="200c2-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="200c2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="200c2-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="200c2-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="200c2-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="200c2-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="200c2-129">Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/аппликатионлаунчрестриктионс"</span><span class="sxs-lookup"><span data-stu-id="200c2-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="200c2-130">**Политика**</span><span class="sxs-lookup"><span data-stu-id="200c2-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="200c2-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="200c2-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="200c2-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="200c2-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="200c2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="200c2-133">Requirements</span></span>



| <span data-ttu-id="200c2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="200c2-134">Requirement</span></span> | <span data-ttu-id="200c2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="200c2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200c2-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="200c2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="200c2-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="200c2-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="200c2-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="200c2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="200c2-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="200c2-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="200c2-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="200c2-140">Namespace</span></span><br/>                | <span data-ttu-id="200c2-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="200c2-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="200c2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="200c2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="200c2-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="200c2-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="200c2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="200c2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="200c2-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="200c2-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200c2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="200c2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200c2-147">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="200c2-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

