---
description: Метод Провидекомпонент объекта Installer возвращает полный путь к компоненту и выполняет все необходимые установки.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Метод Installer. Провидекомпонент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651984"
---
# <a name="installerprovidecomponent-method"></a><span data-ttu-id="2839b-103">Метод Installer. Провидекомпонент</span><span class="sxs-lookup"><span data-stu-id="2839b-103">Installer.ProvideComponent method</span></span>

<span data-ttu-id="2839b-104">Метод **провидекомпонент** объекта [**Installer**](installer-object.md) возвращает полный путь к компоненту и выполняет все необходимые установки.</span><span class="sxs-lookup"><span data-stu-id="2839b-104">The **ProvideComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="2839b-105">При необходимости метод **провидекомпонент** объекта [**Installer**](installer-object.md) запрашивает источник и увеличивает счетчик использования для функции.</span><span class="sxs-lookup"><span data-stu-id="2839b-105">If necessary, the **ProvideComponent** method of the [**Installer**](installer-object.md) object prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="2839b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2839b-106">Syntax</span></span>


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="2839b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2839b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2839b-108">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="2839b-108">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="2839b-109">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="2839b-109">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="2839b-110">*Компонент*</span><span class="sxs-lookup"><span data-stu-id="2839b-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="2839b-111">Указывает идентификатор компонента, содержащего компонент.</span><span class="sxs-lookup"><span data-stu-id="2839b-111">Specifies the feature ID of the feature containing the component.</span></span>

</dd> <dt>

<span data-ttu-id="2839b-112">*Компонент*</span><span class="sxs-lookup"><span data-stu-id="2839b-112">*Component*</span></span> 
</dt> <dd>

<span data-ttu-id="2839b-113">Указывает код компонента.</span><span class="sxs-lookup"><span data-stu-id="2839b-113">Specifies the component code.</span></span>

</dd> <dt>

<span data-ttu-id="2839b-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="2839b-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="2839b-115">Определяет режим установки.</span><span class="sxs-lookup"><span data-stu-id="2839b-115">Defines the installation mode.</span></span> <span data-ttu-id="2839b-116">Этот параметр может принимать одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2839b-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="2839b-117">Имя</span><span class="sxs-lookup"><span data-stu-id="2839b-117">Name</span></span>                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="2839b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2839b-118">Meaning</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="2839b-119"><dt>**мсиинсталлмодедефаулт**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2839b-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                | <span data-ttu-id="2839b-120">Предоставляет путь к компоненту, при необходимости выполняя установку.</span><span class="sxs-lookup"><span data-stu-id="2839b-120">Provides the component path, performing any installation, if necessary.</span></span><br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="2839b-121"><dt>**мсиинсталлмодиксистинг**</dt> <dt>— 1</dt></span><span class="sxs-lookup"><span data-stu-id="2839b-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                           | <span data-ttu-id="2839b-122">Предоставляет путь к компоненту только в том случае, если компонент существует. в противном случае возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="2839b-122">Provides the component path only if the feature exists; otherwise, returns an empty string.</span></span> <span data-ttu-id="2839b-123">Этот режим проверяет существование файла ключа компонента.</span><span class="sxs-lookup"><span data-stu-id="2839b-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="2839b-124"><dt>**мсиинсталлмоденодетектион**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="2839b-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                               | <span data-ttu-id="2839b-125">Предоставляет путь к компоненту только в том случае, если компонент существует.</span><span class="sxs-lookup"><span data-stu-id="2839b-125">Provides the component path only if the feature exists.</span></span> <span data-ttu-id="2839b-126">В противном случае возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="2839b-126">Otherwise, returns an empty string.</span></span> <span data-ttu-id="2839b-127">Этот режим проверяет регистрацию компонента, но не проверяет существование файла ключа компонента.</span><span class="sxs-lookup"><span data-stu-id="2839b-127">This mode checks the component's registration but does not verify the existence of the component's key file.</span></span><br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="2839b-128"><dt>**мсиинсталлмоденосаурцересолутион**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="2839b-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                   | <span data-ttu-id="2839b-129">Предоставляет путь к компоненту только в том случае, если компонент существует с параметром InstallState параметра *мсиинсталлстателокал*.</span><span class="sxs-lookup"><span data-stu-id="2839b-129">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="2839b-130">При этом проверяется регистрация компонента, но не проверяется наличие файла ключа компонента.</span><span class="sxs-lookup"><span data-stu-id="2839b-130">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="2839b-131"><dt>**сочетание флагов мсиреинсталлмоде**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="2839b-131"><dt>**combination of the msiReinstallMode flags**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="2839b-132">Вызывает [**реинсталлфеатуре**](installer-reinstallfeature.md) для переустановки компонента с помощью этого параметра для параметра *ReinstallMode* , а затем предоставляет компонент.</span><span class="sxs-lookup"><span data-stu-id="2839b-132">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2839b-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2839b-133">Return value</span></span>

<span data-ttu-id="2839b-134">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2839b-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2839b-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2839b-135">Remarks</span></span>

<span data-ttu-id="2839b-136">Метод **провидекомпонент** сочетает в себе функциональные возможности [**усефеатуре**](installer-usefeature.md), [**конфигурефеатуре**](installer-configurefeature.md)и [**компонентпас**](installer-componentpath.md).</span><span class="sxs-lookup"><span data-stu-id="2839b-136">The **ProvideComponent** method combines the functionality of [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md), and [**ComponentPath**](installer-componentpath.md).</span></span> <span data-ttu-id="2839b-137">Метод **провидекомпонент** упрощает вызов последовательности, но также увеличивает счетчик использования и должен использоваться с осторожностью, чтобы предотвратить неточные показатели использования.</span><span class="sxs-lookup"><span data-stu-id="2839b-137">The **ProvideComponent** method simplifies the calling sequence, but it also increments the usage count and should be used with caution to prevent inaccurate usage counts.</span></span> <span data-ttu-id="2839b-138">Метод **провидекомпонент** также обеспечивает меньшую гибкость, чем ряд отдельных вызовов методов и свойств, упомянутых ранее.</span><span class="sxs-lookup"><span data-stu-id="2839b-138">The **ProvideComponent** method also provides less flexibility than a series of individual calls to the methods and properties previously mentioned.</span></span>

<span data-ttu-id="2839b-139">Если приложение восстанавливается после непредвиденной ситуации, приложение, вероятно, уже вызвало [**усефеатуре**](installer-usefeature.md) и увеличило счетчик использования.</span><span class="sxs-lookup"><span data-stu-id="2839b-139">If the application is recovering from an unexpected situation, the application has probably already called [**UseFeature**](installer-usefeature.md) and incremented the usage count.</span></span> <span data-ttu-id="2839b-140">В этом случае приложение должно избежать увеличения числа использований, вызвав метод [**конфигурефеатуре**](installer-configurefeature.md) вместо метода **провидекомпонент** .</span><span class="sxs-lookup"><span data-stu-id="2839b-140">In this case, the application should avoid incrementing the usage count by calling the [**ConfigureFeature**](installer-configurefeature.md) method instead of the **ProvideComponent** method.</span></span>

<span data-ttu-id="2839b-141">Параметр Мсиинсталлмодиксистинг нельзя использовать в сочетании с флагами Мсиреинсталлмоде.</span><span class="sxs-lookup"><span data-stu-id="2839b-141">The msiInstallModeExisting option cannot be used in combination with msiReinstallMode flags.</span></span>

## <a name="requirements"></a><span data-ttu-id="2839b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="2839b-142">Requirements</span></span>



| <span data-ttu-id="2839b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="2839b-143">Requirement</span></span> | <span data-ttu-id="2839b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="2839b-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2839b-145">Версия</span><span class="sxs-lookup"><span data-stu-id="2839b-145">Version</span></span><br/> | <span data-ttu-id="2839b-146">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2839b-146">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2839b-147">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2839b-147">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2839b-148">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="2839b-148">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2839b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2839b-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="2839b-150"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2839b-150"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2839b-151">IID</span><span class="sxs-lookup"><span data-stu-id="2839b-151">IID</span></span><br/>     | <span data-ttu-id="2839b-152">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2839b-152">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="2839b-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2839b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2839b-154">**мсипровидекомпонент**</span><span class="sxs-lookup"><span data-stu-id="2839b-154">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




