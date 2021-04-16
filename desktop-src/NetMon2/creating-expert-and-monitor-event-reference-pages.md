---
description: В этом разделе описывается планирование, разработка и тестирование страниц справочника по событиям (ERP) и их развертывание в эксперте или мониторе. Сведения о ERP и об их использовании с сетевой монитор см. на странице справочника по событиям.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Создание страниц со ссылками на события экспертов и мониторинга
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650772"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a><span data-ttu-id="70b1a-104">Создание страниц со ссылками на события экспертов и мониторинга</span><span class="sxs-lookup"><span data-stu-id="70b1a-104">Creating Expert and Monitor Event Reference Pages</span></span>

<span data-ttu-id="70b1a-105">В этом разделе описывается планирование, разработка и тестирование страниц справочника по событиям (ERP) и их развертывание в эксперте или мониторе.</span><span class="sxs-lookup"><span data-stu-id="70b1a-105">This section describes how to plan, develop, and test event reference pages (ERPs) and how to deploy them in an expert or monitor.</span></span> <span data-ttu-id="70b1a-106">Сведения о ERP и об их использовании с сетевой монитор см. [на странице справочника по событиям](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="70b1a-106">For information about ERPs and how to use them with Network Monitor, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="70b1a-107">Для разработки нового ERP первым шагом является определение событий, требующих отдельного ERP для Вашего специализированного [эксперта](experts.md) или [монитора](monitors.md).</span><span class="sxs-lookup"><span data-stu-id="70b1a-107">To develop a new ERP, the first step is determining the events that require individual ERPs for your custom [expert](experts.md) or [monitor](monitors.md).</span></span> <span data-ttu-id="70b1a-108">Для каждого события, которое необходимо отобразить в сетевой монитор Просмотр событий, необходимо создать отдельный ERP.</span><span class="sxs-lookup"><span data-stu-id="70b1a-108">You must create separate ERPs for each event you wish to display in the Network Monitor Event Viewer.</span></span> <span data-ttu-id="70b1a-109">Например, предположим, что:</span><span class="sxs-lookup"><span data-stu-id="70b1a-109">For example, suppose that:</span></span>

-   <span data-ttu-id="70b1a-110">Вы разрабатываете монитор с именем "игровой монитор" и "наблюдатель запасов".</span><span class="sxs-lookup"><span data-stu-id="70b1a-110">You develop a monitor named Game Monitor and Stock Watcher.</span></span>
-   <span data-ttu-id="70b1a-111">Монитор находится в файле с именем Gamemon.dll.</span><span class="sxs-lookup"><span data-stu-id="70b1a-111">The monitor is located in a file called Gamemon.dll.</span></span>
-   <span data-ttu-id="70b1a-112">Монитор создает два события: игра запущена и моя Интернет Nowalking.</span><span class="sxs-lookup"><span data-stu-id="70b1a-112">The monitor generates two events, Game Running and My Internet Stock Soars.</span></span>
-   <span data-ttu-id="70b1a-113">Планируется разработка двух ERP, Gamemon1.htm и Gamemon2.htm.</span><span class="sxs-lookup"><span data-stu-id="70b1a-113">You plan to develop two ERPs, Gamemon1.htm and Gamemon2.htm.</span></span>

> [!Note]  
> <span data-ttu-id="70b1a-114">Нет необходимости иметь соответствие "один к одному" ERP для отслеживания или экспертных мероприятий.</span><span class="sxs-lookup"><span data-stu-id="70b1a-114">It's not necessary to have a one-to-one correspondence of ERPs to monitor or expert events.</span></span>

 

<span data-ttu-id="70b1a-115">После создания списка уникальных ERP выполните следующие действия, чтобы создать каждый ERP-процесс.</span><span class="sxs-lookup"><span data-stu-id="70b1a-115">After you have established a list of unique ERPs, follow these steps to create each ERP.</span></span>

-   <span data-ttu-id="70b1a-116">[Напишите исходный HTML-документ](writing-an-event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="70b1a-116">[Write the HTML source document](writing-an-event-reference-page.md).</span></span>
-   <span data-ttu-id="70b1a-117">[Сохраните и присвойте](naming-an-event-reference-page.md) исходному файлу HTML имя в виде HTM-файла.</span><span class="sxs-lookup"><span data-stu-id="70b1a-117">[Save and name](naming-an-event-reference-page.md) the HTML source file as an .htm file.</span></span>
-   <span data-ttu-id="70b1a-118">[Протестируйте ERP](testing-an-event-reference-page.md) с завершенным экспертом или монитором.</span><span class="sxs-lookup"><span data-stu-id="70b1a-118">[Test the ERP](testing-an-event-reference-page.md) with the completed expert or monitor.</span></span>

 

 



