---
description: При использовании интерфейса для получения изображений Windows (WIA) в нескольких потоках в рамках одного процесса приложение должно обеспечивать маршалинг для этого интерфейса.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Использование нескольких потоков в приложении WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145361"
---
# <a name="using-multiple-threads-in-a-wia-application"></a><span data-ttu-id="e0a97-103">Использование нескольких потоков в приложении WIA</span><span class="sxs-lookup"><span data-stu-id="e0a97-103">Using Multiple Threads in a WIA Application</span></span>

<span data-ttu-id="e0a97-104">При использовании интерфейса для получения изображений Windows (WIA) в нескольких потоках в рамках одного процесса приложение должно обеспечивать маршалинг для этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e0a97-104">When using a Windows Image Acquisition (WIA) interface in more than one thread within a single process, an application must provide marshalling for that interface.</span></span> <span data-ttu-id="e0a97-105">Если один поток создает указатель интерфейса, нельзя использовать этот указатель в другом потоке без маршалирования.</span><span class="sxs-lookup"><span data-stu-id="e0a97-105">If one thread creates an interface pointer, you cannot use that pointer in a different thread without marshalling.</span></span>

<span data-ttu-id="e0a97-106">Например, если один поток в приложении получает указатель на интерфейс [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) , отдельный поток не может использовать этот указатель интерфейса без маршалирования.</span><span class="sxs-lookup"><span data-stu-id="e0a97-106">For example, if one thread in an application obtains a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface, a separate thread cannot use that interface pointer without marshalling.</span></span>

<span data-ttu-id="e0a97-107">Распространенной методикой, используемой для выполнения этого маршалинга, является использование глобальной таблицы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e0a97-107">A common technique used to accomplish this marshalling is to use the global interface table.</span></span> <span data-ttu-id="e0a97-108">Глобальная таблица интерфейса — это таблица, которая сохраняется во всех потоках в рамках одного процесса.</span><span class="sxs-lookup"><span data-stu-id="e0a97-108">The global interface table is a table maintained across all threads within a single process.</span></span> <span data-ttu-id="e0a97-109">Все потоки, выполняющиеся в процессе, могут извлекать интерфейсы, зарегистрированные в глобальной таблице интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e0a97-109">All threads running within the process can retrieve interfaces that are registered to the global interface table.</span></span> <span data-ttu-id="e0a97-110">Этот метод позволяет избежать необходимости создавать потоки для передачи интерфейсов между потоками.</span><span class="sxs-lookup"><span data-stu-id="e0a97-110">This technique avoids the need to create streams for passing interfaces between threads.</span></span>

<span data-ttu-id="e0a97-111">Сведения об использовании глобальной таблицы интерфейса см. в разделе [иглобалинтерфацетабле](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="e0a97-111">For information on how to use the global interface table, see [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="e0a97-112">Даже если вы не планируете использовать несколько потоков в приложении WIA, необходимо предположить, что все функции обмена данными или обратного вызова событий устройства выполняются в отдельных потоках.</span><span class="sxs-lookup"><span data-stu-id="e0a97-112">Even if you do not intend to use multiple threads in a WIA application, you must assume that all data transfer or device event callback functions run in separate threads.</span></span>

 

 
