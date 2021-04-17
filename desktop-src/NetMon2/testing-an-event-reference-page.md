---
description: Заключительный этап создания страницы ссылки на события (ERP) заключается в его тестировании.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Тестирование страницы ссылки на событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673327"
---
# <a name="testing-an-event-reference-page"></a><span data-ttu-id="5c1af-103">Тестирование страницы ссылки на событие</span><span class="sxs-lookup"><span data-stu-id="5c1af-103">Testing an Event Reference Page</span></span>

<span data-ttu-id="5c1af-104">Заключительный этап создания страницы ссылки на события (ERP) заключается в его тестировании.</span><span class="sxs-lookup"><span data-stu-id="5c1af-104">The final step of creating an event reference page (ERP) is to test it.</span></span> <span data-ttu-id="5c1af-105">Вы можете протестировать ERP, просмотрев файл в браузере HTML, таком как Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5c1af-105">You can test an ERP by viewing the file in an HTML browser such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="5c1af-106">Вы также можете установить ERP и его экспертную библиотеку DLL, чтобы протестировать его для вызова событий и отобразить его в сетевой монитор Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="5c1af-106">Or, you can install the ERP and its expert DLL to test it for event invocation and display it in the Network Monitor Event Viewer.</span></span>

## <a name="viewing-erps-that-have-no-dll"></a><span data-ttu-id="5c1af-107">Просмотр ERP, не имеющих библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="5c1af-107">Viewing ERPs that Have No DLL</span></span>

<span data-ttu-id="5c1af-108">Чтобы просмотреть завершенный ERP без установленной библиотеки DLL эксперта, откройте файл с помощью средства просмотра HTML-страниц, поддерживающего внедренные источники.</span><span class="sxs-lookup"><span data-stu-id="5c1af-108">To view the completed ERP without an installed expert DLL, open the file with an HTML viewer that supports your embedded sources.</span></span> <span data-ttu-id="5c1af-109">На следующем рисунке показан пример ERP-файла, описанный в статье [создание ERP](writing-an-event-reference-page.md) -файлов в том виде, в котором он отображается с помощью Microsoft Internet Explorer версии 4,01.</span><span class="sxs-lookup"><span data-stu-id="5c1af-109">The following illustration shows the sample ERP file described in [Writing an ERP](writing-an-event-reference-page.md) as it is displayed using Microsoft Internet Explorer Version 4.01.</span></span>

![Пример файла ERP](images/ie-erp.png)

<span data-ttu-id="5c1af-111">Тестирование ERP с библиотекой DLL</span><span class="sxs-lookup"><span data-stu-id="5c1af-111">Testing ERPs that Have a DLL</span></span>

<span data-ttu-id="5c1af-112">После создания ERP-файлов и библиотеки DLL [**экспертов**](experts.md) можно протестировать полную функциональность erp с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="5c1af-112">After the ERP files and the [**expert**](experts.md) DLL is created, you can test the complete functionality of your ERPs with Network Monitor.</span></span> <span data-ttu-id="5c1af-113">Предполагается, что библиотека DLL отлаживается и может создавать допустимые события.</span><span class="sxs-lookup"><span data-stu-id="5c1af-113">It is assumed that the DLL is debugged and can generate valid events.</span></span>

<span data-ttu-id="5c1af-114">**Тестирование ERP с библиотекой DLL**</span><span class="sxs-lookup"><span data-stu-id="5c1af-114">**To test ERPs that have a DLL**</span></span>

1.  <span data-ttu-id="5c1af-115">Убедитесь, что в соответствующем каталоге установлена правильная библиотека DLL эксперта.</span><span class="sxs-lookup"><span data-stu-id="5c1af-115">Verify that the correct expert DLL is installed in the appropriate directory.</span></span> <span data-ttu-id="5c1af-116">Дополнительные сведения см. [в статье Установка эксперта в сетевой монитор 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="5c1af-116">For more information, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="5c1af-117">Проверьте [правильное имя](naming-an-event-reference-page.md) ERP файла.</span><span class="sxs-lookup"><span data-stu-id="5c1af-117">Verify the [correct name](naming-an-event-reference-page.md) of the ERP file.</span></span>
3.  <span data-ttu-id="5c1af-118">Проверьте [правильное расположение](installing-existing-erps-to-network-monitor-2-1.md) ERP в каталоге сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="5c1af-118">Verify the [correct location](installing-existing-erps-to-network-monitor-2-1.md) of the ERPs in the Network Monitor directory.</span></span>
4.  <span data-ttu-id="5c1af-119">Тест-эксперт ERP в пользовательском интерфейсе сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="5c1af-119">Test expert ERPs in the Network Monitor UI.</span></span>
5.  <span data-ttu-id="5c1af-120">Создание тестового события.</span><span class="sxs-lookup"><span data-stu-id="5c1af-120">Generate a test event.</span></span>
6.  <span data-ttu-id="5c1af-121">Убедитесь, что ERP отображается в Просмотр событий сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="5c1af-121">Verify that the ERP appears in the Network Monitor Event Viewer.</span></span>

<span data-ttu-id="5c1af-122">Дополнительные сведения о создании ERP см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="5c1af-122">For more information about creating an ERP, see:</span></span>

-   [<span data-ttu-id="5c1af-123">Создание страниц со ссылками на события экспертов и мониторинга</span><span class="sxs-lookup"><span data-stu-id="5c1af-123">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="5c1af-124">Создание страницы ссылки на событие</span><span class="sxs-lookup"><span data-stu-id="5c1af-124">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="5c1af-125">Именование страницы ссылки на события</span><span class="sxs-lookup"><span data-stu-id="5c1af-125">Naming an Event Reference Page</span></span>](naming-an-event-reference-page.md)

 

 



