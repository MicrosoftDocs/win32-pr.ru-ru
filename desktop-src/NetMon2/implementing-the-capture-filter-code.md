---
description: Определив способ организации фильтра с помощью структуры КАПТУРЕФИЛТЕР, необходимо выделить и заполнить структуру, которая затем передается драйверу сетевой монитор с помощью большого двоичного объекта конфигурации.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Реализация кода фильтра записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913859"
---
# <a name="implementing-the-capture-filter-code"></a><span data-ttu-id="b1776-103">Реализация кода фильтра записи</span><span class="sxs-lookup"><span data-stu-id="b1776-103">Implementing the Capture Filter Code</span></span>

<span data-ttu-id="b1776-104">Определив способ организации фильтра с помощью структуры [**каптурефилтер**](capturefilter.md) , необходимо выделить и заполнить структуру, которая затем передается драйверу сетевой монитор с помощью большого двоичного объекта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b1776-104">After you determine how to organize your filter through a [**CAPTUREFILTER**](capturefilter.md) structure, you must allocate and fill in the structure, which is then passed to the Network Monitor driver through a configuration BLOB.</span></span>

<span data-ttu-id="b1776-105">Прямые НПП пользователи добавляют фильтр записи в большой двоичный объект конфигурации, который передается для **подключения**, [**настройки**](configure.md)или обоих.</span><span class="sxs-lookup"><span data-stu-id="b1776-105">Direct NPP users add the capture filter to the configuration BLOB that is passed to **Connect**, [**Configure**](configure.md), or both.</span></span> <span data-ttu-id="b1776-106">Список COM-интерфейсов, которые можно использовать для взаимодействия с НПП, см. в разделе [интерфейсы НПП](npp-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b1776-106">For a list of COM interfaces that you can use to communicate with the NPP, see [NPP Interfaces](npp-interfaces.md).</span></span>

 

 



