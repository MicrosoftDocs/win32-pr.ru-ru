---
title: Временная локализация
description: Временная Локализация — это стратегия предотвращения, которая сокращает окно для частичных обновлений.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486580"
---
# <a name="temporal-locality"></a><span data-ttu-id="ab9e4-103">Временная локализация</span><span class="sxs-lookup"><span data-stu-id="ab9e4-103">Temporal Locality</span></span>

<span data-ttu-id="ab9e4-104">*Временная локализация* — это стратегия предотвращения, которая сокращает окно для частичных обновлений.</span><span class="sxs-lookup"><span data-stu-id="ab9e4-104">*Temporal locality* is an avoidance strategy that reduces the window for partial updates.</span></span> <span data-ttu-id="ab9e4-105">Репликация изменений из заданной исходной реплики продолжается в порядке возрастания USN.</span><span class="sxs-lookup"><span data-stu-id="ab9e4-105">Replication of changes from a given source replica proceeds in ascending USN order.</span></span> <span data-ttu-id="ab9e4-106">Операции записи, которые происходят близко друг к другу, будут иметь USN, которые находятся рядом друг с другом и будут распространяться близко друг к другу вовремя.</span><span class="sxs-lookup"><span data-stu-id="ab9e4-106">Writes that occur close together in time will have USNs that are "near" each other, and will be propagated close together in time.</span></span> <span data-ttu-id="ab9e4-107">Приложения, которые создают или обновляют несколько связанных объектов, должны заставлять объекты как можно ближе друг к другу во времени.</span><span class="sxs-lookup"><span data-stu-id="ab9e4-107">Applications that create or update multiple, related objects should write the objects as close together in time as possible.</span></span> <span data-ttu-id="ab9e4-108">Например, приложение может собрать все необходимые данные от пользователя и применить его к каталогу, когда пользователь нажмет кнопку "Применить".</span><span class="sxs-lookup"><span data-stu-id="ab9e4-108">For example, the application could gather all necessary input from the user and apply it to the directory when the user clicks an "Apply" button.</span></span>

<span data-ttu-id="ab9e4-109">Временная локализация также сокращает вероятность конфликта, что приводит к несогласованности внутри объекта.</span><span class="sxs-lookup"><span data-stu-id="ab9e4-109">Temporal locality also reduces the odds of collision resolution introducing intra-object inconsistencies.</span></span>

 

 




