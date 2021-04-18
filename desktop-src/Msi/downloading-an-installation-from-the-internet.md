---
description: Установщик Windows принимает универсальный указатель ресурсов (URL) в качестве допустимого источника для установки.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Загрузка установки из Интернета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650648"
---
# <a name="downloading-an-installation-from-the-internet"></a><span data-ttu-id="b0ca0-103">Загрузка установки из Интернета</span><span class="sxs-lookup"><span data-stu-id="b0ca0-103">Downloading an Installation from the Internet</span></span>

<span data-ttu-id="b0ca0-104">Установщик Windows принимает универсальный указатель ресурсов (URL) в качестве допустимого источника для установки.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-104">Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for an installation.</span></span> <span data-ttu-id="b0ca0-105">Установщик Windows может устанавливать пакеты, исправления и преобразования из расположения URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-105">Windows Installer can install packages, patches, and transforms from a URL location.</span></span>

<span data-ttu-id="b0ca0-106">Если база данных установки находится по URL-адресу, установщик загружает базу данных в расположение кэша перед началом установки.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-106">If the installation database is at a URL, the installer downloads the database to a cache location before starting the installation.</span></span> <span data-ttu-id="b0ca0-107">Установщик также скачивает файлы и CAB-файлы из источника Интернета, которые подходят для выбора пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-107">The installer also downloads the files and cabinet files from the Internet source that are appropriate for the user's selections.</span></span> <span data-ttu-id="b0ca0-108">Дополнительные сведения см. [в разделе Пример установки установщик Windows на основе URL-адресов](a-url-based-windows-installer-installation-example.md) .</span><span class="sxs-lookup"><span data-stu-id="b0ca0-108">See [A URL-based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md) for more information.</span></span>

<span data-ttu-id="b0ca0-109">Например, чтобы установить пакет с источником, расположенным на веб-сервере https://server/share/package.msi , можно использовать параметры [командной строки](command-line-options.md) для установки пакета и задания [общих](public-properties.md) свойств.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-109">For example, to install a package with a source located on a web server at https://server/share/package.msi, you can use the [command line](command-line-options.md) options to install the package and set [public](public-properties.md) properties.</span></span>

<span data-ttu-id="b0ca0-110">msiexec/i https://server/share/package.msi *свойство = значение*</span><span class="sxs-lookup"><span data-stu-id="b0ca0-110">msiexec /i https://server/share/package.msi *PROPERTY=VALUE*</span></span>

<span data-ttu-id="b0ca0-111">Для запуска установки из веб-браузера необходимо передать в установщик командную строку, аналогичную показанной ранее.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-111">A command line like the one previously shown should be passed to the installer to start an installation from a web browser.</span></span> <span data-ttu-id="b0ca0-112">В общем случае не следует загружать и устанавливать пакет, просто дважды щелкнув MSI-файл в браузере.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-112">In general, you should not download and install the package simply by double-clicking the .msi file from within the browser.</span></span> <span data-ttu-id="b0ca0-113">При этом MSI файл загружается в папку Temporary Internet Files и в установщик передается следующая команда:</span><span class="sxs-lookup"><span data-stu-id="b0ca0-113">This downloads the .msi file to the temporary Internet files folder and passes the following command to the installer:</span></span>

<span data-ttu-id="b0ca0-114">**msiexec/i c: \\ \\ временные файлы интернета Windows \\package.msi**</span><span class="sxs-lookup"><span data-stu-id="b0ca0-114">**msiexec /i c:\\windows\\temporary internet files\\package.msi**</span></span>

<span data-ttu-id="b0ca0-115">Установка завершается сбоем, если пакету требуются внешние исходные файлы или ящики, так как они находятся не в том же расположении, что и MSI-файл.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-115">The installation fails if the package requires any external source files or cabinets because these are not located in the same location as the .msi file.</span></span>

<span data-ttu-id="b0ca0-116">Обратите внимание, что поскольку объект [**установщика**](installer-object.md) не помечен как [сафефорскриптинг](safeforscripting.md) на компьютере пользователя, пользователям необходимо изменить параметры безопасности браузера, чтобы пример работал правильно.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-116">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="b0ca0-117">Метод [**инсталлпродукт**](installer-installproduct.md) можно использовать для запуска предыдущей команды из браузера в качестве события щелчка.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-117">The [**InstallProduct**](installer-installproduct.md) method could be used to run the previous command from a browser as an on-click event.</span></span>


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="b0ca0-118">Обратите внимание, что поскольку некоторые веб-серверы чувствительны к регистру, поле FileName в таблице [File](file-table.md) должно точно соответствовать регистру исходных файлов, чтобы обеспечить поддержку загрузки из Интернета.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-118">Note that because some web servers are case sensitive, the FileName field in the [File](file-table.md) table must match the case of the source files exactly to ensure support of Internet downloads.</span></span>

<span data-ttu-id="b0ca0-119">См. раздел [Загрузка и установка исправления из Интернета](downloading-and-installing-a-patch-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="b0ca0-119">See [Downloading and Installing a Patch from the Internet](downloading-and-installing-a-patch-from-the-internet.md).</span></span> <span data-ttu-id="b0ca0-120">Дополнительные сведения о защите установки и использовании цифровых сертификатов см. в разделе [рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md) и [цифровых подписей и установщик Windows](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="b0ca0-120">For more information about securing installations and using digital certificates, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span> <span data-ttu-id="b0ca0-121">Дополнительные сведения о создании веб-установки пакета установщик Windows см. в разделе [начальная загрузка Интернета](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="b0ca0-121">For more information about how to create a web installation of a Windows Installer package, see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

## <a name="available-internet-protocols"></a><span data-ttu-id="b0ca0-122">Доступные протоколы Интернета</span><span class="sxs-lookup"><span data-stu-id="b0ca0-122">Available Internet Protocols</span></span>

<span data-ttu-id="b0ca0-123">Начиная с Windows Server 2003 и Windows XP, установщик может использовать протоколы HTTP, HTTPS и FILE.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-123">Beginning with Windows Server 2003 and Windows XP, the installer can use the HTTP, HTTPS and FILE protocols.</span></span> <span data-ttu-id="b0ca0-124">Установщик не поддерживает протоколы FTP и GOPHER.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-124">The installer does not support the FTP and GOPHER protocols.</span></span>

<span data-ttu-id="b0ca0-125">Установщик Windows версии 2,0 может использовать протоколы HTTP, FILE и FTP и не может использовать протоколы HTTPS и GOPHER.</span><span class="sxs-lookup"><span data-stu-id="b0ca0-125">Windows Installer version 2.0 can use the HTTP, FILE, and FTP protocols and cannot use the HTTPS and GOPHER protocols.</span></span>

 

 



