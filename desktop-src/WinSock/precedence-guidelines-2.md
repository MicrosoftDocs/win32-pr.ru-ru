---
description: Два (или более) дескрипторов, которые ссылаются на общий сокет, могут использоваться независимо, когда речь идет о вводе-выводе.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Правила приоритета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144983"
---
# <a name="precedence-guidelines"></a><span data-ttu-id="786d8-103">Правила приоритета</span><span class="sxs-lookup"><span data-stu-id="786d8-103">Precedence Guidelines</span></span>

<span data-ttu-id="786d8-104">Два (или более) дескрипторов, которые ссылаются на общий сокет, могут использоваться независимо, когда речь идет о вводе-выводе.</span><span class="sxs-lookup"><span data-stu-id="786d8-104">The two (or more) descriptors that reference a shared socket may be used independently as far as I/O is concerned.</span></span> <span data-ttu-id="786d8-105">Однако интерфейс сокетов Windows не реализует какой-либо тип контроля доступа, поэтому он предназначен для координации операций на общем сокете.</span><span class="sxs-lookup"><span data-stu-id="786d8-105">However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket.</span></span> <span data-ttu-id="786d8-106">Обычно для общих сокетов используется один процесс, отвечающий за создание сокетов и установление соединения, а не сокеты для других процессов, ответственных за обмен данными.</span><span class="sxs-lookup"><span data-stu-id="786d8-106">A typical use for shared sockets is to have one process that is responsible for creating sockets and establishing connections hand off sockets to other processes that are responsible for information exchange.</span></span>

<span data-ttu-id="786d8-107">Общая рекомендация по поддержке нескольких необработанных операций на общих сокетах заключается в том, что поставщик услуг должен учитывать все одновременные операции на общих сокетах, особенно самая последняя операция с объектом сокета.</span><span class="sxs-lookup"><span data-stu-id="786d8-107">The general guideline for supporting multiple outstanding operations on shared sockets is that a service provider is encouraged to honor all simultaneous operations on shared sockets, especially the most recent operation on a socket object.</span></span> <span data-ttu-id="786d8-108">При необходимости это может произойти за счет отмены некоторых из предыдущих, но еще ожидающих операций, которые будут возвращать ВСАЕИНТР в этом случае.</span><span class="sxs-lookup"><span data-stu-id="786d8-108">If need be, this may occur at the expense of canceling some of the previous but still pending operations, which will return WSAEINTR in this case.</span></span>

 

 



