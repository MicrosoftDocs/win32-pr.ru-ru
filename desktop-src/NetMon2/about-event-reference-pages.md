---
description: Страница ссылки на события (ERP) — это HTML-документ, который предоставляет сетевой монитор сведения о событиях, обнаруженных во время работы эксперта или монитора.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Сведения о страницах ссылок на события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910087"
---
# <a name="about-event-reference-pages"></a><span data-ttu-id="a9381-103">Сведения о страницах ссылок на события</span><span class="sxs-lookup"><span data-stu-id="a9381-103">About Event Reference Pages</span></span>

<span data-ttu-id="a9381-104">Страница ссылки на события (ERP) — это HTML-документ, который предоставляет сетевой монитор сведения о событиях, обнаруженных во время работы эксперта или монитора.</span><span class="sxs-lookup"><span data-stu-id="a9381-104">An event reference page (ERP) is an HTML document that provides Network Monitor information about events detected during expert or monitor operation.</span></span>

<span data-ttu-id="a9381-105">ERP можно просмотреть в Просмотр событий сетевой монитор, средства управления монитора или в любом браузере, поддерживающем функции HTML Microsoft Internet Explorer 4,01 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a9381-105">You can view ERPs in the Event Viewer of Network Monitor, Monitor Control Tool, or in any browser that supports the HTML features of Microsoft Internet Explorer Version 4.01 or later.</span></span> <span data-ttu-id="a9381-106">Это значит, что в ERP можно добавить поддерживаемые элементы управления или скриптовые языки.</span><span class="sxs-lookup"><span data-stu-id="a9381-106">That is, you can add supported controls or scripted languages into your ERP.</span></span>

<span data-ttu-id="a9381-107">Однако ERP отображается только в том случае, если эксперт обозначает HTML-документ по имени.</span><span class="sxs-lookup"><span data-stu-id="a9381-107">However, ERPs appear only if the expert designates the HTML document by name.</span></span> <span data-ttu-id="a9381-108">При правильном обозначении ERP отображается в нижней области, когда выбрано событие в Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="a9381-108">When properly designated, the ERP appears in the lower pane when the event in the Event Viewer is selected.</span></span> <span data-ttu-id="a9381-109">На рисунке ниже показан ERP, связанный с монитором диапазона IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a9381-109">The figure below shows an ERP associated with the Internet Protocol (IP) Range monitor.</span></span>

![система ERP, связанная с монитором диапазона IP-адресов](images/exview2.png)

## <a name="expert-events"></a><span data-ttu-id="a9381-111">Мероприятия экспертов</span><span class="sxs-lookup"><span data-stu-id="a9381-111">Expert Events</span></span>

<span data-ttu-id="a9381-112">События экспертов определяются элементом **евентидент** структуры [**нмевентдата**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="a9381-112">Expert events are identified by the **EventIdent** member of an [**NMEVENTDATA**](nmeventdata.md) structure.</span></span> <span data-ttu-id="a9381-113">При написании эксперта вы определяете значения **евентидент** , которые обычно пронумерованы 1, 2, 3 и т. д.</span><span class="sxs-lookup"><span data-stu-id="a9381-113">When you write an expert you determine the **EventIdent** values, which are typically numbered 1, 2, 3, and so on.</span></span> <span data-ttu-id="a9381-114">Например, предположим, что эксперт создает два события (**EventIdent1** и **EventIdent2**).</span><span class="sxs-lookup"><span data-stu-id="a9381-114">For example, suppose that an expert generates two events (**EventIdent1** and **EventIdent2**).</span></span> <span data-ttu-id="a9381-115">Если требуется, чтобы Просмотр событий отображал события отдельно, необходимо создать два отдельных документа ERP.</span><span class="sxs-lookup"><span data-stu-id="a9381-115">If you want the Event Viewer to display the events separately, you must create two separate ERP documents.</span></span>

 

 



