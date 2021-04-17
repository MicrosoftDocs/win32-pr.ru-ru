---
description: Метод Адвертисепродукт объекта Installer объявляет пакет установки.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Метод Installer:: Адвертисепродукт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651915"
---
# <a name="installeradvertiseproduct-method"></a><span data-ttu-id="8d7fe-103">Метод Installer:: Адвертисепродукт</span><span class="sxs-lookup"><span data-stu-id="8d7fe-103">Installer::AdvertiseProduct method</span></span>

<span data-ttu-id="8d7fe-104">Метод **адвертисепродукт** объекта [**Installer**](installer-object.md) объявляет пакет установки.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-104">The **AdvertiseProduct** method of the [**Installer**](installer-object.md) object advertises an installation package.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d7fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d7fe-105">Syntax</span></span>


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="8d7fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d7fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d7fe-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="8d7fe-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="8d7fe-108">Полный путь к пакету установщик Windows (MSI), который требуется объявить.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="8d7fe-109">*context*</span><span class="sxs-lookup"><span data-stu-id="8d7fe-109">*context*</span></span> 
</dt> <dd>

<span data-ttu-id="8d7fe-110">Контекст объявления.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-110">The context of the advertisement.</span></span> <span data-ttu-id="8d7fe-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8d7fe-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8d7fe-112">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="8d7fe-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8d7fe-113">Meaning</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <span data-ttu-id="8d7fe-114"><dt>**мсиадвертисепродуктмачине**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8d7fe-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="8d7fe-115">Объявляет приложение для [установки в контексте инсталляции](installation-context.md)для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-115">Advertises the application for an instalation in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="8d7fe-116">Это сделает пакет доступным для установки всеми пользователями компьютера.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-116">This makes the package available for installation by all users of the computer.</span></span><br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <span data-ttu-id="8d7fe-117"><dt>**мсиадвертисепродуктусер**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8d7fe-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="8d7fe-118">Объявляет приложение для установки в [контексте установки](installation-context.md)на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-118">Advertises the application for an installation in the per-user [installation context](installation-context.md).</span></span><br/>                                                                                   |



 

</dd> <dt>

<span data-ttu-id="8d7fe-119">*преобразования*</span><span class="sxs-lookup"><span data-stu-id="8d7fe-119">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="8d7fe-120">Список преобразований, применяемых к продукту.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-120">The list of transforms to apply to the product.</span></span> <span data-ttu-id="8d7fe-121">Преобразования в списке разделяются точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-121">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="8d7fe-122">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-122">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8d7fe-123">*language*</span><span class="sxs-lookup"><span data-stu-id="8d7fe-123">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="8d7fe-124">Язык используемого пакета установки.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-124">The language of the installation package to use.</span></span> <span data-ttu-id="8d7fe-125">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-125">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8d7fe-126">*options*</span><span class="sxs-lookup"><span data-stu-id="8d7fe-126">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="8d7fe-127">Параметры объявления.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-127">The advertisement options.</span></span> <span data-ttu-id="8d7fe-128">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-128">This parameter is optional.</span></span> <span data-ttu-id="8d7fe-129">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8d7fe-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8d7fe-130">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="8d7fe-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8d7fe-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="8d7fe-132"><dt>**мсиадвертиседефаулт**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8d7fe-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="8d7fe-133">Стандартное объявление</span><span class="sxs-lookup"><span data-stu-id="8d7fe-133">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="8d7fe-134"><dt>**мсиадвертисесинглеинстанце**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8d7fe-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="8d7fe-135">Объявляет новый экземпляр продукта.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-135">Advertises a new instance of the product.</span></span> <span data-ttu-id="8d7fe-136">Требует, чтобы первое преобразование в списке *преобразования параметра* преобразований было преобразованием экземпляра, которое изменяет код продукта.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-136">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="8d7fe-137">Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="8d7fe-137">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d7fe-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d7fe-138">Return value</span></span>

<span data-ttu-id="8d7fe-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d7fe-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d7fe-140">Remarks</span></span>

<span data-ttu-id="8d7fe-141">Метод **адвертисепродукт** использует функцию [**мсиадвертисепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="8d7fe-141">The **AdvertiseProduct** method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="8d7fe-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="8d7fe-142">Examples</span></span>

<span data-ttu-id="8d7fe-143">В следующем примере демонстрируется использование метода **адвертисепродукт** .</span><span class="sxs-lookup"><span data-stu-id="8d7fe-143">The following example demonstrates the use of the **AdvertiseProduct** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a><span data-ttu-id="8d7fe-144">Требования</span><span class="sxs-lookup"><span data-stu-id="8d7fe-144">Requirements</span></span>



| <span data-ttu-id="8d7fe-145">Требование</span><span class="sxs-lookup"><span data-stu-id="8d7fe-145">Requirement</span></span> | <span data-ttu-id="8d7fe-146">Значение</span><span class="sxs-lookup"><span data-stu-id="8d7fe-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7fe-147">Версия</span><span class="sxs-lookup"><span data-stu-id="8d7fe-147">Version</span></span><br/> | <span data-ttu-id="8d7fe-148">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8d7fe-149">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8d7fe-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8d7fe-150">Установщик Windows 4,5 в Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d7fe-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="8d7fe-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8d7fe-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="8d7fe-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d7fe-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="8d7fe-153">IID</span><span class="sxs-lookup"><span data-stu-id="8d7fe-153">IID</span></span><br/>     | <span data-ttu-id="8d7fe-154">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8d7fe-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="8d7fe-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d7fe-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d7fe-156">**Установщик**</span><span class="sxs-lookup"><span data-stu-id="8d7fe-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="8d7fe-157">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="8d7fe-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




