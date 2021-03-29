---
title: Вход в загруженное состояние
description: Вход в загруженное состояние
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774978"
---
# <a name="entering-the-loaded-state"></a><span data-ttu-id="d3d63-103">Вход в загруженное состояние</span><span class="sxs-lookup"><span data-stu-id="d3d63-103">Entering the Loaded State</span></span>

<span data-ttu-id="d3d63-104">Когда объект входит в загруженное состояние, создаются структуры в памяти, представляющие объект, чтобы можно было вызывать операции с ним.</span><span class="sxs-lookup"><span data-stu-id="d3d63-104">When an object enters the loaded state, the in-memory structures representing the object are created so that operations can be invoked on it.</span></span> <span data-ttu-id="d3d63-105">Загружается обработчик объекта или внутрипроцессный сервер.</span><span class="sxs-lookup"><span data-stu-id="d3d63-105">The object's handler or in-process server is loaded.</span></span> <span data-ttu-id="d3d63-106">Этот процесс, называемый *созданием экземпляра*, возникает, когда объект загружается из постоянного хранилища (переход от пассивного состояния к загруженному) или когда объект создается в первый раз.</span><span class="sxs-lookup"><span data-stu-id="d3d63-106">This process, referred to as *instantiation*, occurs when an object is loaded from persistent storage (a transition from the passive to the loaded state) or when an object is being created for the first time.</span></span>

<span data-ttu-id="d3d63-107">На внутреннем уровне создание экземпляра — двухэтапный процесс.</span><span class="sxs-lookup"><span data-stu-id="d3d63-107">Internally, instantiation is a two-phase process.</span></span> <span data-ttu-id="d3d63-108">Создается объект соответствующего класса, после которого вызывается метод этого объекта для выполнения инициализации и предоставления доступа к данным этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d3d63-108">An object of the appropriate class is created, after which a method on that object is called to perform initialization and give access to the object's data.</span></span> <span data-ttu-id="d3d63-109">Метод инициализации определен в одном из поддерживаемых интерфейсов объекта.</span><span class="sxs-lookup"><span data-stu-id="d3d63-109">The initialization method is defined in one of the object's supported interfaces.</span></span> <span data-ttu-id="d3d63-110">Определенный метод инициализации зависит от контекста, в котором создается экземпляр объекта, и расположения данных инициализации.</span><span class="sxs-lookup"><span data-stu-id="d3d63-110">The particular initialization method called depends on the context in which the object is being instantiated and the location of the initialization data.</span></span>

 

 




