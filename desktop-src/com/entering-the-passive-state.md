---
title: Вход в пассивное состояние
description: Вход в пассивное состояние
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889016"
---
# <a name="entering-the-passive-state"></a><span data-ttu-id="b8f7e-103">Вход в пассивное состояние</span><span class="sxs-lookup"><span data-stu-id="b8f7e-103">Entering the Passive State</span></span>

<span data-ttu-id="b8f7e-104">Закрытие объекта принудительно принуждает внедренный или связанный объект в пассивное состояние.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-104">Object closure forces an embedded or linked object into the passive state.</span></span> <span data-ttu-id="b8f7e-105">Обычно она инициируется из пользовательского интерфейса приложения OLE-сервера, например, когда пользователь выбирает команду Закрыть файл.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-105">It is typically initiated from the OLE server application's user interface, such as when the user selects the File Close command.</span></span> <span data-ttu-id="b8f7e-106">В этом случае серверное приложение OLE уведомляет контейнер, который освобождает его счетчик ссылок на объект.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-106">In this case, the OLE server application notifies the container, which releases its reference count on the object.</span></span> <span data-ttu-id="b8f7e-107">Когда все ссылки на объект были освобождены, объект можно освободить.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-107">When all references to the object have been released, the object can be freed.</span></span> <span data-ttu-id="b8f7e-108">Когда все объекты были освобождены, приложение OLE Server может безопасно завершить работу.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-108">When all objects have been freed, the OLE server application can safely terminate.</span></span>

<span data-ttu-id="b8f7e-109">Приложение-контейнер также может инициировать закрытие объекта.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-109">A container application can also initiate object closure.</span></span> <span data-ttu-id="b8f7e-110">Чтобы закрыть объект, контейнер освобождает его счетчик ссылок после выполнения необязательной операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-110">To close an object, the container releases its reference count after completing an optional save operation.</span></span> <span data-ttu-id="b8f7e-111">Можно создавать контейнеры, чтобы освободить объекты, когда они деактивируются после сеанса активации на месте, позволяя пользователю щелкнуть за пределами объекта без потери активного сеанса редактирования.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-111">You can design containers to release objects when they are deactivating after an in-place activation session, allowing the user to click outside the object without losing the active editing session.</span></span>

 

 




