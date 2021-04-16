---
description: Существует еще один класс асинхронных событий, помимо описанных выше.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Асинхронное безсобытие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683802"
---
# <a name="asynchronous-spontaneous-events"></a><span data-ttu-id="00a92-103">Асинхронное безсобытие</span><span class="sxs-lookup"><span data-stu-id="00a92-103">Asynchronous Spontaneous Events</span></span>

<span data-ttu-id="00a92-104">Существует еще один класс асинхронных событий, помимо описанных выше.</span><span class="sxs-lookup"><span data-stu-id="00a92-104">There is another class of asynchronous events besides those described above.</span></span> <span data-ttu-id="00a92-105">Эти события «недоступны» в том смысле, что они не являются прямыми результатами соответствующих запросов.</span><span class="sxs-lookup"><span data-stu-id="00a92-105">These events are "spontaneous" in the sense that they are not direct results of corresponding requests.</span></span> <span data-ttu-id="00a92-106">Эти события обнаруживаются в таких случаях, как при поступлении входящего вызова, или когда исходящий вызов поступает из "звонка" в состояние "ответ".</span><span class="sxs-lookup"><span data-stu-id="00a92-106">These events are detected in such cases as when an incoming call arrives, or when an outbound call goes from a "ringing" to an "answering" state.</span></span> <span data-ttu-id="00a92-107">Когда TAPI сначала инициализирует взаимодействия с ТСПИ для конкретного устройства, он передает указатель на процедуру обратного вызова, которая вызывается для создания отчетов о таких событиях.</span><span class="sxs-lookup"><span data-stu-id="00a92-107">When TAPI first initializes interactions with the TSPI for a particular device, it passes a pointer to a callback procedure to be called for reporting such spontaneous events.</span></span> <span data-ttu-id="00a92-108">Кроме того, этот указатель процедуры является обработчиком устройства, который поставщик услуг включает в качестве одного из фактических параметров обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="00a92-108">Along with this procedure pointer is a device handle that the service provider includes as one of the actual parameters to the callback.</span></span>

 

 



