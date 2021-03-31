---
description: Запрос возможностей поиска
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Запрос возможностей поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894922"
---
# <a name="querying-for-seeking-capabilities"></a><span data-ttu-id="06707-103">Запрос возможностей поиска</span><span class="sxs-lookup"><span data-stu-id="06707-103">Querying for Seeking Capabilities</span></span>

<span data-ttu-id="06707-104">Microsoft® DirectShow® поддерживает поиск через интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="06707-104">Microsoft® DirectShow® supports seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="06707-105">Диспетчер графов фильтров предоставляет этот интерфейс, но функции поиска всегда реализуются фильтрами в графе.</span><span class="sxs-lookup"><span data-stu-id="06707-105">The Filter Graph Manager exposes this interface, but the seeking functionality is always implemented by filters in the graph.</span></span>

<span data-ttu-id="06707-106">Не удается выполнить поиск некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="06707-106">Some data cannot be seeked.</span></span> <span data-ttu-id="06707-107">Например, невозможно выполнить поиск потока видео с камеры.</span><span class="sxs-lookup"><span data-stu-id="06707-107">For example, you cannot seek a live video stream from a camera.</span></span> <span data-ttu-id="06707-108">Однако если поток доступен для поиска, он может поддерживать различные типы поиска.</span><span class="sxs-lookup"><span data-stu-id="06707-108">If a stream is seekable, however, there are various types of seeking it might support.</span></span> <span data-ttu-id="06707-109">Сюда входит следующее.</span><span class="sxs-lookup"><span data-stu-id="06707-109">These include:</span></span>

-   <span data-ttu-id="06707-110">Поиск произвольной позицией в потоке.</span><span class="sxs-lookup"><span data-stu-id="06707-110">Seeking to an arbitrary position in the stream.</span></span>
-   <span data-ttu-id="06707-111">Получение длительности потока.</span><span class="sxs-lookup"><span data-stu-id="06707-111">Retrieving the duration of the stream.</span></span>
-   <span data-ttu-id="06707-112">Получение текущей позицией в потоке.</span><span class="sxs-lookup"><span data-stu-id="06707-112">Retrieving the current position within the stream.</span></span>
-   <span data-ttu-id="06707-113">Воспроизведение в обратную.</span><span class="sxs-lookup"><span data-stu-id="06707-113">Playing in reverse.</span></span>

<span data-ttu-id="06707-114">Интерфейс **имедиасикинг** определяет набор флагов, которые [**\_ ищут \_ \_ возможности поиска**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), которые описывают возможные возможности поиска.</span><span class="sxs-lookup"><span data-stu-id="06707-114">The **IMediaSeeking** interface defines a set of flags, [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), that describe the possible seeking capabilities.</span></span> <span data-ttu-id="06707-115">Чтобы получить возможности потока, вызовите метод [**имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="06707-115">To retrieve the stream's capabilities, call the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="06707-116">Метод возвращает побитовое сочетание флагов.</span><span class="sxs-lookup"><span data-stu-id="06707-116">The method returns a bitwise combination of flags.</span></span> <span data-ttu-id="06707-117">Приложение может проверить их с помощью оператора & (побитовое **и**).</span><span class="sxs-lookup"><span data-stu-id="06707-117">The application can test them using the & (bitwise **AND**) operator.</span></span> <span data-ttu-id="06707-118">Например, следующий код проверяет, может ли граф перейти к произвольной должности:</span><span class="sxs-lookup"><span data-stu-id="06707-118">For example, the following code checks whether the graph can seek to an arbitrary position:</span></span>


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



