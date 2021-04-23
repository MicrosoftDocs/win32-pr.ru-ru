---
description: Метод Провидеассембли объекта Installer возвращает установленный путь к сборке.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Установщик::P метод Ровидеассембли
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652167"
---
# <a name="installerprovideassembly-method"></a><span data-ttu-id="b0caf-103">Установщик::P метод Ровидеассембли</span><span class="sxs-lookup"><span data-stu-id="b0caf-103">Installer::ProvideAssembly method</span></span>

<span data-ttu-id="b0caf-104">Метод **провидеассембли** объекта [**Installer**](installer-object.md) возвращает установленный путь к сборке.</span><span class="sxs-lookup"><span data-stu-id="b0caf-104">The **ProvideAssembly** method of the [**Installer**](installer-object.md) object returns the installed path of an assembly.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0caf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0caf-105">Syntax</span></span>


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a><span data-ttu-id="b0caf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0caf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0caf-107">*сборок*</span><span class="sxs-lookup"><span data-stu-id="b0caf-107">*assembly*</span></span> 
</dt> <dd>

<span data-ttu-id="b0caf-108">Строгое имя установленной сборки, к которой выполняется запрос.</span><span class="sxs-lookup"><span data-stu-id="b0caf-108">The strong name of installed assembly that is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="b0caf-109">*appContext*</span><span class="sxs-lookup"><span data-stu-id="b0caf-109">*appContext*</span></span> 
</dt> <dd>

<span data-ttu-id="b0caf-110">Задайте для глобальных сборок значение null.</span><span class="sxs-lookup"><span data-stu-id="b0caf-110">Set to null for global assemblies.</span></span> <span data-ttu-id="b0caf-111">Для закрытых сборок задайте для *appContext* полный путь к файлу конфигурации приложения или полный путь к исполняемому файлу приложения, для которого сборка была закрыта.</span><span class="sxs-lookup"><span data-stu-id="b0caf-111">For private assemblies, set *appContext* to the full path of the application configuration file or to the full path of the executable file of the application to which the assembly has been made private.</span></span>

</dd> <dt>

<span data-ttu-id="b0caf-112">*installMode*</span><span class="sxs-lookup"><span data-stu-id="b0caf-112">*installMode*</span></span> 
</dt> <dd>

<span data-ttu-id="b0caf-113">Определяет режим установки.</span><span class="sxs-lookup"><span data-stu-id="b0caf-113">Defines the installation mode.</span></span> <span data-ttu-id="b0caf-114">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="b0caf-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b0caf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b0caf-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="b0caf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b0caf-116">Meaning</span></span>                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="b0caf-117"><dt>**мсиинсталлмодедефаулт**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0caf-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                                | <span data-ttu-id="b0caf-118">Укажите компонент и выполните установку, необходимую для предоставления компонента.</span><span class="sxs-lookup"><span data-stu-id="b0caf-118">Provide the component and perform any installation necessary to provide the component.</span></span> <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="b0caf-119"><dt>**мсиинсталлмодиксистинг**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="b0caf-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span></span> </dl>                                                                                           | <span data-ttu-id="b0caf-120">Предоставьте компонент только в том случае, если компонент существует.</span><span class="sxs-lookup"><span data-stu-id="b0caf-120">Provide the component only if the feature exists.</span></span> <span data-ttu-id="b0caf-121">Этот параметр позволяет проверить существование сборки.</span><span class="sxs-lookup"><span data-stu-id="b0caf-121">This option will verify that the assembly exists.</span></span><br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="b0caf-122"><dt>**мсиинсталлмоденодетектион**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="b0caf-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span></span> </dl>                                                                               | <span data-ttu-id="b0caf-123">Предоставьте компонент только в том случае, если компонент существует.</span><span class="sxs-lookup"><span data-stu-id="b0caf-123">Provide the component only if the feature exists.</span></span> <span data-ttu-id="b0caf-124">Этот параметр не проверяет существование сборки.</span><span class="sxs-lookup"><span data-stu-id="b0caf-124">This option does not verify that the assembly exists.</span></span><br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="b0caf-125"><dt>**мсиинсталлмоденосаурцересолутион**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="b0caf-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span></span> </dl>                                                   | <span data-ttu-id="b0caf-126">Предоставляет сборку только в том случае, если сборка установлена локально.</span><span class="sxs-lookup"><span data-stu-id="b0caf-126">Provides the assembly only if the assembly is installed local.</span></span><br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <span data-ttu-id="b0caf-127"><dt>**Сочетание флагов, используемых [ **реинсталлфеатуре**](installer-reinstallfeature.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b0caf-127"><dt>**Combination of the flags used by [**ReinstallFeature**](installer-reinstallfeature.md)**</dt></span></span> </dl> | <span data-ttu-id="b0caf-128">Вызывает метод [**реинсталлфеатуре**](installer-reinstallfeature.md) для переустановки компонента с помощью этого параметра для *ReinstallMode*, а затем возвращает путь к сборке.</span><span class="sxs-lookup"><span data-stu-id="b0caf-128">Calls the [**ReinstallFeature**](installer-reinstallfeature.md) method to reinstall the feature using this parameter for *ReinstallMode*, and then returns the assembly path.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b0caf-129">*Файле*</span><span class="sxs-lookup"><span data-stu-id="b0caf-129">*assemblyInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b0caf-130">Сведения о сборке и тип сборки.</span><span class="sxs-lookup"><span data-stu-id="b0caf-130">Assembly information and assembly type.</span></span> <span data-ttu-id="b0caf-131">Задайте одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b0caf-131">Set to one of the following values.</span></span>



| <span data-ttu-id="b0caf-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b0caf-132">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="b0caf-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b0caf-133">Meaning</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <span data-ttu-id="b0caf-134"><dt>**мсипровидеассемблинет**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0caf-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="b0caf-135">Сборка .NET.</span><span class="sxs-lookup"><span data-stu-id="b0caf-135">A .NET assembly.</span></span><br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <span data-ttu-id="b0caf-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b0caf-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="b0caf-137">Параллельная сборка Win32.</span><span class="sxs-lookup"><span data-stu-id="b0caf-137">A Win32 side-by-side assembly.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0caf-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0caf-138">Return value</span></span>

<span data-ttu-id="b0caf-139">Путь к установленной сборке.</span><span class="sxs-lookup"><span data-stu-id="b0caf-139">The path to the installed assembly.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0caf-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0caf-140">Remarks</span></span>

<span data-ttu-id="b0caf-141">Метод **провидеассембли** использует функцию [**мсипровидеассембли**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) .</span><span class="sxs-lookup"><span data-stu-id="b0caf-141">The **ProvideAssembly** method uses the [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) function.</span></span>

## <a name="examples"></a><span data-ttu-id="b0caf-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="b0caf-142">Examples</span></span>

<span data-ttu-id="b0caf-143">В следующем примере сценария демонстрируется использование метода Провидеассембли.</span><span class="sxs-lookup"><span data-stu-id="b0caf-143">The following sample script demonstrates the use of the ProvideAssembly method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a><span data-ttu-id="b0caf-144">Требования</span><span class="sxs-lookup"><span data-stu-id="b0caf-144">Requirements</span></span>



| <span data-ttu-id="b0caf-145">Требование</span><span class="sxs-lookup"><span data-stu-id="b0caf-145">Requirement</span></span> | <span data-ttu-id="b0caf-146">Значение</span><span class="sxs-lookup"><span data-stu-id="b0caf-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0caf-147">Версия</span><span class="sxs-lookup"><span data-stu-id="b0caf-147">Version</span></span><br/> | <span data-ttu-id="b0caf-148">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b0caf-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b0caf-149">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b0caf-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b0caf-150">Установщик Windows 4,5 в Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b0caf-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="b0caf-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b0caf-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="b0caf-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0caf-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="b0caf-153">IID</span><span class="sxs-lookup"><span data-stu-id="b0caf-153">IID</span></span><br/>     | <span data-ttu-id="b0caf-154">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b0caf-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="b0caf-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0caf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0caf-156">**Установщик**</span><span class="sxs-lookup"><span data-stu-id="b0caf-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="b0caf-157">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="b0caf-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




