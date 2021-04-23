---
description: В этом документе содержатся сведения о вопросах безопасности, связанных с получением образа Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Вопросы безопасности: получение образа Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711089"
---
# <a name="security-considerations-windows-image-acquisition"></a><span data-ttu-id="5c7b9-103">Вопросы безопасности: получение образа Windows</span><span class="sxs-lookup"><span data-stu-id="5c7b9-103">Security Considerations: Windows Image Acquisition</span></span>

<span data-ttu-id="5c7b9-104">В этом документе содержатся сведения о вопросах безопасности, связанных с получением образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="5c7b9-104">This document provides information about security considerations related to Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="5c7b9-105">Этот документ не предоставляет все, что нужно знать о проблемах безопасности. вместо этого используйте его в качестве отправной точки и справочной информации для этой области технологий.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-105">This document doesn't provide all you need to know about security issues - instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="5c7b9-106">Используйте кавычки вокруг имен путей</span><span class="sxs-lookup"><span data-stu-id="5c7b9-106">Use quotation marks around path names</span></span>](#use-quotation-marks-around-path-names)
-   [<span data-ttu-id="5c7b9-107">Размещение зарегистрированных приложений в защищенных расположениях</span><span class="sxs-lookup"><span data-stu-id="5c7b9-107">Place registered applications in secure locations</span></span>](#place-registered-applications-in-secure-locations)
-   [<span data-ttu-id="5c7b9-108">Не используйте базовые каталоги или разделы реестра</span><span class="sxs-lookup"><span data-stu-id="5c7b9-108">Do not use underlying directories or registry keys</span></span>](#do-not-use-underlying-directories-or-registry-keys)
-   [<span data-ttu-id="5c7b9-109">См. также</span><span class="sxs-lookup"><span data-stu-id="5c7b9-109">Related Topics</span></span>](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a><span data-ttu-id="5c7b9-110">Используйте кавычки вокруг имен путей</span><span class="sxs-lookup"><span data-stu-id="5c7b9-110">Use quotation marks around path names</span></span>

<span data-ttu-id="5c7b9-111">При использовании [**ивиадевмгр:: регистеревенткаллбаккпрограм**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) для регистрации приложения для получения событий устройства обязательно заключите путь и имя файла приложения в кавычки.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-111">When using [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register an application to receive device events, be sure to surround the path and filename of the application with quotation marks.</span></span> <span data-ttu-id="5c7b9-112">Это позволяет избежать неправильной интерпретации пути и запуска неавторизованного приложения.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-112">This avoids the possibility that the path is misinterpreted and an unauthorized application is run.</span></span>

## <a name="place-registered-applications-in-secure-locations"></a><span data-ttu-id="5c7b9-113">Размещение зарегистрированных приложений в защищенных расположениях</span><span class="sxs-lookup"><span data-stu-id="5c7b9-113">Place registered applications in secure locations</span></span>

<span data-ttu-id="5c7b9-114">Когда приложение регистрируется для получения события устройства, оно может быть запущено любым пользователем, имеющим доступ к этому устройству.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-114">When an application is registered to receive a device event, that application can be run by any user that has access to that device.</span></span> <span data-ttu-id="5c7b9-115">Например, если приложение зарегистрировано для события сканирования, нажатие кнопки "Сканировать" на сканере приведет к запуску этого приложения.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-115">For example, if an application is registered for a scan event, pressing the "scan" button on a scanner will cause that application to run.</span></span> <span data-ttu-id="5c7b9-116">Если приложение работает с более высокой привилегией, чем у пользователя, это вызывает потенциальную угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-116">If the application runs with a higher privilege than the user has, this causes a potential security issue.</span></span>

## <a name="do-not-use-underlying-directories-or-registry-keys"></a><span data-ttu-id="5c7b9-117">Не используйте базовые каталоги или разделы реестра</span><span class="sxs-lookup"><span data-stu-id="5c7b9-117">Do not use underlying directories or registry keys</span></span>

<span data-ttu-id="5c7b9-118">Для хранения данных или информации WIA использует несколько каталогов и разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-118">WIA uses several directories and registry keys internally to store data or information.</span></span> <span data-ttu-id="5c7b9-119">Не изменяйте доступ к этим каталогам или разделам реестра напрямую.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-119">Do not access these directories or registry keys directly.</span></span> <span data-ttu-id="5c7b9-120">Вместо этого используйте предоставляемые методы интерфейса, чтобы указать каталоги для полученных изображений.</span><span class="sxs-lookup"><span data-stu-id="5c7b9-120">Instead, use the exposed interface methods to specify directories for acquired images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c7b9-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5c7b9-121">Related Topics</span></span>

-   [<span data-ttu-id="5c7b9-122">Microsoft Security</span><span class="sxs-lookup"><span data-stu-id="5c7b9-122">Microsoft Security</span></span>](https://www.microsoft.com/security/)
-   [<span data-ttu-id="5c7b9-123">Домашняя страница безопасности библиотеки MSDN</span><span class="sxs-lookup"><span data-stu-id="5c7b9-123">MSDN Library Security Home Page</span></span>](https://msdn.microsoft.com/security/default.aspx)
-   [<span data-ttu-id="5c7b9-124">Материалы по безопасности</span><span class="sxs-lookup"><span data-stu-id="5c7b9-124">Security How-to Resources</span></span>](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [<span data-ttu-id="5c7b9-125">Материалы по безопасности TechNet</span><span class="sxs-lookup"><span data-stu-id="5c7b9-125">TechNet Security Resources</span></span>](https://technet.microsoft.com/security/default.aspx)
-   <span data-ttu-id="5c7b9-126">[Вопросы безопасности для разработчиков Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="5c7b9-126">[Security Considerations for Windows XP Embedded Developers](/previous-versions/ms838345(v=msdn.10))</span></span>
-   [<span data-ttu-id="5c7b9-127">Рекомендации по обеспечению безопасности</span><span class="sxs-lookup"><span data-stu-id="5c7b9-127">Security Best Practices</span></span>](../secbp/best-practices-for-the-security-apis.md)

 

 
