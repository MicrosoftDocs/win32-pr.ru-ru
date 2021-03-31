---
title: Типы уведомлений
description: Типы уведомлений
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411223"
---
# <a name="types-of-notifications"></a><span data-ttu-id="882ef-103">Типы уведомлений</span><span class="sxs-lookup"><span data-stu-id="882ef-103">Types of Notifications</span></span>

<span data-ttu-id="882ef-104">Уведомления делятся на три группы: составной документ, данные и представление.</span><span class="sxs-lookup"><span data-stu-id="882ef-104">Notifications fall into three groups: compound document, data, and view.</span></span> <span data-ttu-id="882ef-105">Объект отправляет уведомления составного документа в ответ на переименование, сохранение, закрытие или, в случае ссылки, с переименованием источника ссылки.</span><span class="sxs-lookup"><span data-stu-id="882ef-105">An object sends compound document notifications in response to being renamed, saved, closed or, in the case of a link, having its link source renamed.</span></span> <span data-ttu-id="882ef-106">Как и предполагалось, объекты отправляют уведомления в ответ на изменения в своих данных и отправляют уведомления представления в ответ на изменения в их представлении.</span><span class="sxs-lookup"><span data-stu-id="882ef-106">As you would expect, objects send data notifications in response to changes in their data and send view notifications in response to changes in their presentation.</span></span> <span data-ttu-id="882ef-107">Приложения-контейнеры должны регистрироваться отдельно для каждого из этих типов уведомлений, но все могут обрабатываться одним приемником рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="882ef-107">Container applications must register separately for each of these notification types, but all can be handled by a single advisory sink.</span></span>

<span data-ttu-id="882ef-108">Все контейнеры, обработчики объектов и связанные объекты регистрируются для отправки уведомлений составного документа.</span><span class="sxs-lookup"><span data-stu-id="882ef-108">All containers, the object handler, and the linked object register for compound document notifications.</span></span> <span data-ttu-id="882ef-109">Стандартный контейнер также регистрируется для просмотра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="882ef-109">The typical container also registers for view notifications.</span></span> <span data-ttu-id="882ef-110">Уведомления об изменении данных обычно отправляются как в связанный объект, так и в обработчик объектов.</span><span class="sxs-lookup"><span data-stu-id="882ef-110">Data notifications are usually sent to both the linked object and object handler.</span></span> <span data-ttu-id="882ef-111">Специальный контейнер назначения, например, который визуализирует сами данные, может использовать преимущества получения уведомлений о данных вместо просмотра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="882ef-111">A special purpose container, such as one that renders the data itself, might benefit from receiving data notifications instead of view notifications.</span></span> <span data-ttu-id="882ef-112">Например, встроенный контейнер диаграммы со ссылкой на таблицу можно зарегистрировать для получения уведомлений об изменении данных.</span><span class="sxs-lookup"><span data-stu-id="882ef-112">For example, an embedded chart container with a link to a table can register for data notifications.</span></span> <span data-ttu-id="882ef-113">Так как изменение таблицы влияет на диаграмму, получение уведомления об изменении данных будет направлять контейнер для получения новых табличных данных.</span><span class="sxs-lookup"><span data-stu-id="882ef-113">Because a change to the table affects the chart, the receipt of a data notification would direct the container to get the new tabular data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="882ef-114">См. также</span><span class="sxs-lookup"><span data-stu-id="882ef-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="882ef-115">Уведомления</span><span class="sxs-lookup"><span data-stu-id="882ef-115">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 




