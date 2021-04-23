---
description: Для каждого продукта, указанного пакетом обновления в качестве право на получение исправления, метод Апплипатч объекта Installer вызывает установку и задает для свойства PATCH путь к пакету обновления.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Метод Installer. Апплипатч
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651912"
---
# <a name="installerapplypatch-method"></a><span data-ttu-id="0d0b9-103">Метод Installer. Апплипатч</span><span class="sxs-lookup"><span data-stu-id="0d0b9-103">Installer.ApplyPatch method</span></span>

<span data-ttu-id="0d0b9-104">Для каждого продукта, указанного пакетом обновления в качестве право на получение исправления, метод **апплипатч** объекта [**Installer**](installer-object.md) вызывает установку и задает для свойства [**Patch**](patch.md) путь к пакету обновления.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-104">For each product listed by the patch package as eligible to receive the patch, the **ApplyPatch** method of the [**Installer**](installer-object.md) object invokes an installation and sets the [**PATCH**](patch.md) property to the path of the patch package.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d0b9-105">Syntax</span></span>


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a><span data-ttu-id="0d0b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d0b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d0b9-107">*патчпаккаже*</span><span class="sxs-lookup"><span data-stu-id="0d0b9-107">*PatchPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="0d0b9-108">Указывает путь к пакету исправлений.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-108">Specifies a path to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="0d0b9-109">*инсталлпаккаже*</span><span class="sxs-lookup"><span data-stu-id="0d0b9-109">*InstallPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="0d0b9-110">Если для *инсталлтипе* задано значение Мсиинсталлтипенетворкимаже, *инсталлпаккаже* указывает путь к продукту, для которого устанавливается исправление.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-110">If *InstallType* is set to msiInstallTypeNetworkImage, *InstallPackage* specifies the path to the product that is to be patched.</span></span> <span data-ttu-id="0d0b9-111">Если для *инсталлтипе* задано значение мсиинсталлтипедефаулт, а *инсталлпаккаже* имеет значение 0, установщик применяет исправление ко всем соответствующим продуктам, перечисленным в пакете исправлений.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-111">If *InstallType* is set to msiInstallTypeDefault and *InstallPackage* is set to 0, the installer applies the patch to every eligible product listed in the patch package.</span></span>

<span data-ttu-id="0d0b9-112">Если *инсталлтипе* имеет значение мсиинсталлтипесинглеинстанце, установщик применяет исправление к продукту, указанному в *инсталлпаккаже*.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-112">If *InstallType* is msiInstallTypeSingleInstance, the installer applies the patch to the product specified by *InstallPackage*.</span></span> <span data-ttu-id="0d0b9-113">В этом случае другие подходящие продукты, перечисленные в пакете исправлений, игнорируются, а параметр *инсталлпаккаже* содержит строку с завершающим нулем, представляющую код продукта экземпляра для исправления.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-113">In this case, other eligible products listed in the patch package are ignored and the *InstallPackage* parameter contains the null-terminated string representing the product code of the instance to patch.</span></span> <span data-ttu-id="0d0b9-114">Для этого типа установки требуется версия установщик Windows, поставляемая с Windows Server 2003 или более поздней версии или установщик Windows XP SP1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-114">This type of installation requires the Windows Installer version shipped with the Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span>

</dd> <dt>

<span data-ttu-id="0d0b9-115">*InstallType*</span><span class="sxs-lookup"><span data-stu-id="0d0b9-115">*InstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="0d0b9-116">Этот параметр указывает тип установки для исправления.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-116">This parameter specifies the type of installation to patch.</span></span> <span data-ttu-id="0d0b9-117">Параметр *инсталлтипе* игнорируется, если *инсталлпаккаже* опущен.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-117">The *InstallType* parameter is ignored if *InstallPackage* is omitted.</span></span>



| <span data-ttu-id="0d0b9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0d0b9-118">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="0d0b9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0d0b9-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <span data-ttu-id="0d0b9-120"><dt>**мсиинсталлтипенетворкимаже**</dt></span><span class="sxs-lookup"><span data-stu-id="0d0b9-120"><dt>**msiInstallTypeNetworkImage**</dt></span></span> </dl> | <span data-ttu-id="0d0b9-121">Указывает административную установку.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-121">Indicates a administrative installation.</span></span> <span data-ttu-id="0d0b9-122">В этом случае для *инсталлпаккаже* необходимо задать путь к пакету.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-122">In this case, *InstallPackage* must be set to a package path.</span></span> <span data-ttu-id="0d0b9-123">Значение 1 для Мсиинсталлтипенетворкимаже указывает административную установку.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-123">A value of 1 for msiInstallTypeNetworkImage specifies a administrative installation.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <span data-ttu-id="0d0b9-124"><dt>**мсиинсталлтипедефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="0d0b9-124"><dt>**msiInstallTypeDefault**</dt></span></span> </dl>                     | <span data-ttu-id="0d0b9-125">Ищет в системе продукты для исправления.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-125">Searches system for products to patch.</span></span> <span data-ttu-id="0d0b9-126">В этом случае *инсталлпаккаже* должно быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-126">In this case, *InstallPackage* must be an empty string.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <span data-ttu-id="0d0b9-127"><dt>**мсиинсталлсинглеинстанце**</dt></span><span class="sxs-lookup"><span data-stu-id="0d0b9-127"><dt>**msiInstallSingleInstance**</dt></span></span> </dl>         | <span data-ttu-id="0d0b9-128">Исправление продукта, указанного параметром *инсталлпаккаже*.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-128">Patch the product specified by *InstallPackage*.</span></span> <span data-ttu-id="0d0b9-129">*Инсталлпаккаже* — это код продукта экземпляра для исправления.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-129">*InstallPackage* is the product code of the instance to patch.</span></span> <span data-ttu-id="0d0b9-130">Для этого типа установки требуется версия установщик Windows, поставляемая с Windows Server 2003 или более поздней версии или установщик Windows XP SP1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-130">This type of installation requires the Windows Installer version shipped with Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span> <span data-ttu-id="0d0b9-131">Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="0d0b9-131">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d0b9-132">*CommandLine*</span><span class="sxs-lookup"><span data-stu-id="0d0b9-132">*CommandLine*</span></span> 
</dt> <dd>

<span data-ttu-id="0d0b9-133">Задает параметры свойств, заданные в командной строке.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-133">Specifies property settings being set on the command line.</span></span> <span data-ttu-id="0d0b9-134">См. раздел "Примечания".</span><span class="sxs-lookup"><span data-stu-id="0d0b9-134">See Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d0b9-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d0b9-135">Return value</span></span>

<span data-ttu-id="0d0b9-136">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-136">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0b9-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d0b9-137">Remarks</span></span>

<span data-ttu-id="0d0b9-138">Так как разделителем списков для преобразований, источников и исправлений является точка с запятой, этот символ не следует использовать для имен файлов и путей.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-138">Because the list delimiter for transforms, sources, and patches is a semicolon, this character should not be used for file names or paths.</span></span>

<span data-ttu-id="0d0b9-139">Свойство [**REINSTALL**](reinstall.md) требуется при применении [небольшого обновления](small-updates.md) или исправления [незначительного обновления](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="0d0b9-139">The [**REINSTALL**](reinstall.md) property is required when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="0d0b9-140">Без этого свойства исправление регистрируется в системе, но не может обновлять файлы.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-140">Without this property, the patch is registered on the system but cannot update files.</span></span>

<span data-ttu-id="0d0b9-141">**Установщик Windows 2,0:** При применении [небольшого обновления](small-updates.md) или исправления [незначительного обновления](minor-upgrades.md) необходимо задать свойство [**переустановки**](reinstall.md) в командной строке.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-141">**Windows Installer 2.0:** You must set the [**REINSTALL**](reinstall.md) property on the command line when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="0d0b9-142">Для исправлений, не использующих [Пользовательский тип действия 51](custom-action-type-51.md) для автоматической установки свойств **REINSTALL** и [**REINSTALLMODE**](reinstallmode.md) , необходимо явно задать свойство **REINSTALL** с параметром *commandline* .</span><span class="sxs-lookup"><span data-stu-id="0d0b9-142">For patches that do not use a [Custom Action Type 51](custom-action-type-51.md) to automatically set the **REINSTALL** and [**REINSTALLMODE**](reinstallmode.md) properties, the **REINSTALL** property must be explicitly set with the *CommandLine* parameter.</span></span> <span data-ttu-id="0d0b9-143">Задайте свойство **REINSTALL** , чтобы получить список функций, затронутых исправлением, или используйте практическую настройку по умолчанию (REINSTALL = ALL).</span><span class="sxs-lookup"><span data-stu-id="0d0b9-143">Set the **REINSTALL** property to list the features affected by the patch, or use a practical default setting of "REINSTALL=ALL".</span></span> <span data-ttu-id="0d0b9-144">Значение свойства **REINSTALLMODE** по умолчанию — "omus".</span><span class="sxs-lookup"><span data-stu-id="0d0b9-144">The default value of the **REINSTALLMODE** property is "omus".</span></span>

<span data-ttu-id="0d0b9-145">**Установщик Windows 3,0 и более поздних версий:** Начиная с версии установщик Windows 3,0, свойство [**REINSTALL**](reinstall.md) настраивается установщиком и не требуется задавать в командной строке.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-145">**Windows Installer 3.0 and later:** Beginning with Windows Installer version 3.0, the [**REINSTALL**](reinstall.md) property is configured by the installer and does not need to be set on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0b9-146">Требования</span><span class="sxs-lookup"><span data-stu-id="0d0b9-146">Requirements</span></span>



| <span data-ttu-id="0d0b9-147">Требование</span><span class="sxs-lookup"><span data-stu-id="0d0b9-147">Requirement</span></span> | <span data-ttu-id="0d0b9-148">Значение</span><span class="sxs-lookup"><span data-stu-id="0d0b9-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0b9-149">Версия</span><span class="sxs-lookup"><span data-stu-id="0d0b9-149">Version</span></span><br/> | <span data-ttu-id="0d0b9-150">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-150">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0d0b9-151">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-151">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0d0b9-152">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0d0b9-152">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="0d0b9-153">DLL</span><span class="sxs-lookup"><span data-stu-id="0d0b9-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d0b9-154"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d0b9-154"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="0d0b9-155">IID</span><span class="sxs-lookup"><span data-stu-id="0d0b9-155">IID</span></span><br/>     | <span data-ttu-id="0d0b9-156">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0d0b9-156">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="0d0b9-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d0b9-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0b9-158">**мсиапплипатч**</span><span class="sxs-lookup"><span data-stu-id="0d0b9-158">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[<span data-ttu-id="0d0b9-159">Сведения о свойствах</span><span class="sxs-lookup"><span data-stu-id="0d0b9-159">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="0d0b9-160">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="0d0b9-160">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




