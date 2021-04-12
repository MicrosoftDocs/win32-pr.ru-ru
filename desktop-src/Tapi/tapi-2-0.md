---
description: TAPI 2,0 предоставляет небольшое количество улучшений базовой функциональности TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345425"
---
# <a name="tapi-20"></a><span data-ttu-id="086dd-103">TAPI 2,0</span><span class="sxs-lookup"><span data-stu-id="086dd-103">TAPI 2.0</span></span>

<span data-ttu-id="086dd-104">TAPI 2,0 предоставляет небольшое количество улучшений базовой функциональности TAPI 1,4.</span><span class="sxs-lookup"><span data-stu-id="086dd-104">TAPI 2.0 provides a small number of enhancements to the basic TAPI 1.4 functionality.</span></span> <span data-ttu-id="086dd-105">Однако были внесены значительные изменения в архитектуру, которые значительно улучшили стабильность.</span><span class="sxs-lookup"><span data-stu-id="086dd-105">However, there were some major architectural changes that greatly improved its stability.</span></span> <span data-ttu-id="086dd-106">Большинство изменений были фундаментальными изменениями, необходимыми для переноса TAPI в Windows NT 4,0 и использования его возможностей (полной 32-разрядной поддержки, служб и Юникода).</span><span class="sxs-lookup"><span data-stu-id="086dd-106">Most of the changes were fundamental changes necessary to bring TAPI to Windows NT 4.0 and take advantage of its features (full 32-bit support, services, and Unicode).</span></span> <span data-ttu-id="086dd-107">Однако эти изменения были внутренними в TAPI и не оказывают влияния на приложения TAPI.</span><span class="sxs-lookup"><span data-stu-id="086dd-107">However, these changes were internal to TAPI and had little effect on TAPI applications.</span></span>

<span data-ttu-id="086dd-108">Приложения, поддерживающие TAPI 1,3 и 1,4 (16-разрядные приложения с помощью слоя преобразования), хорошо работают в операционных системах Windows Server 2003, Windows XP, Windows 2000 и Windows NT.</span><span class="sxs-lookup"><span data-stu-id="086dd-108">Applications that support TAPI 1.3 and 1.4 (16-bit applications by way of a thunking layer) work well on Windows Server 2003 operating systems, Windows XP, Windows 2000, and Windows NT.</span></span> <span data-ttu-id="086dd-109">Однако воздействие на разработчиков поставщиков услуг было существенным.</span><span class="sxs-lookup"><span data-stu-id="086dd-109">However, the effect on service-provider developers was significant.</span></span> <span data-ttu-id="086dd-110">Поставщики услуг для этих операционных систем должны быть полностью 32-битовыми библиотеками Юникода, которые могут выполняться в контексте ТАПИСРВ, а не в контексте приложения TAPI (как и все более ранние специалистами на основе Win16).</span><span class="sxs-lookup"><span data-stu-id="086dd-110">Service providers for these operating systems must be fully 32-bit Unicode DLLs that can run in the context of TAPISRV, not in the context of the TAPI application (as did all earlier Win16-based TSPs).</span></span> <span data-ttu-id="086dd-111">Специалистами, разработанный для TAPI 1,4, не работает в операционных системах Windows Server 2003, Windows XP, Windows 2000 или Windows NT.</span><span class="sxs-lookup"><span data-stu-id="086dd-111">TSPs designed for TAPI 1.4 do not work on Windows Server 2003 operating systems, Windows XP, Windows 2000, or Windows NT.</span></span>

<span data-ttu-id="086dd-112">TAPI 2,0 также добавляет важные функции поддержки центра обработки вызовов и качества обслуживания (QOS).</span><span class="sxs-lookup"><span data-stu-id="086dd-112">TAPI 2.0 also adds the important features of call center support and Quality of Service (QOS) support.</span></span>

<span data-ttu-id="086dd-113">Системные двоичные файлы TAPI, которые входят в состав Windows, поддерживают TAPI версии 1,3 и 1,4 для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="086dd-113">The TAPI system binaries that come with Windows support TAPI versions 1.3 and 1.4 for all applications.</span></span> <span data-ttu-id="086dd-114">Однако 16-разрядные приложения не могут использовать TAPI 2,0, и вы не можете использовать 16-разрядный TSP TAPI 2. x.</span><span class="sxs-lookup"><span data-stu-id="086dd-114">However, 16-bit applications cannot use TAPI 2.0, and you cannot use a 16-bit TAPI 2.x TSP.</span></span>

 

 



