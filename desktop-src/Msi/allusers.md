---
Description: Свойство ALLUSERS настраивает контекст установки пакета.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: Свойство ALLUSERS
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669125"
---
# <a name="allusers-property"></a><span data-ttu-id="186fe-103">Свойство ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="186fe-103">ALLUSERS property</span></span>

<span data-ttu-id="186fe-104">Свойство **ALLUSERS** настраивает контекст установки пакета.</span><span class="sxs-lookup"><span data-stu-id="186fe-104">The **ALLUSERS** property configures the installation context of the package.</span></span> <span data-ttu-id="186fe-105">Установщик Windows выполняет установку на уровне пользователя или на компьютере в зависимости от привилегий доступа пользователя, требуются ли повышенные привилегии для установки приложения, значение свойства **ALLUSERS** , значение свойства [**мсиинсталлперусер**](msiinstallperuser.md) и версия операционной системы.</span><span class="sxs-lookup"><span data-stu-id="186fe-105">The Windows Installer performs a per-user installation or per-machine installation depending on the access privileges of the user, whether elevated privileges are required to install the application, the value of the **ALLUSERS** property, the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property and the version of the operating system.</span></span>

<span data-ttu-id="186fe-106">Значение свойства **ALLUSERS** во время установки определяет [контекст установки](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="186fe-106">The value of the **ALLUSERS** property, at installation time, determines the [installation context](installation-context.md).</span></span>

-   <span data-ttu-id="186fe-107">Свойство **ALLUSERS** , равное 1, указывает контекст установки для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="186fe-107">An **ALLUSERS** property value of 1 specifies the per-machine installation context.</span></span>
-   <span data-ttu-id="186fe-108">Значение свойства **ALLUSERS** пустой строки ("") указывает контекст установки для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="186fe-108">An **ALLUSERS** property value of an empty string ("") specifies the per-user installation context.</span></span>
-   <span data-ttu-id="186fe-109">Если свойству **ALLUSERS** присвоено значение 2, установщик Windows всегда сбрасывает значение свойства **ALLUSERS** равным 1 и выполняет установку на компьютере или сбрасывает значение свойства **ALLUSERS** в пустую строку ("") и выполняет установку на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="186fe-109">If the value of the **ALLUSERS** property is set to 2, the Windows Installer always resets the value of the **ALLUSERS** property to 1 and performs a per-machine installation or it resets the value of the **ALLUSERS** property to an empty string ("") and performs a per-user installation.</span></span> <span data-ttu-id="186fe-110">Значение ALLUSERS = 2 позволяет системе сбрасывать значение **ALLUSERS** и контекст установки, зависящие от привилегий пользователя и версии Windows.</span><span class="sxs-lookup"><span data-stu-id="186fe-110">The value ALLUSERS=2 enables the system to reset the value of **ALLUSERS**, and the installation context, dependent upon the user's privileges and the version of Windows.</span></span>

    <span data-ttu-id="186fe-111">**Windows 7:** Задайте для свойства **ALLUSERS** значение 2, чтобы использовать свойство [**мсиинсталлперусер**](msiinstallperuser.md) для указания контекста установки.</span><span class="sxs-lookup"><span data-stu-id="186fe-111">**Windows 7:** Set the **ALLUSERS** property to 2 to use the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property to specify the installation context.</span></span> <span data-ttu-id="186fe-112">Для установки на компьютер задайте для свойства **мсиинсталлперусер** пустую строку ("").</span><span class="sxs-lookup"><span data-stu-id="186fe-112">Set the **MSIINSTALLPERUSER** property to an empty string ("") for a per-machine installation.</span></span> <span data-ttu-id="186fe-113">Присвойте свойству **мсиинсталлперусер** значение 1 для установки на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="186fe-113">Set the **MSIINSTALLPERUSER** property to 1 for a per-user installation.</span></span> <span data-ttu-id="186fe-114">Если пакет был написан согласно рекомендациям по разработке, описанным в разделе [Создание отдельного пакета](single-package-authoring.md), пользователи, имеющие доступ пользователей, могут установить в контекст для каждого пользователя без необходимости предоставлять учетные данные UAC.</span><span class="sxs-lookup"><span data-stu-id="186fe-114">If the package has been written following the development guidelines described in [Single Package Authoring](single-package-authoring.md), users having user access can install into the per-user context without having to provide UAC credentials.</span></span> <span data-ttu-id="186fe-115">Если у пользователя есть права доступа пользователя, установщик выполняет установку на компьютере только в том случае, если в диалоговое окно UAC передаются учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="186fe-115">If the user has user access privileges, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span>

    <span data-ttu-id="186fe-116">**Windows Vista:** Задайте для свойства **ALLUSERS** значение 2 и установщик Windows соответствует [*контролю учетных записей*](u-gly.md) (UAC).</span><span class="sxs-lookup"><span data-stu-id="186fe-116">**Windows Vista:** Set the **ALLUSERS** property to 2 and Windows Installer complies with [*User Account Control*](u-gly.md) (UAC).</span></span> <span data-ttu-id="186fe-117">Если у пользователя есть права доступа пользователя и ALLUSERS = 2, установщик выполняет установку на компьютере только в том случае, если в диалоговое окно UAC передаются учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="186fe-117">If the user has user access privileges, and ALLUSERS=2, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span> <span data-ttu-id="186fe-118">Если включен контроль учетных записей и не предоставлены правильные учетные данные администратора, установка завершается с ошибкой, сообщающей, что требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="186fe-118">If UAC is enabled and the correct Admin credentials are not provided, the installation fails with an error stating that administrator privileges are required.</span></span> <span data-ttu-id="186fe-119">Если контроль учетных записей отключен с помощью раздела реестра, групповой политики или панели управления, диалоговое окно UAC не отображается, и установка завершается с ошибкой, сообщающей о необходимости прав администратора.</span><span class="sxs-lookup"><span data-stu-id="186fe-119">If UAC is disabled by the registry key, group policy, or the control panel, the UAC dialog box is not displayed and the installation fails with an error stating that administrator privileges are required.</span></span>

    <span data-ttu-id="186fe-120">**Windows XP:** Присвойте свойству **ALLUSERS** значение 2, а установщик Windows выполняет установку на уровне пользователя, если у пользователя есть права доступа пользователя.</span><span class="sxs-lookup"><span data-stu-id="186fe-120">**Windows XP:** Set the **ALLUSERS** property to 2 and Windows Installer performs a per-user installation if the user has user access privileges.</span></span>

-   <span data-ttu-id="186fe-121">Если значение свойства **ALLUSERS** не равно 2, установщик Windows игнорирует значение свойства [**мсиинсталлперусер**](msiinstallperuser.md) .</span><span class="sxs-lookup"><span data-stu-id="186fe-121">If the value of the **ALLUSERS** property does not equal 2, the Windows Installer ignores the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property.</span></span>

## <a name="example"></a><span data-ttu-id="186fe-122">Пример</span><span class="sxs-lookup"><span data-stu-id="186fe-122">Example</span></span>

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

<span data-ttu-id="186fe-123">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="186fe-123">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) on GitHub.</span></span>

## <a name="default-value"></a><span data-ttu-id="186fe-124">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="186fe-124">Default Value</span></span>

<span data-ttu-id="186fe-125">Рекомендуемый контекст установки по умолчанию — "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="186fe-125">The recommended default installation context is per-user.</span></span> <span data-ttu-id="186fe-126">Если параметр **ALLUSERS** не задан, установщик выполняет установку для отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="186fe-126">If **ALLUSERS** is not set, the installer does a per-user installation.</span></span> <span data-ttu-id="186fe-127">Чтобы убедиться, что свойство **ALLUSERS** не задано, присвоив ему значение пустой строки (""), ALLUSERS = "".</span><span class="sxs-lookup"><span data-stu-id="186fe-127">You can ensure the **ALLUSERS** property has not been set by setting its value to an empty string (""), ALLUSERS="".</span></span>

## <a name="remarks"></a><span data-ttu-id="186fe-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="186fe-128">Remarks</span></span>

<span data-ttu-id="186fe-129">[Контекст установки](installation-context.md) определяет значения свойств [**DesktopFolder**](desktopfolder.md), [**программенуфолдер**](programmenufolder.md), [**programmenufolder**](startmenufolder.md), [**стартупфолдер**](startupfolder.md), [**темплатефолдер**](templatefolder.md), [**админтулсфолдер**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**коммонфилесфолдер**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)и [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="186fe-129">The [installation context](installation-context.md) determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="186fe-130">Контекст установки определяет части реестра, в которых записи в [таблице реестра](registry-table.md) и [таблице ремоверегистри](removeregistry-table.md)с параметром-1 в корневом столбце, записываются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="186fe-130">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="186fe-131">Требования</span><span class="sxs-lookup"><span data-stu-id="186fe-131">Requirements</span></span>



| <span data-ttu-id="186fe-132">Требование</span><span class="sxs-lookup"><span data-stu-id="186fe-132">Requirement</span></span> | <span data-ttu-id="186fe-133">Значение</span><span class="sxs-lookup"><span data-stu-id="186fe-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186fe-134">Версия</span><span class="sxs-lookup"><span data-stu-id="186fe-134">Version</span></span><br/> | <span data-ttu-id="186fe-135">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="186fe-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="186fe-136">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="186fe-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="186fe-137">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="186fe-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="186fe-138">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="186fe-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="186fe-139">См. также</span><span class="sxs-lookup"><span data-stu-id="186fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186fe-140">Свойства</span><span class="sxs-lookup"><span data-stu-id="186fe-140">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="186fe-141">**мсиинсталлперусер**</span><span class="sxs-lookup"><span data-stu-id="186fe-141">**MSIINSTALLPERUSER**</span></span>](msiinstallperuser.md)
</dt> <dt>

[<span data-ttu-id="186fe-142">Контекст установки</span><span class="sxs-lookup"><span data-stu-id="186fe-142">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="186fe-143">Создание отдельных пакетов</span><span class="sxs-lookup"><span data-stu-id="186fe-143">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




