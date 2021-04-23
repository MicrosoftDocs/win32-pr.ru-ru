---
title: Обработчик по умолчанию и пользовательские обработчики
description: Обработчик по умолчанию и пользовательские обработчики
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986299"
---
# <a name="the-default-handler-and-custom-handlers"></a><span data-ttu-id="248e9-103">Обработчик по умолчанию и пользовательские обработчики</span><span class="sxs-lookup"><span data-stu-id="248e9-103">The Default Handler and Custom Handlers</span></span>

<span data-ttu-id="248e9-104">Обработчик по умолчанию, реализация, предоставляемый OLE, используется большинством приложений в качестве обработчика.</span><span class="sxs-lookup"><span data-stu-id="248e9-104">The default handler, an implementation provided by OLE, is used by most applications as the handler.</span></span> <span data-ttu-id="248e9-105">Приложение реализует пользовательский обработчик, когда возможности обработчика по умолчанию недостаточны.</span><span class="sxs-lookup"><span data-stu-id="248e9-105">An application implements a custom handler when the default handler's capabilities are insufficient.</span></span> <span data-ttu-id="248e9-106">Пользовательский обработчик может либо полностью заменить обработчик по умолчанию, либо использовать части предоставляемых им функций, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="248e9-106">A custom handler can either completely replace the default handler or use parts of the functionality it provides where appropriate.</span></span> <span data-ttu-id="248e9-107">В последнем случае обработчик приложения реализуется как агрегатный объект, состоящий из нового управляющего объекта и обработчика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="248e9-107">In the latter case, the application handler is implemented as an aggregate object composed of a new control object and the default handler.</span></span> <span data-ttu-id="248e9-108">Сочетания приложений и обработчиков по умолчанию также называются *внутрипроцессный обработчиками*.</span><span class="sxs-lookup"><span data-stu-id="248e9-108">Combination application/default handlers are also known as *in-process handlers*.</span></span> <span data-ttu-id="248e9-109">*Обработчик удаленного взаимодействия* используется для объектов, которым не назначен CLSID в системном реестре или которые не имеют указанного обработчика.</span><span class="sxs-lookup"><span data-stu-id="248e9-109">The *remoting handler* is used for objects that are not assigned a CLSID in the system registry or that have no specified handler.</span></span> <span data-ttu-id="248e9-110">Все, что требуется из обработчика для этих типов объектов, заключается в том, что они передают информацию через границу процесса.</span><span class="sxs-lookup"><span data-stu-id="248e9-110">All that is required from a handler for these types of objects is that they pass information across the process boundary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="248e9-111">См. также</span><span class="sxs-lookup"><span data-stu-id="248e9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="248e9-112">Обработчики объектов</span><span class="sxs-lookup"><span data-stu-id="248e9-112">Object Handlers</span></span>](object-handlers.md)
</dt> </dl>

 

 




