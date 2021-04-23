---
title: Использование элемента управления ActiveX удаленный рабочий стол
description: Использование элемента управления удаленный рабочий стол ActiveX для настройки службы удаленных рабочих столов взаимодействия с пользователем.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов службы удаленных рабочих столов с помощью элемента управления ActiveX удаленный рабочий стол
- Веб-подключение к удаленному рабочему столу службы удаленных рабочих столов с помощью
- протокол удаленного рабочего стола службы удаленных рабочих столов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681392"
---
# <a name="using-the-remote-desktop-activex-control"></a><span data-ttu-id="2ff21-106">Использование элемента управления ActiveX удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="2ff21-106">Using the Remote Desktop ActiveX control</span></span>

<span data-ttu-id="2ff21-107">В следующих разделах содержатся сведения об использовании элемента управления ActiveX удаленный рабочий стол для настройки службы удаленных рабочих столов взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="2ff21-107">The following topics contain information about how you can use the Remote Desktop ActiveX control to customize the Remote Desktop Services user experience.</span></span>

<span data-ttu-id="2ff21-108">Удаленный рабочий стол элемент управления ActiveX доступен в следующих формах:</span><span class="sxs-lookup"><span data-stu-id="2ff21-108">The Remote Desktop ActiveX control is available in the following forms:</span></span>

-   <span data-ttu-id="2ff21-109">**Элемент управления для сценариев**— реализует интерфейсы, которые являются надежными для сценариев.</span><span class="sxs-lookup"><span data-stu-id="2ff21-109">**The scriptable control**—implements interfaces that are safe for scripting.</span></span> <span data-ttu-id="2ff21-110">Эта форма элемента управления может использоваться веб-клиентами или сценариями (например, VBScript).</span><span class="sxs-lookup"><span data-stu-id="2ff21-110">This form of the control can be used by web clients or scripting (such as VBScript) hosts.</span></span>
-   <span data-ttu-id="2ff21-111">**Необрабатываемый элемент управления**— предоставляет дополнительные функциональные возможности, которые не являются надежными для сценариев.</span><span class="sxs-lookup"><span data-stu-id="2ff21-111">**The nonscriptable control**—offers additional functionality that is not safe for scripting.</span></span> <span data-ttu-id="2ff21-112">Эту форму элемента управления можно использовать из машинного или управляемого кода, но эта форма не может использоваться веб-клиентами или узлами, использующими только скрипты.</span><span class="sxs-lookup"><span data-stu-id="2ff21-112">This form of the control can be used from native or managed code, but this form cannot be used by web clients or scripting-only hosts.</span></span>

<span data-ttu-id="2ff21-113">Следующий список содержит **идентификаторы CLSID** для различных элементов управления для различных версий операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2ff21-113">The following list contains the **CLSID** s for the different controls for different operating system versions.</span></span> <span data-ttu-id="2ff21-114">Каждый **идентификатор CLSID** совместим с более поздними версиями системы.</span><span class="sxs-lookup"><span data-stu-id="2ff21-114">Each of the **CLSID** s is compatible with later system versions.</span></span> <span data-ttu-id="2ff21-115">Например, **идентификатор CLSID** для элемента управления с сценарием в Windows Vista будет работать в более поздних версиях системы, таких как Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2ff21-115">For example, the **CLSID** for the scriptable control on Windows Vista will work on later system versions, such as Windows 7.</span></span>



| <span data-ttu-id="2ff21-116">Версия системы</span><span class="sxs-lookup"><span data-stu-id="2ff21-116">System version</span></span>                          | <span data-ttu-id="2ff21-117">CLSID элемента управления, поддерживающий Скрипт</span><span class="sxs-lookup"><span data-stu-id="2ff21-117">Scriptable control CLSID</span></span>             | <span data-ttu-id="2ff21-118">Нескриптовый CLSID элемента управления</span><span class="sxs-lookup"><span data-stu-id="2ff21-118">Nonscriptable control CLSID</span></span>          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="2ff21-119">Windows 8.1, Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2ff21-119">Windows 8.1, Windows Server 2012 R2</span></span>     | <span data-ttu-id="2ff21-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="2ff21-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span> | <span data-ttu-id="2ff21-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="2ff21-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span> |
| <span data-ttu-id="2ff21-122">Windows 8, Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ff21-122">Windows 8, Windows Server 2012</span></span>          | <span data-ttu-id="2ff21-123">5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="2ff21-123">5F681803-2900-4C43-A1CC-CF405404A676</span></span> | <span data-ttu-id="2ff21-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="2ff21-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span> |
| <span data-ttu-id="2ff21-125">Windows 7, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff21-125">Windows 7, Windows Server 2008</span></span>          | <span data-ttu-id="2ff21-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="2ff21-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span> | <span data-ttu-id="2ff21-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="2ff21-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span> |
| <span data-ttu-id="2ff21-128">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="2ff21-128">Windows Vista with Service Pack 1 (SP1)</span></span> | <span data-ttu-id="2ff21-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span><span class="sxs-lookup"><span data-stu-id="2ff21-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span> | <span data-ttu-id="2ff21-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="2ff21-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span> |
| <span data-ttu-id="2ff21-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ff21-131">Windows Vista</span></span>                           | <span data-ttu-id="2ff21-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span><span class="sxs-lookup"><span data-stu-id="2ff21-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span> | <span data-ttu-id="2ff21-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span><span class="sxs-lookup"><span data-stu-id="2ff21-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="2ff21-134">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2ff21-134">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2ff21-135">Внедрение удаленный рабочий стол элемента управления ActiveX на веб-страницу</span><span class="sxs-lookup"><span data-stu-id="2ff21-135">Embedding the Remote Desktop ActiveX control in a webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

<span data-ttu-id="2ff21-136">Пример, демонстрирующий использование интерфейсов, поддерживающих сценарии.</span><span class="sxs-lookup"><span data-stu-id="2ff21-136">Example that demonstrates the use of the scriptable interfaces.</span></span>

</dd> <dt>

[<span data-ttu-id="2ff21-137">Реализация виртуальных каналов с использованием скриптов с помощью веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="2ff21-137">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="2ff21-138">Примеры кода, демонстрирующие шаги для реализации виртуальных каналов с помощью сценариев с веб-подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="2ff21-138">Code examples that show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2ff21-139">Использование элемента управления ActiveX удаленный рабочий стол с виртуальными каналами</span><span class="sxs-lookup"><span data-stu-id="2ff21-139">Using the Remote Desktop ActiveX control with virtual channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="2ff21-140">Если вы включили приложение виртуальных каналов в развертывание службы удаленных рабочих столов, это приложение можно будет сделать доступным для клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="2ff21-140">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers.</span></span>

</dd> <dt>

[<span data-ttu-id="2ff21-141">Пример веб-страницы, входящей в состав элемента управления удаленный рабочий стол ActiveX</span><span class="sxs-lookup"><span data-stu-id="2ff21-141">Sample webpage included with the Remote Desktop ActiveX control</span></span>](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="2ff21-142">Пример веб-страницы (Default.htm) находится в каталоге, где установлена веб-подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="2ff21-142">A sample webpage (Default.htm) is in the directory where Remote Desktop Web Connection is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="2ff21-143">Предоставление для безопасности клиента RDP</span><span class="sxs-lookup"><span data-stu-id="2ff21-143">Providing for RDP client security</span></span>](providing-for-rdp-client-security.md)
</dt> <dd>

<span data-ttu-id="2ff21-144">Некоторые свойства объекта элемента управления ActiveX удаленный рабочий стол ограничены определенными зонами безопасности URL-адресов Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2ff21-144">Some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span>

</dd> <dt>

[<span data-ttu-id="2ff21-145">Отключение функций службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="2ff21-145">Disabling Remote Desktop Services features</span></span>](disabling-terminal-services-features.md)
</dt> <dd>

<span data-ttu-id="2ff21-146">Для повышения безопасности можно отключить службы удаленных рабочих столов функции.</span><span class="sxs-lookup"><span data-stu-id="2ff21-146">For enhanced security, you might choose to disable Remote Desktop Services features.</span></span>

</dd> </dl>

<span data-ttu-id="2ff21-147">Дополнительные сведения о примере веб-страницы, которая входит в состав установки элемента управления ActiveX удаленный рабочий стол, см. [в разделе Пример веб-страницы, включенной в удаленный рабочий стол элемент управления ActiveX](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span><span class="sxs-lookup"><span data-stu-id="2ff21-147">For more information about the sample webpage that is included with the installation of the Remote Desktop ActiveX control, see [Sample webpage included with the Remote Desktop ActiveX control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 




