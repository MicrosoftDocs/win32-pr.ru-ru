---
title: Windows 10
description: Эта Cookbook предоставляет разработчикам сведения об изменениях платформы в операционных системах Windows 10.
ms.assetid: bf8d7d10-bab6-4711-b65f-5393d906e47b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03fce627969573deb395fda356564a85a3573682
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413503"
---
# <a name="windows-10"></a><span data-ttu-id="567a2-103">Windows 10</span><span class="sxs-lookup"><span data-stu-id="567a2-103">Windows 10</span></span>

<span data-ttu-id="567a2-104">Эта Cookbook предоставляет разработчикам сведения об изменениях платформы в операционных системах Windows 10.</span><span class="sxs-lookup"><span data-stu-id="567a2-104">This Cookbook provides info for developers about platform changes to the Windows 10 operating systems (OS).</span></span> <span data-ttu-id="567a2-105">Мы также предоставляем рекомендации по проверке совместимости существующих и запланированных приложений с последней версией операционной системы.</span><span class="sxs-lookup"><span data-stu-id="567a2-105">We also provide guidelines for you to verify the compatibility of your existing and planned apps with the latest version of the OS.</span></span> <span data-ttu-id="567a2-106">Предполагается, что вы знакомы с предыдущими версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="567a2-106">We assume that you are familiar with previous versions of Windows.</span></span>

<span data-ttu-id="567a2-107">Содержимое применяется к: Windows 10</span><span class="sxs-lookup"><span data-stu-id="567a2-107">The content applies to: Windows 10</span></span>

<span data-ttu-id="567a2-108">Cookbook предназначен для сторонних разработчиков приложений и устройств, предназначенных для использования в среде Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="567a2-108">The Cookbook is for third party developers of apps and devices that are designed to be used in the Microsoft Windows environment.</span></span>

## <a name="introduction"></a><span data-ttu-id="567a2-109">Введение</span><span class="sxs-lookup"><span data-stu-id="567a2-109">Introduction</span></span>

<span data-ttu-id="567a2-110">В Windows 10 появилась последняя версия технологии ОС и платформы разработки программного обеспечения, используемая разработчиками приложений и драйверов, а также предприятиями по всему миру.</span><span class="sxs-lookup"><span data-stu-id="567a2-110">Windows 10 introduces the latest OS technology and software development platforms for use by app and driver developers and enterprises worldwide.</span></span> <span data-ttu-id="567a2-111">Для дальнейшего повышения безопасности, надежности, производительности и взаимодействия с пользователем в Windows корпорация Майкрософт представила множество новых функций, улучшенные существующие функции и удалила другие.</span><span class="sxs-lookup"><span data-stu-id="567a2-111">To further enhance the security, reliability, performance, and user experience of Windows, Microsoft has introduced many new features, improved existing features, and removed others.</span></span>

<span data-ttu-id="567a2-112">Хотя целью Windows 10 является обеспечение совместимости с приложениями, написанными для ранее выпущенных версий ОС Windows, некоторые нарушения совместимости неизбежны из-за нововведений, усиленной безопасности и повышенной надежности.</span><span class="sxs-lookup"><span data-stu-id="567a2-112">While the goal of Windows 10 is to maintain compatibility with apps written for previously released versions of the Windows OS, some compatibility breaks are inevitable due to innovations, tightened security, and increased reliability.</span></span> <span data-ttu-id="567a2-113">В целом совместимость с последней версией ОС Windows с существующими приложениями и устройствами является высокой.</span><span class="sxs-lookup"><span data-stu-id="567a2-113">Overall, the compatibility of the latest version of the Windows OS with existing apps and devices is high.</span></span>

<span data-ttu-id="567a2-114">В этом документе показано, как проверить, совместимы ли ваши приложения и устройства с последней версией ОС, а также обзор известных проблем несовместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="567a2-114">This document shows you how to verify that your apps and devices are compatible with the latest version of the OS and provides an overview of known app incompatibility issues.</span></span>

<span data-ttu-id="567a2-115">Мы приглашаем вас ознакомиться с этими статьями, чтобы узнать, как оптимизировать приложения и воспользоваться преимуществами новых выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="567a2-115">We invite you to check out these topics to learn how to optimize your apps and take advantage of what this newest release of Windows has to offer.</span></span>

## <a name="contents"></a><span data-ttu-id="567a2-116">Содержимое</span><span class="sxs-lookup"><span data-stu-id="567a2-116">Contents</span></span>

-   [<span data-ttu-id="567a2-117">Основные изменения с момента выпуска Windows 7 для обеспечения совместимости</span><span class="sxs-lookup"><span data-stu-id="567a2-117">Key changes since Windows 7 to ensure compatibility</span></span>](key-changes-since-windows-7-to-ensure-compatibility.md)
-   [<span data-ttu-id="567a2-118">Как обеспечить совместимость Объединенной экосистемы</span><span class="sxs-lookup"><span data-stu-id="567a2-118">How we can ensure compatibility of the combined ecosystem</span></span>](how-we-can-ensure-compatibility-of-the-combined-ecosystem.md)
    -   [<span data-ttu-id="567a2-119">Проверка версии Windows</span><span class="sxs-lookup"><span data-stu-id="567a2-119">Windows version check</span></span>](windows-version-check.md)
    -   [<span data-ttu-id="567a2-120">Недокументированные API</span><span class="sxs-lookup"><span data-stu-id="567a2-120">Undocumented APIs</span></span>](undocumented-apis.md)
    -   [<span data-ttu-id="567a2-121">Разрабатывайте приложения UWP и Desktop Bridge</span><span class="sxs-lookup"><span data-stu-id="567a2-121">Develop UWP and Desktop Bridge apps</span></span>](/windows/desktop/w8cookbook/develop-universal-windows-platform-apps)
    -   [<span data-ttu-id="567a2-122">Современные функции настольных приложений затрагиваются, если не выполняются в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="567a2-122">Modern Desktop App functionality is impacted if not run in Windowed Mode</span></span>](modern-desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode.md)
    -   [<span data-ttu-id="567a2-123">Доступность применимых драйверов графики на Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="567a2-123">Availability of applicable graphics drivers on Windows Update</span></span>](availability-of-applicable-graphics-drivers-on-windows-update.md)
    -   [<span data-ttu-id="567a2-124">Перенос драйвера графики на Windows 10</span><span class="sxs-lookup"><span data-stu-id="567a2-124">Graphics driver migration to Windows 10</span></span>](graphics-driver-migration-to-windows-10.md)
    -   [<span data-ttu-id="567a2-125">Драйверы Bluetooth</span><span class="sxs-lookup"><span data-stu-id="567a2-125">Bluetooth drivers</span></span>](bluetooth-drivers.md)

## <a name="download-the-cookbook"></a><span data-ttu-id="567a2-126">Скачивание Cookbook</span><span class="sxs-lookup"><span data-stu-id="567a2-126">Download the cookbook</span></span>

<span data-ttu-id="567a2-127">Чтобы получить краткий справочник по всей этой информации, а также сведения о Windows как службе, поддержке приложений в Windows и оптимизированных стратегиях тестирования приложения, [Скачайте Cookbook совместимости Windows 10](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span><span class="sxs-lookup"><span data-stu-id="567a2-127">For a quick reference to all this information, as well as information on Windows as a service, supporting apps in Windows, and optimized strategies for testing your app, [download the Windows 10 Compatibility Cookbook](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span></span>

## <a name="see-also"></a><span data-ttu-id="567a2-128">См. также:</span><span class="sxs-lookup"><span data-stu-id="567a2-128">See Also</span></span>

-   <span data-ttu-id="567a2-129">[Windows как услуга](/windows/deployment/update/)для получения сведений о типах выпусков Windows 10 и поддержке приложений.</span><span class="sxs-lookup"><span data-stu-id="567a2-129">[Windows as a service](/windows/deployment/update/), for information about Windows 10 release types and app support.</span></span>
-   <span data-ttu-id="567a2-130">[Предварительная версия Windows](https://insider.windows.com/), для доступа к предварительным сборкам, тестирования и предоставления отзывов.</span><span class="sxs-lookup"><span data-stu-id="567a2-130">[Windows Insider](https://insider.windows.com/), to access preview builds, test, and provide feedback.</span></span>
-   <span data-ttu-id="567a2-131">[Все готово для Windows 10](https://www.readyfor10.com/), чтобы отправить сведения об Организации в ресурс для ИТ-руководителей.</span><span class="sxs-lookup"><span data-stu-id="567a2-131">[Ready for Windows 10](https://www.readyfor10.com/), to submit your company's information to a resource for IT managers.</span></span>

 

 