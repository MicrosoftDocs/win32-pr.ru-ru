---
title: Создание и оптимизация GUID
description: Создание и оптимизация GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411347"
---
# <a name="guid-creation-and-optimizations"></a><span data-ttu-id="b7978-103">Создание и оптимизация GUID</span><span class="sxs-lookup"><span data-stu-id="b7978-103">GUID Creation and Optimizations</span></span>

<span data-ttu-id="b7978-104">Поскольку CLSID, например идентификатор интерфейса (IID), является идентификатором GUID, никакой другой класс, независимо от его записи, имеет дублирующийся идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="b7978-104">Because a CLSID, like an interface identifier (IID), is a GUID, no other class, no matter who writes it, has a duplicate CLSID.</span></span> <span data-ttu-id="b7978-105">Разработчики серверов обычно получают идентификаторы CLSID через функцию [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .</span><span class="sxs-lookup"><span data-stu-id="b7978-105">Server implementers generally obtain CLSIDs through the [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) function.</span></span> <span data-ttu-id="b7978-106">Эта функция гарантированно создает уникальные идентификаторы CLSID, поэтому разработчики серверов в мире могут независимо разрабатывать и развертывать их программное обеспечение, не опасаясь случайного конфликта с программным обеспечением, написанным другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="b7978-106">This function is guaranteed to produce unique CLSIDs, so server implementers across the world can independently develop and deploy their software without fear of accidental collision with software written by others.</span></span>

<span data-ttu-id="b7978-107">Использование уникальных идентификаторов CLSID позволяет избежать конфликтов имен между классами, так как CLSID не подключены к именам, используемым в базовой реализации.</span><span class="sxs-lookup"><span data-stu-id="b7978-107">Using unique CLSIDs avoids the possibility of name collisions among classes because CLSIDs are in no way connected to the names used in the underlying implementation.</span></span> <span data-ttu-id="b7978-108">Например, два разных поставщика могут писать классы с именем "Стакккласс", но каждый из них будет иметь уникальный идентификатор CLSID, поэтому их не следует путать.</span><span class="sxs-lookup"><span data-stu-id="b7978-108">For example, two different vendors can write classes called "StackClass," but each would have a unique CLSID and therefore could not be confused.</span></span>

<span data-ttu-id="b7978-109">COM часто должен сопоставлять идентификаторы GUID (идентификаторов IID и CLSID) с произвольным большим набором других значений.</span><span class="sxs-lookup"><span data-stu-id="b7978-109">COM frequently must map GUIDs (IIDs and CLSIDs) to some arbitrarily large set of other values.</span></span> <span data-ttu-id="b7978-110">Как разработчик приложения вы можете ускорить такой поиск и, таким образом, повысить производительность системы, создав идентификаторы GUID для приложения в виде блока последовательных значений.</span><span class="sxs-lookup"><span data-stu-id="b7978-110">As an application developer, you can help speed up such searches, and thereby enhance system performance, by generating the GUIDs for your application as a block of consecutive values.</span></span>

<span data-ttu-id="b7978-111">Наиболее эффективный способ создания блока последовательных идентификаторов GUID — запуск служебной программы uuidgen с параметрами-n и-x, которая создает блок UUID, каждый из которых имеет первое значение DWORD, увеличенное на единицу.</span><span class="sxs-lookup"><span data-stu-id="b7978-111">The most efficient way to generate a block of consecutive GUIDs is to run the uuidgen utility using the -n and -x switches, which generates a block of UUIDs, each of whose first DWORD value is incremented by one.</span></span>

<span data-ttu-id="b7978-112">Например, если необходимо ввести</span><span class="sxs-lookup"><span data-stu-id="b7978-112">For example, if you were to type</span></span>

<span data-ttu-id="b7978-113">**uuidgen-N5-x**</span><span class="sxs-lookup"><span data-stu-id="b7978-113">**uuidgen -n5 -x**</span></span>

<span data-ttu-id="b7978-114">Служебная программа Uuidgen создаст блок UUID, аналогичный приведенному ниже:</span><span class="sxs-lookup"><span data-stu-id="b7978-114">the uuidgen utility would generate a block of UUIDs similar to the following:</span></span>

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

<span data-ttu-id="b7978-115">Один из методов создания и отслеживания идентификаторов GUID для всего проекта начинается с создания блока некоторого произвольного большого количества UUID, скажем 500.</span><span class="sxs-lookup"><span data-stu-id="b7978-115">One method for generating and tracking GUIDs for an entire project begins with generating a block of some arbitrarily large number of UUIDs, say 500.</span></span> <span data-ttu-id="b7978-116">Например, если необходимо ввести</span><span class="sxs-lookup"><span data-stu-id="b7978-116">For example, if you were to type</span></span>

<span data-ttu-id="b7978-117">**uuidgen-N500-x > guids.txt**</span><span class="sxs-lookup"><span data-stu-id="b7978-117">**uuidgen -n500 -x > guids.txt**</span></span>

<span data-ttu-id="b7978-118">Программа создаст 500 последовательных UUID и запишет их в указанный текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="b7978-118">the utility would generate 500 consecutive UUIDs and write them to the specified text file.</span></span> <span data-ttu-id="b7978-119">Затем этот файл можно вернуть в исходное дерево, предоставив единый репозиторий для всех идентификаторов GUID, которые будут использоваться в проекте.</span><span class="sxs-lookup"><span data-stu-id="b7978-119">You could then check this file into your source tree, providing a single repository for all GUIDs to be used in a project.</span></span> <span data-ttu-id="b7978-120">Так как пользователям требуются идентификаторы GUID для своих частей проекта, они могут извлечь файл, получить необходимое количество идентификаторов GUID, пометить их как выполненные и отказаться от заметок о том, где в коде или «Spec» они их используют.</span><span class="sxs-lookup"><span data-stu-id="b7978-120">As people require GUIDs for their portions of the project, they can check out the file, take however many GUIDs they need, marking them as taken and leaving a note about where in the code or "spec" they are using them.</span></span>

<span data-ttu-id="b7978-121">Помимо повышения производительности системы, создание блоков последовательных идентификаторов GUID таким образом имеет следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="b7978-121">In addition to improving system performance, generating blocks of consecutive GUIDs in this way has the following benefits:</span></span>

-   <span data-ttu-id="b7978-122">Центральный файл, содержащий все идентификаторы GUID для приложения, позволяет легко отследить, какие идентификаторы GUID предназначены для того, что и какие пользователи используют.</span><span class="sxs-lookup"><span data-stu-id="b7978-122">A central file containing all GUIDs for an application makes it easy to keep track of which GUIDs are for what and which people are using them.</span></span>
-   <span data-ttu-id="b7978-123">Блок последовательных идентификаторов GUID, связанных с конкретным приложением, помогает разработчикам и тестерам распознать внутренние идентификаторы GUID во время отладки и упрощает их поиск в системном реестре, поскольку они хранятся последовательно.</span><span class="sxs-lookup"><span data-stu-id="b7978-123">A block of consecutive GUIDs associated with a particular application helps developers and testers recognize internal GUIDs during debugging and makes it easier to find them in the system registry because they are stored sequentially.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7978-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b7978-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7978-125">Обязанности сервера COM</span><span class="sxs-lookup"><span data-stu-id="b7978-125">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 




