---
description: Автоматическое освобождение ресурсов
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Автоматическое освобождение ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342292"
---
# <a name="automatic-resource-reclamation"></a><span data-ttu-id="808c8-103">Автоматическое освобождение ресурсов</span><span class="sxs-lookup"><span data-stu-id="808c8-103">Automatic Resource Reclamation</span></span>

<span data-ttu-id="808c8-104">COM+ Уведомляет диспетчер распределителя каждый раз, когда заканчивается время существования объекта.</span><span class="sxs-lookup"><span data-stu-id="808c8-104">COM+ notifies the dispenser manager each time an object's lifetime ends.</span></span> <span data-ttu-id="808c8-105">Затем Диспетчер распределителя уведомляет каждый зарегистрированный держатель ресурса, чтобы узнать, есть ли у него ресурсы, удерживаемые этим объектом.</span><span class="sxs-lookup"><span data-stu-id="808c8-105">The dispenser manager then notifies each registered resource dispenser's Holder to see whether it has any resources still held by this object.</span></span> <span data-ttu-id="808c8-106">Если это так, эти ресурсы освобождаются, предотвращая вероятность утечки ресурсов компонентами, которые получают ресурсы через распределитель ресурсов.</span><span class="sxs-lookup"><span data-stu-id="808c8-106">If so, those resources are freed, preventing the possibility of resource leaks by components that get resources through a resource dispenser.</span></span>

<span data-ttu-id="808c8-107">Функция автоматического восстановления является параметром, который по умолчанию отключен.</span><span class="sxs-lookup"><span data-stu-id="808c8-107">The auto-reclamation feature is an option that is turned off by default.</span></span> <span data-ttu-id="808c8-108">Распределитель ресурсов может включить этот параметр, и при этом гарантирует, что ссылка на любой ресурс, который был передан объекту, никогда не будет возвращаться методами объекта.</span><span class="sxs-lookup"><span data-stu-id="808c8-108">A resource dispenser can choose to enable this option and, in doing so, guarantees that a reference to any resource dispensed to an object is never returned by the object methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="808c8-109">См. также</span><span class="sxs-lookup"><span data-stu-id="808c8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="808c8-110">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="808c8-110">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



