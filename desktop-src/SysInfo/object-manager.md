---
description: Объект состоит из стандартного заголовка и атрибутов, зависящих от объекта. Поскольку все объекты имеют одинаковую структуру, в Windows имеется один диспетчер объектов, поддерживающий все объекты.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Диспетчер объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999003"
---
# <a name="object-manager"></a><span data-ttu-id="cef02-104">Диспетчер объектов</span><span class="sxs-lookup"><span data-stu-id="cef02-104">Object Manager</span></span>

<span data-ttu-id="cef02-105">Объект состоит из стандартного заголовка и атрибутов, зависящих от объекта.</span><span class="sxs-lookup"><span data-stu-id="cef02-105">An object consists of a standard header and object-specific attributes.</span></span> <span data-ttu-id="cef02-106">Поскольку все объекты имеют одинаковую структуру, в Windows имеется один диспетчер объектов, поддерживающий все объекты.</span><span class="sxs-lookup"><span data-stu-id="cef02-106">Because all objects have the same structure, there is a single object manager in Windows that maintains all objects.</span></span>

<span data-ttu-id="cef02-107">Заголовок объекта включает такие элементы, как имя объекта, чтобы другие процессы могли ссылаться на объект по имени и дескриптор безопасности, чтобы диспетчер объектов мог контролировать, какие процессы обращаются к системному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="cef02-107">The object header includes items such as the object name, so that other processes can reference the object by name, and a security descriptor, so that the object manager can control which processes access the system resource.</span></span>

<span data-ttu-id="cef02-108">В число задач, выполняемых диспетчером объектов, входят следующие.</span><span class="sxs-lookup"><span data-stu-id="cef02-108">The tasks that the object manager performs include the following:</span></span>

-   <span data-ttu-id="cef02-109">Создание объектов</span><span class="sxs-lookup"><span data-stu-id="cef02-109">Creating objects</span></span>
-   <span data-ttu-id="cef02-110">Проверка того, что процесс имеет право использовать объект</span><span class="sxs-lookup"><span data-stu-id="cef02-110">Verifying that a process has the right to use the object</span></span>
-   <span data-ttu-id="cef02-111">Создание дескрипторов объектов и их возврат вызывающему объекту</span><span class="sxs-lookup"><span data-stu-id="cef02-111">Creating object handles and returning them to the caller</span></span>
-   <span data-ttu-id="cef02-112">Обслуживание квот ресурсов</span><span class="sxs-lookup"><span data-stu-id="cef02-112">Maintaining resource quotas</span></span>
-   <span data-ttu-id="cef02-113">Создание повторяющихся дескрипторов</span><span class="sxs-lookup"><span data-stu-id="cef02-113">Creating duplicate handles</span></span>
-   <span data-ttu-id="cef02-114">Закрытие дескрипторов объектов</span><span class="sxs-lookup"><span data-stu-id="cef02-114">Closing handles to objects</span></span>

 

 



