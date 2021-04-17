---
description: Метод Конфигурефеатуре объекта Installer настраивает установленное состояние компонента продукта.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configметод Урефеатуре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652289"
---
# <a name="installerconfigurefeature-method"></a><span data-ttu-id="bc8ff-103">Installer.Configметод Урефеатуре</span><span class="sxs-lookup"><span data-stu-id="bc8ff-103">Installer.ConfigureFeature method</span></span>

<span data-ttu-id="bc8ff-104">Метод **конфигурефеатуре** объекта [**Installer**](installer-object.md) настраивает установленное состояние компонента продукта.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-104">The **ConfigureFeature** method of the [**Installer**](installer-object.md) object configures the installed state of a product feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc8ff-105">Syntax</span></span>


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="bc8ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc8ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8ff-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="bc8ff-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="bc8ff-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="bc8ff-109">*Компонент*</span><span class="sxs-lookup"><span data-stu-id="bc8ff-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="bc8ff-110">Указывает идентификатор компонента для настраиваемого компонента.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-110">Specifies the feature ID of the feature to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="bc8ff-111">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="bc8ff-111">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="bc8ff-112">Указывает состояние установки для компонента.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-112">Specifies the installation state for the feature.</span></span> <span data-ttu-id="bc8ff-113">Этот параметр должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-113">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="bc8ff-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bc8ff-114">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="bc8ff-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bc8ff-115">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="bc8ff-116"><dt>**мсиинсталлстатеадвертисед**</dt></span><span class="sxs-lookup"><span data-stu-id="bc8ff-116"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="bc8ff-117">Эта функция объявлена</span><span class="sxs-lookup"><span data-stu-id="bc8ff-117">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="bc8ff-118"><dt>**мсиинсталлстателокал**</dt></span><span class="sxs-lookup"><span data-stu-id="bc8ff-118"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="bc8ff-119">Этот компонент устанавливается локально.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-119">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="bc8ff-120"><dt>**мсиинсталлстатеабсент**</dt></span><span class="sxs-lookup"><span data-stu-id="bc8ff-120"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="bc8ff-121">Компонент удален.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-121">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="bc8ff-122"><dt>**мсиинсталлстатесаурце**</dt></span><span class="sxs-lookup"><span data-stu-id="bc8ff-122"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="bc8ff-123">Компонент устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-123">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="bc8ff-124"><dt>**мсиинсталлстатедефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="bc8ff-124"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="bc8ff-125">Компонент устанавливается в расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-125">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8ff-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc8ff-126">Return value</span></span>

<span data-ttu-id="bc8ff-127">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8ff-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bc8ff-128">Requirements</span></span>



| <span data-ttu-id="bc8ff-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bc8ff-129">Requirement</span></span> | <span data-ttu-id="bc8ff-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bc8ff-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8ff-131">Версия</span><span class="sxs-lookup"><span data-stu-id="bc8ff-131">Version</span></span><br/> | <span data-ttu-id="bc8ff-132">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc8ff-133">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc8ff-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bc8ff-134">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc8ff-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bc8ff-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bc8ff-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc8ff-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc8ff-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bc8ff-137">IID</span><span class="sxs-lookup"><span data-stu-id="bc8ff-137">IID</span></span><br/>     | <span data-ttu-id="bc8ff-138">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bc8ff-138">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="bc8ff-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc8ff-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8ff-140">**мсиконфигурефеатуре**</span><span class="sxs-lookup"><span data-stu-id="bc8ff-140">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[<span data-ttu-id="bc8ff-141">Функции установки и настройки</span><span class="sxs-lookup"><span data-stu-id="bc8ff-141">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




