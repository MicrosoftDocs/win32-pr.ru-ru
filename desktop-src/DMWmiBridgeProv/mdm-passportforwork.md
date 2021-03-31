---
title: Класс MDM_PassportForWork
description: MDM \_ пасспортфорворк используется для инициализации Windows Hello для бизнеса.
ms.assetid: 49bba780-e26f-463d-97ae-e095ea16be87
keywords:
- Класс MDM_PassportForWork
- MDM_PassportForWork класс, описание
topic_type:
- apiref
api_name:
- MDM_PassportForWork
- MDM_PassportForWork.InstanceID
- MDM_PassportForWork.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7f061c0ab8f0405e8f0e6a6d43d8d896c62f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071439"
---
# <a name="mdm_passportforwork-class"></a><span data-ttu-id="cde74-105">\_Класс MDM пасспортфорворк</span><span class="sxs-lookup"><span data-stu-id="cde74-105">MDM\_PassportForWork class</span></span>

<span data-ttu-id="cde74-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="cde74-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cde74-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="cde74-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cde74-108">**MDM \_ пасспортфорворк** используется для инициализации Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="cde74-108">The **MDM\_PassportForWork** is used to provision Windows Hello for Business.</span></span>

<span data-ttu-id="cde74-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cde74-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde74-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cde74-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
};
```

## <a name="members"></a><span data-ttu-id="cde74-111">Члены</span><span class="sxs-lookup"><span data-stu-id="cde74-111">Members</span></span>

<span data-ttu-id="cde74-112">Класс **MDM \_ пасспортфорворк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cde74-112">The **MDM\_PassportForWork** class has these types of members:</span></span>

-   [<span data-ttu-id="cde74-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="cde74-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cde74-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="cde74-114">Properties</span></span>

<span data-ttu-id="cde74-115">Класс **MDM \_ пасспортфорворк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cde74-115">The **MDM\_PassportForWork** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cde74-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cde74-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde74-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde74-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde74-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde74-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde74-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cde74-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cde74-120">Указывает идентификатор клиента в формате глобального уникального идентификатора (GUID) без фигурных скобок ({,}), которые будут использоваться как часть подготовки и управления Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="cde74-120">Specifies the Tenant ID in the format of a Globally Unique Identifier (GUID) without curly braces ( { , } ), which will be used as part of Windows Hello for Business provisioning and management.</span></span>

</dd> <dt>

<span data-ttu-id="cde74-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cde74-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde74-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde74-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde74-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde74-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde74-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cde74-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cde74-125">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="cde74-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="cde74-126">Для этого класса строка имеет значение "./вендор/мсфт/пасспортфорворк/"</span><span class="sxs-lookup"><span data-stu-id="cde74-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="cde74-127">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="cde74-127">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde74-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cde74-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cde74-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="cde74-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cde74-130">Требования</span><span class="sxs-lookup"><span data-stu-id="cde74-130">Requirements</span></span>



| <span data-ttu-id="cde74-131">Требование</span><span class="sxs-lookup"><span data-stu-id="cde74-131">Requirement</span></span> | <span data-ttu-id="cde74-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cde74-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cde74-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cde74-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cde74-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cde74-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cde74-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cde74-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cde74-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cde74-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cde74-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cde74-137">Namespace</span></span><br/>                | <span data-ttu-id="cde74-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="cde74-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cde74-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cde74-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cde74-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cde74-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cde74-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cde74-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde74-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde74-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cde74-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cde74-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde74-144">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="cde74-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

