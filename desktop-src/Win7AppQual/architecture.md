---
description: Слабо связанный Internet Explorer (ЛЦИЕ) повышает надежность обозревателя за счет разделения компонентов и ослабления их взаимозависимости.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Архитектура (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818465"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="7f194-103">Архитектура (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="7f194-103">Architecture (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="7f194-104">*Слабо связанный Internet Explorer* (лЦие) повышает надежность обозревателя за счет разделения компонентов и ослабления их взаимозависимости.</span><span class="sxs-lookup"><span data-stu-id="7f194-104">*Loosely-coupled Internet Explorer* (LCIE) improves the browser’s reliability by separating its components and loosening their interdependence.</span></span>

<span data-ttu-id="7f194-105">В частности, ЛЦИЕ пытается изолировать фрейм Windows Internet Explorer и его вкладки в отдельных процессах.</span><span class="sxs-lookup"><span data-stu-id="7f194-105">In particular, LCIE tries to isolate the Windows Internet Explorer frame and its tabs into separate processes.</span></span> <span data-ttu-id="7f194-106">В Windows Internet Explorer 8 такая изоляция повышает производительность и масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="7f194-106">In Windows Internet Explorer 8, this isolation improves performance and scalability.</span></span> <span data-ttu-id="7f194-107">Это изменение архитектуры может повлиять на совместимость расширений и надстроек, включая элементы управления ActiveX, вспомогательные объекты браузера (BHO) и компоненты панели инструментов пользовательского интерфейса, созданные с помощью старых методов программирования.</span><span class="sxs-lookup"><span data-stu-id="7f194-107">This architectural change might affect the compatibility of extensions and add-ons, including ActiveX Controls, Browser Helper Objects (BHOs), and UI toolbar components that are built by using older programming techniques.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f194-108">См. также</span><span class="sxs-lookup"><span data-stu-id="7f194-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f194-109">Разработка обновлений, влияющих на совместимость браузеров</span><span class="sxs-lookup"><span data-stu-id="7f194-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



