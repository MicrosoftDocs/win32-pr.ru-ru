---
title: Хранилища и потоки
description: Объект хранилища аналогичен каталогу файловой системы.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773889"
---
# <a name="storages-and-streams"></a><span data-ttu-id="f5bdd-103">Хранилища и потоки</span><span class="sxs-lookup"><span data-stu-id="f5bdd-103">Storages and Streams</span></span>

<span data-ttu-id="f5bdd-104">Объект хранилища аналогичен каталогу файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-104">A storage object is analogous to a file system directory.</span></span> <span data-ttu-id="f5bdd-105">Так же как каталог может содержать другие каталоги и файлы, объект хранилища может содержать другие объекты хранилища и объекты потока.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-105">Just as a directory can contain other directories and files, a storage object can contain other storage objects and stream objects.</span></span> <span data-ttu-id="f5bdd-106">Также как и в каталоге, объект хранилища отслеживает расположения и размеры объектов хранилища и объектов потоков, вложенных под него.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-106">Also like a directory, a storage object tracks the locations and sizes of the storage objects and stream objects nested beneath it.</span></span>

<span data-ttu-id="f5bdd-107">Объект потока является аналогом традиционного понятия файла.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-107">A stream object is analogous to the traditional notion of a file.</span></span> <span data-ttu-id="f5bdd-108">Как и файл, поток содержит данные, хранящиеся в виде последовательности байтов.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-108">Like a file, a stream contains data stored as a consecutive sequence of bytes.</span></span>

<span data-ttu-id="f5bdd-109">Составной файл COM состоит из объекта корневого хранилища, содержащего по крайней мере один объект потока, представляющий собственные данные, а также один или несколько объектов хранилища, соответствующих связанным и внедренным объектам.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-109">A COM compound file consists of a root storage object containing at least one stream object representing its native data along with one or more storage objects corresponding to its linked and embedded objects.</span></span> <span data-ttu-id="f5bdd-110">Корневой объект хранилища сопоставляется с именем файла в любой файловой системе, в которой он находится.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-110">The root storage object maps to a file name in whatever file system it happens to reside.</span></span> <span data-ttu-id="f5bdd-111">Каждый объект в документе также представляется объектом хранилища, содержащим один или несколько объектов потока, и, возможно, также содержит один или несколько объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-111">Each of the objects inside the document also is represented by a storage object containing one or more stream objects, and perhaps also containing one or more storage objects.</span></span> <span data-ttu-id="f5bdd-112">Таким образом, документ может состоять из неограниченного числа вложенных объектов.</span><span class="sxs-lookup"><span data-stu-id="f5bdd-112">In this way, a document can consist of an unlimited number of nested objects.</span></span> <span data-ttu-id="f5bdd-113">Дополнительные сведения см. в разделе [Составные файлы](compound-files.md).</span><span class="sxs-lookup"><span data-stu-id="f5bdd-113">For more information, see [Compound Files](compound-files.md).</span></span>

 

 




