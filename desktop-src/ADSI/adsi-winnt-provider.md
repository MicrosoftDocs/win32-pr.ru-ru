---
title: Поставщик ADSI WinNT
description: Поставщик Microsoft ADSI реализует набор объектов ADSI для поддержки различных интерфейсов ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI поставщика ADSI provider
- Служба WinNT Service Provider ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410607"
---
# <a name="adsi-winnt-provider"></a><span data-ttu-id="9b0ee-105">Поставщик ADSI WinNT</span><span class="sxs-lookup"><span data-stu-id="9b0ee-105">ADSI WinNT Provider</span></span>

<span data-ttu-id="9b0ee-106">Поставщик Microsoft ADSI реализует набор объектов ADSI для поддержки различных интерфейсов ADSI.</span><span class="sxs-lookup"><span data-stu-id="9b0ee-106">The Microsoft ADSI provider implements a set of ADSI objects to support various ADSI interfaces.</span></span> <span data-ttu-id="9b0ee-107">Имя пространства имен для поставщика Windows — "WinNT", а этот поставщик обычно называется поставщиком WinNT.</span><span class="sxs-lookup"><span data-stu-id="9b0ee-107">The namespace name for the Windows provider is "WinNT" and this provider is commonly referred to as the WinNT provider.</span></span> <span data-ttu-id="9b0ee-108">Чтобы получить доступ к поставщику WinNT, выполните привязку к любому из [объектов ADSI в Winnt](adsi-objects-of-winnt.md), используя файл [WinNT AdsPath](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="9b0ee-108">To access the WinNT provider, bind to any of the [ADSI objects of WinNT](adsi-objects-of-winnt.md), using the [WinNT AdsPath](winnt-adspath.md).</span></span>

<span data-ttu-id="9b0ee-109">Поставщик WinNT включен в системный компонент ADSI для Windows и Windows Server.</span><span class="sxs-lookup"><span data-stu-id="9b0ee-109">The WinNT provider is included in the ADSI system component for Windows and Windows Server.</span></span>

> [!Note]  
> <span data-ttu-id="9b0ee-110">Поставщик WinNT по умолчанию не может считаться полностью потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="9b0ee-110">The default WinNT provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="9b0ee-111">Средства записи многопоточных приложений должны обеспечивать обработку многопоточности для правильной координации любого доступа между потоками с помощью надлежащего использования объектов синхронизации, таких как семафоры, мьютексы, критические разделы и т. д.</span><span class="sxs-lookup"><span data-stu-id="9b0ee-111">Writers of multithreaded applications should handle multithreading to properly coordinate any access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




