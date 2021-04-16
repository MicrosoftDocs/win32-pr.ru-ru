---
description: Метод Конфигурепродукт объекта Installer устанавливает или удаляет продукт.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configметод Урепродукт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652290"
---
# <a name="installerconfigureproduct-method"></a><span data-ttu-id="c3882-103">Installer.Configметод Урепродукт</span><span class="sxs-lookup"><span data-stu-id="c3882-103">Installer.ConfigureProduct method</span></span>

<span data-ttu-id="c3882-104">Метод **конфигурепродукт** объекта [**Installer**](installer-object.md) устанавливает или удаляет продукт.</span><span class="sxs-lookup"><span data-stu-id="c3882-104">The **ConfigureProduct** method of the [**Installer**](installer-object.md) object installs or uninstalls a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3882-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3882-105">Syntax</span></span>


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="c3882-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3882-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="c3882-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="c3882-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="c3882-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="c3882-109">*инсталллевел*</span><span class="sxs-lookup"><span data-stu-id="c3882-109">*InstallLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="c3882-110">Задает конфигурацию установки по умолчанию для продукта.</span><span class="sxs-lookup"><span data-stu-id="c3882-110">Specifies the default installation configuration of the product.</span></span> <span data-ttu-id="c3882-111">Параметр Инсталллевел игнорируется, и все компоненты устанавливаются, если параметру InstallState задано любое другое значение, отличное от Мсиинсталлстатедефаулт.</span><span class="sxs-lookup"><span data-stu-id="c3882-111">The InstallLevel parameter is ignored and all features are installed if the InstallState parameter is set to any other value than msiInstallStateDefault.</span></span>

<span data-ttu-id="c3882-112">Для установки подмножества доступных компонентов этот параметр должен быть равен 0 (установить с использованием уровней автора), 65535 (установка всех компонентов) или значение от 0 до 65535.</span><span class="sxs-lookup"><span data-stu-id="c3882-112">This parameter must be either 0 (install using authored feature levels), 65535 (install all features), or a value between 0 and 65535 to install a subset of available features.</span></span>

</dd> <dt>

<span data-ttu-id="c3882-113">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="c3882-113">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="c3882-114">Указывает состояние установки для компонента.</span><span class="sxs-lookup"><span data-stu-id="c3882-114">Specifies the installation state for the feature.</span></span> <span data-ttu-id="c3882-115">Этот параметр должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c3882-115">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="c3882-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c3882-116">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="c3882-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c3882-117">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="c3882-118"><dt>**мсиинсталлстатеадвертисед**</dt></span><span class="sxs-lookup"><span data-stu-id="c3882-118"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="c3882-119">Эта функция объявлена</span><span class="sxs-lookup"><span data-stu-id="c3882-119">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="c3882-120"><dt>**мсиинсталлстателокал**</dt></span><span class="sxs-lookup"><span data-stu-id="c3882-120"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="c3882-121">Этот компонент устанавливается локально.</span><span class="sxs-lookup"><span data-stu-id="c3882-121">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="c3882-122"><dt>**мсиинсталлстатеабсент**</dt></span><span class="sxs-lookup"><span data-stu-id="c3882-122"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="c3882-123">Компонент удален.</span><span class="sxs-lookup"><span data-stu-id="c3882-123">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="c3882-124"><dt>**мсиинсталлстатесаурце**</dt></span><span class="sxs-lookup"><span data-stu-id="c3882-124"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="c3882-125">Компонент устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="c3882-125">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="c3882-126"><dt>**мсиинсталлстатедефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="c3882-126"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="c3882-127">Компонент устанавливается в расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3882-127">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3882-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3882-128">Return value</span></span>

<span data-ttu-id="c3882-129">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c3882-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3882-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3882-130">Remarks</span></span>

<span data-ttu-id="c3882-131">Метод **конфигурепродукт** отображает пользовательский интерфейс, используя текущие параметры.</span><span class="sxs-lookup"><span data-stu-id="c3882-131">The **ConfigureProduct** method displays the user interface using current settings.</span></span> <span data-ttu-id="c3882-132">Параметры пользовательского интерфейса можно изменить, изменив [**свойство duilevel (объект установщика)**](installer-uilevel.md) перед вызовом метода **конфигурепродукт** .</span><span class="sxs-lookup"><span data-stu-id="c3882-132">User interface settings can be changed by modifying the [**UILevel property (Installer object)**](installer-uilevel.md) before calling the **ConfigureProduct** method.</span></span>

<span data-ttu-id="c3882-133">Если для параметра *InstallState* задано любое другое значение, отличное от мсиинсталлстатедефаулт, то параметр *инсталллевел* игнорируется и устанавливаются все компоненты продукта.</span><span class="sxs-lookup"><span data-stu-id="c3882-133">If the *InstallState* parameter is set to any other value than msiInstallStateDefault, the *InstallLevel* parameter is ignored and all features of the product are installed.</span></span> <span data-ttu-id="c3882-134">Используйте метод [**конфигурефеатуре**](installer-configurefeature.md) для управления установкой отдельных компонентов, если для параметра *InstallState* не задано значение мсиинсталлстатедефаулт.</span><span class="sxs-lookup"><span data-stu-id="c3882-134">Use the [**ConfigureFeature**](installer-configurefeature.md) method to control the installation of individual features when the *InstallState* parameter is not set to msiInstallStateDefault.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3882-135">Требования</span><span class="sxs-lookup"><span data-stu-id="c3882-135">Requirements</span></span>



| <span data-ttu-id="c3882-136">Требование</span><span class="sxs-lookup"><span data-stu-id="c3882-136">Requirement</span></span> | <span data-ttu-id="c3882-137">Значение</span><span class="sxs-lookup"><span data-stu-id="c3882-137">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3882-138">Версия</span><span class="sxs-lookup"><span data-stu-id="c3882-138">Version</span></span><br/> | <span data-ttu-id="c3882-139">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3882-139">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c3882-140">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3882-140">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c3882-141">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3882-141">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c3882-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c3882-142">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3882-143"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3882-143"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c3882-144">IID</span><span class="sxs-lookup"><span data-stu-id="c3882-144">IID</span></span><br/>     | <span data-ttu-id="c3882-145">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c3882-145">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="c3882-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3882-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3882-147">**мсиконфигурепродукт**</span><span class="sxs-lookup"><span data-stu-id="c3882-147">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[<span data-ttu-id="c3882-148">Функции установки и настройки</span><span class="sxs-lookup"><span data-stu-id="c3882-148">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




