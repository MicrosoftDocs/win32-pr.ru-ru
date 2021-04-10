---
description: Использование Впуклосивент для уничтожения объекта события (приложения или поставщика услуг), когда объект события больше не требуется.
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: Уничтожение объектов событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f0a17f623d0dd9ebceaf76b963ce72306000b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343542"
---
# <a name="destroying-event-objects"></a><span data-ttu-id="2d49c-103">Уничтожение объектов событий</span><span class="sxs-lookup"><span data-stu-id="2d49c-103">Destroying Event Objects</span></span>

<span data-ttu-id="2d49c-104">Сущность, которая создает объект события (приложение или поставщик услуг), несет ответственность за его уничтожение, когда оно больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="2d49c-104">The entity that creates an event object (application or service provider) is responsible for destroying it when it is no longer required.</span></span> <span data-ttu-id="2d49c-105">Поставщики услуг выполняют это через **впуклосивент**.</span><span class="sxs-lookup"><span data-stu-id="2d49c-105">Service providers do this through **WPUCloseEvent**.</span></span>

 

 



