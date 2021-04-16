---
description: Как подключаются фильтры
ms.assetid: 6a126dd5-00fa-4ea6-b00a-09b7e1246874
title: Как подключаются фильтры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a72b2540133e84e473e3e82896a6427b923319
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105650413"
---
# <a name="how-filters-connect"></a><span data-ttu-id="d5191-103">Как подключаются фильтры</span><span class="sxs-lookup"><span data-stu-id="d5191-103">How Filters Connect</span></span>

<span data-ttu-id="d5191-104">В этой статье описывается, как фильтры соединяются в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d5191-104">This article describes how filters connect in DirectShow.</span></span> <span data-ttu-id="d5191-105">Статья предназначена для разработчиков фильтров.</span><span class="sxs-lookup"><span data-stu-id="d5191-105">The article is intended for filter developers.</span></span> <span data-ttu-id="d5191-106">Если вы пишете приложение DirectShow, вы можете проигнорировать приведенные здесь сведения.</span><span class="sxs-lookup"><span data-stu-id="d5191-106">If you are writing a DirectShow application, you can probably ignore the details presented here.</span></span>

<span data-ttu-id="d5191-107">Эта статья содержит следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="d5191-107">This article contains the following topics:</span></span>

-   [<span data-ttu-id="d5191-108">Закрепление подключений</span><span class="sxs-lookup"><span data-stu-id="d5191-108">Pin Connections</span></span>](pin-connections.md)
-   [<span data-ttu-id="d5191-109">Согласование типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d5191-109">Negotiating Media Types</span></span>](negotiating-media-types.md)
-   [<span data-ttu-id="d5191-110">Согласование распределителя</span><span class="sxs-lookup"><span data-stu-id="d5191-110">Negotiating Allocators</span></span>](negotiating-allocators.md)
-   [<span data-ttu-id="d5191-111">Предоставление пользовательского распределителя</span><span class="sxs-lookup"><span data-stu-id="d5191-111">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
-   [<span data-ttu-id="d5191-112">Повторное подключение ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="d5191-112">Reconnecting Pins</span></span>](reconnecting-pins.md)

## <a name="related-topics"></a><span data-ttu-id="d5191-113">См. также</span><span class="sxs-lookup"><span data-stu-id="d5191-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5191-114">Процесс подключения Кбасепин</span><span class="sxs-lookup"><span data-stu-id="d5191-114">CBasePin Connection Process</span></span>](cbasepin-connection-process.md)
</dt> <dt>

[<span data-ttu-id="d5191-115">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5191-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



