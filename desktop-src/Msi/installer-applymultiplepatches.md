---
description: Метод Апплимултиплепатчес применяет один или несколько исправлений к продуктам, которые могут получить исправление. Метод задает свойство PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Метод Installer. Апплимултиплепатчес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651913"
---
# <a name="installerapplymultiplepatches-method"></a><span data-ttu-id="d6b4f-104">Метод Installer. Апплимултиплепатчес</span><span class="sxs-lookup"><span data-stu-id="d6b4f-104">Installer.ApplyMultiplePatches method</span></span>

<span data-ttu-id="d6b4f-105">Метод **апплимултиплепатчес** применяет один или несколько исправлений к продуктам, которые могут получить исправление.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-105">The **ApplyMultiplePatches** method applies one or more patches to products that are eligible to receive the patch.</span></span> <span data-ttu-id="d6b4f-106">Метод задает свойство [**Patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="d6b4f-106">The method sets the [**PATCH**](patch.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b4f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6b4f-107">Syntax</span></span>


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a><span data-ttu-id="d6b4f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6b4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6b4f-109">*патчпаккажеслист*</span><span class="sxs-lookup"><span data-stu-id="d6b4f-109">*PatchPackagesList*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b4f-110">Строка, содержащая разделенный точками с запятой список путей к файлам исправлений.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-110">A string that contains a semicolon-delimited list of the paths to patch files.</span></span> <span data-ttu-id="d6b4f-111">Например: "" c: \\ \\ кэш скачивания SUS \\ \\ Office \\ с пакетом обновления 1 (SP1). MSP; в. \\ \\ скачивание с \\ \\ пакетом обновления Office \\ QFE1. MSP; c: \\ SUS \\ download \\ кэша \\ Office \\ кфен. MSP ""</span><span class="sxs-lookup"><span data-stu-id="d6b4f-111">For example: ""c:\\sus\\download\\cache\\Office\\sp1.msp; c:\\sus\\download\\cache\\Office\\QFE1.msp;c:\\sus\\download\\cache\\Office\\QFEn.msp""</span></span>

</dd> <dt>

<span data-ttu-id="d6b4f-112">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="d6b4f-112">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b4f-113">Этот параметр предоставляет [**код**](productcode.md) продукта для исправления.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-113">This parameter provides the [**ProductCode**](productcode.md) of the product being patched.</span></span> <span data-ttu-id="d6b4f-114">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-114">This parameter is optional.</span></span> <span data-ttu-id="d6b4f-115">Если этот параметр имеет значение null, исправления применяются ко всем продуктам, которые могут принимать эти исправления.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-115">When this parameter is null, the patches are applied to all products that are eligible to receive these patches.</span></span>

</dd> <dt>

<span data-ttu-id="d6b4f-116">*сзпропертиеслист*</span><span class="sxs-lookup"><span data-stu-id="d6b4f-116">*szPropertiesList*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b4f-117">Строка, завершающаяся нулем, которая задает параметры свойства командной строки.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-117">A null-terminated string that specifies command-line property settings.</span></span> <span data-ttu-id="d6b4f-118">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-118">This parameter is optional.</span></span> <span data-ttu-id="d6b4f-119">См. раздел [о свойствах](about-properties.md) и [Установка значений общих свойств в командной строке](setting-public-property-values-on-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="d6b4f-119">See [About Properties](about-properties.md) and [Setting Public Property Values on the Command Line](setting-public-property-values-on-the-command-line.md).</span></span> <span data-ttu-id="d6b4f-120">Эти свойства являются общими для всех целевых продуктов.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-120">These properties are shared by all target products.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6b4f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6b4f-121">Return value</span></span>

<span data-ttu-id="d6b4f-122">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b4f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d6b4f-123">Requirements</span></span>



| <span data-ttu-id="d6b4f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d6b4f-124">Requirement</span></span> | <span data-ttu-id="d6b4f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d6b4f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b4f-126">Версия</span><span class="sxs-lookup"><span data-stu-id="d6b4f-126">Version</span></span><br/> | <span data-ttu-id="d6b4f-127">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6b4f-128">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6b4f-129">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6b4f-129">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="d6b4f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d6b4f-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6b4f-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6b4f-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="d6b4f-132">IID</span><span class="sxs-lookup"><span data-stu-id="d6b4f-132">IID</span></span><br/>     | <span data-ttu-id="d6b4f-133">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d6b4f-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="d6b4f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6b4f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b4f-135">Сведения о свойствах</span><span class="sxs-lookup"><span data-stu-id="d6b4f-135">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="d6b4f-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="d6b4f-136">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="d6b4f-137">**PATCH**</span><span class="sxs-lookup"><span data-stu-id="d6b4f-137">**PATCH**</span></span>](patch.md)
</dt> <dt>

[<span data-ttu-id="d6b4f-138">Установка значений открытых свойств в командной строке</span><span class="sxs-lookup"><span data-stu-id="d6b4f-138">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="d6b4f-139">**мсиапплимултиплепатчес**</span><span class="sxs-lookup"><span data-stu-id="d6b4f-139">**MsiApplyMultiplePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[<span data-ttu-id="d6b4f-140">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="d6b4f-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




