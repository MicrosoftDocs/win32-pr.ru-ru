---
description: Метод Креатеадвертисескрипт объекта Installer создает скрипт объявления.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Метод Installer:: Креатеадвертисескрипт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652288"
---
# <a name="installercreateadvertisescript-method"></a><span data-ttu-id="57543-103">Метод Installer:: Креатеадвертисескрипт</span><span class="sxs-lookup"><span data-stu-id="57543-103">Installer::CreateAdvertiseScript method</span></span>

<span data-ttu-id="57543-104">Метод **креатеадвертисескрипт** объекта [**Installer**](installer-object.md) создает скрипт объявления.</span><span class="sxs-lookup"><span data-stu-id="57543-104">The **CreateAdvertiseScript** method of the [**Installer**](installer-object.md) object generates an advertise script.</span></span>

## <a name="syntax"></a><span data-ttu-id="57543-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57543-105">Syntax</span></span>


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="57543-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57543-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57543-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="57543-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="57543-108">Полный путь к пакету установщик Windows (MSI), который требуется объявить.</span><span class="sxs-lookup"><span data-stu-id="57543-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="57543-109">*скриптфилепас*</span><span class="sxs-lookup"><span data-stu-id="57543-109">*scriptFilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="57543-110">Полный путь к файлу скрипта, который создается с объявленной информацией.</span><span class="sxs-lookup"><span data-stu-id="57543-110">The full path to the script file to be created with the advertised information.</span></span>

</dd> <dt>

<span data-ttu-id="57543-111">*преобразования*</span><span class="sxs-lookup"><span data-stu-id="57543-111">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="57543-112">Список преобразований, применяемых к продукту.</span><span class="sxs-lookup"><span data-stu-id="57543-112">The list of transforms to apply to the product.</span></span> <span data-ttu-id="57543-113">Преобразования в списке разделяются точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="57543-113">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="57543-114">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="57543-114">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="57543-115">*language*</span><span class="sxs-lookup"><span data-stu-id="57543-115">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="57543-116">Язык используемого пакета установки.</span><span class="sxs-lookup"><span data-stu-id="57543-116">The language of the installation package to use.</span></span> <span data-ttu-id="57543-117">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="57543-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="57543-118">*platform*</span><span class="sxs-lookup"><span data-stu-id="57543-118">*platform*</span></span> 
</dt> <dd>

<span data-ttu-id="57543-119">Этот параметр указывает, для какой платформы установщик должен создать скрипт.</span><span class="sxs-lookup"><span data-stu-id="57543-119">This parameter specifies for which platform the installer should create the script.</span></span> <span data-ttu-id="57543-120">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="57543-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="57543-121">Значение</span><span class="sxs-lookup"><span data-stu-id="57543-121">Value</span></span>                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="57543-122">Значение</span><span class="sxs-lookup"><span data-stu-id="57543-122">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <span data-ttu-id="57543-123"><dt>**мсиадвертисекуррентплатформ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="57543-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="57543-124">Создает скрипт для текущей платформы.</span><span class="sxs-lookup"><span data-stu-id="57543-124">Creates a script for the current platform.</span></span><br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <span data-ttu-id="57543-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="57543-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="57543-126">Создает скрипт для платформы x86.</span><span class="sxs-lookup"><span data-stu-id="57543-126">Creates a script for the x86 platform.</span></span><br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <span data-ttu-id="57543-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="57543-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="57543-128">Создает скрипт для систем на базе процессоров Itanium.</span><span class="sxs-lookup"><span data-stu-id="57543-128">Creates a script for Itanium-based systems.</span></span><br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <span data-ttu-id="57543-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="57543-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="57543-130">Создает скрипт для платформы x64.</span><span class="sxs-lookup"><span data-stu-id="57543-130">Creates a script for the x64 platform.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="57543-131">*options*</span><span class="sxs-lookup"><span data-stu-id="57543-131">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="57543-132">Параметры объявления.</span><span class="sxs-lookup"><span data-stu-id="57543-132">Advertisement options.</span></span> <span data-ttu-id="57543-133">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="57543-133">This parameter is optional.</span></span> <span data-ttu-id="57543-134">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="57543-134">This parameter can be one of the following values.</span></span> <span data-ttu-id="57543-135">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="57543-135">This parameter is optional.</span></span>



| <span data-ttu-id="57543-136">Значение</span><span class="sxs-lookup"><span data-stu-id="57543-136">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="57543-137">Значение</span><span class="sxs-lookup"><span data-stu-id="57543-137">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="57543-138"><dt>**мсиадвертиседефаулт**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="57543-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="57543-139">Стандартное объявление</span><span class="sxs-lookup"><span data-stu-id="57543-139">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="57543-140"><dt>**мсиадвертисесинглеинстанце**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="57543-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="57543-141">Объявляет новый экземпляр продукта.</span><span class="sxs-lookup"><span data-stu-id="57543-141">Advertises a new instance of the product.</span></span> <span data-ttu-id="57543-142">Требует, чтобы первое преобразование в списке *преобразования параметра* преобразований было преобразованием экземпляра, которое изменяет код продукта.</span><span class="sxs-lookup"><span data-stu-id="57543-142">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="57543-143">Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="57543-143">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57543-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57543-144">Return value</span></span>

<span data-ttu-id="57543-145">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="57543-145">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57543-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57543-146">Remarks</span></span>

<span data-ttu-id="57543-147">Метод [**адвертисепродукт**](installer-advertiseproduct.md) использует функцию [**мсиадвертисепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="57543-147">The [**AdvertiseProduct**](installer-advertiseproduct.md) method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="57543-148">Примеры</span><span class="sxs-lookup"><span data-stu-id="57543-148">Examples</span></span>

<span data-ttu-id="57543-149">В следующем примере демонстрируется использование метода **креатеадвертисескрипт** .</span><span class="sxs-lookup"><span data-stu-id="57543-149">The following example demonstrates the use of the **CreateAdvertiseScript** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a><span data-ttu-id="57543-150">Требования</span><span class="sxs-lookup"><span data-stu-id="57543-150">Requirements</span></span>



| <span data-ttu-id="57543-151">Требование</span><span class="sxs-lookup"><span data-stu-id="57543-151">Requirement</span></span> | <span data-ttu-id="57543-152">Значение</span><span class="sxs-lookup"><span data-stu-id="57543-152">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57543-153">Версия</span><span class="sxs-lookup"><span data-stu-id="57543-153">Version</span></span><br/> | <span data-ttu-id="57543-154">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="57543-154">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="57543-155">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="57543-155">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="57543-156">Установщик Windows 4,5 в Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="57543-156">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="57543-157">DLL</span><span class="sxs-lookup"><span data-stu-id="57543-157">DLL</span></span><br/>     | <dl> <span data-ttu-id="57543-158"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57543-158"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="57543-159">IID</span><span class="sxs-lookup"><span data-stu-id="57543-159">IID</span></span><br/>     | <span data-ttu-id="57543-160">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="57543-160">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="57543-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57543-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57543-162">**Установщик**</span><span class="sxs-lookup"><span data-stu-id="57543-162">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="57543-163">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="57543-163">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




