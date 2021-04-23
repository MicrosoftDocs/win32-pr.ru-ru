---
description: Microsoft установщик Windows принимает URL-адрес в качестве допустимого источника для исправления.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Загрузка и установка исправления из Интернета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154822"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a><span data-ttu-id="2e726-103">Загрузка и установка исправления из Интернета</span><span class="sxs-lookup"><span data-stu-id="2e726-103">Downloading and Installing a Patch From the Internet</span></span>

<span data-ttu-id="2e726-104">Microsoft установщик Windows принимает URL-адрес в качестве допустимого источника для [исправления](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="2e726-104">Microsoft Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for a [patch](patch-packages.md).</span></span> <span data-ttu-id="2e726-105">Чтобы установить исправление, расположенное на веб-сервере https://MyWeb/MyPatch.msp , используйте следующую командную строку:</span><span class="sxs-lookup"><span data-stu-id="2e726-105">To install a patch located on a web server at https://MyWeb/MyPatch.msp, use the following command line:</span></span>

<span data-ttu-id="2e726-106">**msiexec/p https://MyWeb/MyPatch.msp**</span><span class="sxs-lookup"><span data-stu-id="2e726-106">**msiexec /p https://MyWeb/MyPatch.msp**</span></span>

<span data-ttu-id="2e726-107">Чтобы избежать непредвиденных результатов, не запускайте исправление, щелкнув ссылку на веб-странице, на которой отображается URL-адрес файла исправления.</span><span class="sxs-lookup"><span data-stu-id="2e726-107">To avoid unexpected results, do not launch a patch by clicking the link on the webpage showing the patch file's URL.</span></span> <span data-ttu-id="2e726-108">Также можно установить исправление с помощью сценария, как в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="2e726-108">You can also install a patch by using a script like the following:</span></span>


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="2e726-109">Обратите внимание, что поскольку объект [**установщика**](installer-object.md) не помечен как [сафефорскриптинг](safeforscripting.md) на компьютере пользователя, пользователям необходимо изменить параметры безопасности браузера, чтобы пример работал правильно.</span><span class="sxs-lookup"><span data-stu-id="2e726-109">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="2e726-110">Дополнительные сведения см. в разделе [рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md) и [цифровых подписей и установщик Windows](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="2e726-110">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e726-111">См. также</span><span class="sxs-lookup"><span data-stu-id="2e726-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e726-112">Пакеты исправлений</span><span class="sxs-lookup"><span data-stu-id="2e726-112">Patch Packages</span></span>](patch-packages.md)
</dt> <dt>

[<span data-ttu-id="2e726-113">Создание пакета исправлений</span><span class="sxs-lookup"><span data-stu-id="2e726-113">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="2e726-114">Исправление настроенных приложений</span><span class="sxs-lookup"><span data-stu-id="2e726-114">Patching Customized Applications</span></span>](patching-customized-applications.md)
</dt> <dt>

[<span data-ttu-id="2e726-115">Загрузка установки из Интернета</span><span class="sxs-lookup"><span data-stu-id="2e726-115">Downloading an Installation From the Internet</span></span>](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



