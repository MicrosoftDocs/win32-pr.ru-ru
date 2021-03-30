---
title: Зачем нужны прокси-объекты
description: При наличии доступных объектов, когда клиент устанавливает функцию-обработчик в контексте, Библиотека DLL, в которой реализована функция-ловушка клиента, загружается в адресное пространство сервера.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329915"
---
# <a name="why-proxy-objects-are-needed"></a><span data-ttu-id="03574-103">Зачем нужны прокси-объекты</span><span class="sxs-lookup"><span data-stu-id="03574-103">Why Proxy Objects Are Needed</span></span>

<span data-ttu-id="03574-104">При наличии доступных объектов, когда клиент устанавливает [функцию-обработчик в контексте](in-context-and-out-of-context-hook-functions.md), Библиотека DLL, в которой реализована функция-ловушка клиента, загружается в адресное пространство сервера.</span><span class="sxs-lookup"><span data-stu-id="03574-104">With accessible objects, when a client sets an [in-context hook function](in-context-and-out-of-context-hook-functions.md), the DLL in which the client's hook function is implemented is loaded into the server's address space.</span></span> <span data-ttu-id="03574-105">В этом случае, когда клиент вызывает [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) из функции-ловушки, указатель интерфейса, который возвращается, указывает непосредственно на код в адресном пространстве сервера.</span><span class="sxs-lookup"><span data-stu-id="03574-105">In this case, when the client calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) from within the hook function, the interface pointer that is returned points directly to code in the server's address space.</span></span> <span data-ttu-id="03574-106">Когда клиент вызывает свойство интерфейса с помощью этого указателя, Библиотека COM не участвует в упаковке или распаковке и не может обнаружить уничтожение объекта.</span><span class="sxs-lookup"><span data-stu-id="03574-106">When the client calls an interface property using this pointer, the Component Object Model (COM) library is not involved with marshaling or unmarshaling and cannot detect if an object is destroyed.</span></span> <span data-ttu-id="03574-107">Поэтому сервер должен обнаружить эту ситуацию и вернуть клиенту код ошибки.</span><span class="sxs-lookup"><span data-stu-id="03574-107">Therefore, the server must detect this situation and return an error code to the client.</span></span>

 

 




