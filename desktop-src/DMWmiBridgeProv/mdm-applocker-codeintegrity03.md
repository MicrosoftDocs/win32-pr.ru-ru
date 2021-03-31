---
title: Класс MDM_AppLocker_CodeIntegrity03
description: Класс MDM \_ AppLocker \_ CodeIntegrity03 определяет политику для обеспечения целостности кода.
ms.assetid: 8e7649b4-2e89-4d79-923e-3767e5b0ea52
keywords:
- Класс MDM_AppLocker_CodeIntegrity03
- MDM_AppLocker_CodeIntegrity03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_CodeIntegrity03
- MDM_AppLocker_CodeIntegrity03.InstanceID
- MDM_AppLocker_CodeIntegrity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff702f2887f47c1cc5fcebeb4b8ec9a08c450b8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802051"
---
# <a name="mdm_applocker_codeintegrity03-class"></a><span data-ttu-id="52a5c-105">\_Класс MDM AppLocker \_ CodeIntegrity03</span><span class="sxs-lookup"><span data-stu-id="52a5c-105">MDM\_AppLocker\_CodeIntegrity03 class</span></span>

<span data-ttu-id="52a5c-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="52a5c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="52a5c-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="52a5c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="52a5c-108">Класс **MDM \_ AppLocker \_ CodeIntegrity03** определяет политику для обеспечения целостности кода.</span><span class="sxs-lookup"><span data-stu-id="52a5c-108">The **MDM\_AppLocker\_CodeIntegrity03** class defines the policy for Code Integrity.</span></span>

<span data-ttu-id="52a5c-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="52a5c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a5c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52a5c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_CodeIntegrity03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="52a5c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="52a5c-111">Members</span></span>

<span data-ttu-id="52a5c-112">Класс **MDM \_ AppLocker \_ CodeIntegrity03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="52a5c-112">The **MDM\_AppLocker\_CodeIntegrity03** class has these types of members:</span></span>

-   [<span data-ttu-id="52a5c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="52a5c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52a5c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="52a5c-114">Properties</span></span>

<span data-ttu-id="52a5c-115">Класс **MDM \_ AppLocker \_ CodeIntegrity03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="52a5c-115">The **MDM\_AppLocker\_CodeIntegrity03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52a5c-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="52a5c-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52a5c-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="52a5c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52a5c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52a5c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52a5c-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52a5c-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="52a5c-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="52a5c-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="52a5c-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="52a5c-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52a5c-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="52a5c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52a5c-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52a5c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52a5c-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52a5c-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="52a5c-125">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="52a5c-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="52a5c-126">Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/аппликатионлаунчрестриктионс"</span><span class="sxs-lookup"><span data-stu-id="52a5c-126">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="52a5c-127">**Политика**</span><span class="sxs-lookup"><span data-stu-id="52a5c-127">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52a5c-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="52a5c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52a5c-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="52a5c-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="52a5c-130">Квалификаторы: **октетстринг**</span><span class="sxs-lookup"><span data-stu-id="52a5c-130">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52a5c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="52a5c-131">Requirements</span></span>



| <span data-ttu-id="52a5c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="52a5c-132">Requirement</span></span> | <span data-ttu-id="52a5c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="52a5c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52a5c-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52a5c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="52a5c-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="52a5c-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52a5c-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52a5c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="52a5c-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="52a5c-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="52a5c-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="52a5c-138">Namespace</span></span><br/>                | <span data-ttu-id="52a5c-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="52a5c-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="52a5c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="52a5c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52a5c-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52a5c-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="52a5c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="52a5c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52a5c-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52a5c-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a5c-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52a5c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a5c-145">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="52a5c-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

