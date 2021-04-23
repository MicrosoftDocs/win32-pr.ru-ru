---
description: Настраиваемый исполняемый файл начальной загрузки (Setup.exe) и средство настройки (Msistuff.exe) входят в состав Windows SDK компонентов для установщик Windows разработчиков.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Настройка ресурсов Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105651537"
---
# <a name="configuring-the-setupexe-resources"></a><span data-ttu-id="5b25d-103">Настройка ресурсов Setup.exe</span><span class="sxs-lookup"><span data-stu-id="5b25d-103">Configuring the Setup.exe Resources</span></span>

<span data-ttu-id="5b25d-104">Настраиваемый исполняемый файл начальной загрузки (Setup.exe) и средство настройки ( [Msistuff.exe](msistuff-exe.md)) входят в состав [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="5b25d-104">A configurable bootstrap executable (Setup.exe) and configuration tool ( [Msistuff.exe](msistuff-exe.md)) is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="5b25d-105">Используя Msistuff.exe для настройки ресурсов в Setup.exe, разработчики могут легко создать веб-установку пакета установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="5b25d-105">By using Msistuff.exe to configure the resources in Setup.exe, developers can easily create a web installation of a Windows Installer package.</span></span> <span data-ttu-id="5b25d-106">Дополнительные сведения см. в разделе [начальная загрузка Интернета](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="5b25d-106">For more information see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

<span data-ttu-id="5b25d-107">Введите следующую командную строку, чтобы настроить ресурсы для образца, описанного в [примере установки установщик Windows на основе URL-адреса](a-url-based-windows-installer-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="5b25d-107">Entering the following command line configures the resources for the sample described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span>

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[<span data-ttu-id="5b25d-108">Продолжить</span><span class="sxs-lookup"><span data-stu-id="5b25d-108">Continue</span></span>](sign-setup-exe-and-mysetup-msi.md)

 

 



