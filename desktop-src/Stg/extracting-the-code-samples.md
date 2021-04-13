---
title: Извлечение примеров кода
description: Хотя примеры кода делятся на ряд учебных занятий, соответствующие примеры группирования можно легко извлечь из коллекции.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410817"
---
# <a name="extracting-the-code-samples"></a><span data-ttu-id="6f29b-103">Извлечение примеров кода</span><span class="sxs-lookup"><span data-stu-id="6f29b-103">Extracting the Code Samples</span></span>

<span data-ttu-id="6f29b-104">Хотя примеры кода делятся на ряд учебных занятий, соответствующие примеры группирования можно легко извлечь из коллекции.</span><span class="sxs-lookup"><span data-stu-id="6f29b-104">Though the code samples are divided into a series of tutorial lessons, the appropriate sample groupings can easily be extracted from the collection.</span></span> <span data-ttu-id="6f29b-105">Большинство отдельных каталогов примеров предназначены для работы в сочетании с одним и тем же каталогом примеров.</span><span class="sxs-lookup"><span data-stu-id="6f29b-105">Most of the individual sample directories are meant to work in conjunction with at least one other sample directory.</span></span> <span data-ttu-id="6f29b-106">Примеры, связанные с компонентами, состоят из пары "клиент-сервер" с сервером, требующим использования примера программы REGISTER.</span><span class="sxs-lookup"><span data-stu-id="6f29b-106">The component-related samples consist of a client and server pair, with the server requiring the use of the REGISTER sample utility.</span></span> <span data-ttu-id="6f29b-107">Ниже приведена сводка по примерам группирования и способам извлечения каждой группы в качестве единицы сборки.</span><span class="sxs-lookup"><span data-stu-id="6f29b-107">Here is a summary of the sample groupings and how to extract each group as a buildable unit.</span></span> <span data-ttu-id="6f29b-108">Для каждого примера группировки скопируйте содержимое указанных каталогов.</span><span class="sxs-lookup"><span data-stu-id="6f29b-108">For each sample grouping, copy the content of the directories shown.</span></span> <span data-ttu-id="6f29b-109">Для указанного \[ родительского \] каталога назначения не требуется содержимое из ветви Samples.</span><span class="sxs-lookup"><span data-stu-id="6f29b-109">The parent \[destination\] directory shown requires no content from the samples branch.</span></span> <span data-ttu-id="6f29b-110">Однако меню «Справка» в выполняющихся примерах предполагает, что вам нужно руководство. Файлы справки HTM находятся в этом родительском \[ \] каталоге назначения.</span><span class="sxs-lookup"><span data-stu-id="6f29b-110">However, the help menus in the running samples do assume that the appropriate tutorial .HTM help files are located in this parent \[destination\] directory.</span></span>

<span data-ttu-id="6f29b-111">Для приложения Win32 РЕАДТУТ:</span><span class="sxs-lookup"><span data-stu-id="6f29b-111">For the Win32 READTUT application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

<span data-ttu-id="6f29b-112">Для приложения с каркасом Win32 EXE:</span><span class="sxs-lookup"><span data-stu-id="6f29b-112">For the Win32 EXE skeleton application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

<span data-ttu-id="6f29b-113">Для схемы Win32 DLL:</span><span class="sxs-lookup"><span data-stu-id="6f29b-113">For the Win32 DLL skeleton:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

<span data-ttu-id="6f29b-114">Для основных примеров COM-объектов:</span><span class="sxs-lookup"><span data-stu-id="6f29b-114">For the basic COM object samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

<span data-ttu-id="6f29b-115">Для базового внутрипроцессного компонента DLL клиент/сервер-компонент:</span><span class="sxs-lookup"><span data-stu-id="6f29b-115">For the basic in-process DLL component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

<span data-ttu-id="6f29b-116">Для лицензий с лицензированным компонентом "клиент-сервер":</span><span class="sxs-lookup"><span data-stu-id="6f29b-116">For the licensed component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

<span data-ttu-id="6f29b-117">Для стандартных примеров маршалирования:</span><span class="sxs-lookup"><span data-stu-id="6f29b-117">For the standard marshaling samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

<span data-ttu-id="6f29b-118">Для необработанных примеров локального клиента/сервера:</span><span class="sxs-lookup"><span data-stu-id="6f29b-118">For the out-of-process local client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

<span data-ttu-id="6f29b-119">Для образцов клиент/сервер модели подразделения:</span><span class="sxs-lookup"><span data-stu-id="6f29b-119">For the apartment model client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

<span data-ttu-id="6f29b-120">Для образцов клиент/сервер DCOM (Distributed COM):</span><span class="sxs-lookup"><span data-stu-id="6f29b-120">For the DCOM (Distributed COM) client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

<span data-ttu-id="6f29b-121">Для бесплатных образцов клиента/сервера:</span><span class="sxs-lookup"><span data-stu-id="6f29b-121">For the free threading client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

<span data-ttu-id="6f29b-122">Для подключаемых примеров клиента или сервера COM-объекта:</span><span class="sxs-lookup"><span data-stu-id="6f29b-122">For the connectable COM object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

<span data-ttu-id="6f29b-123">Примеры для клиента или сервера структурированного хранилища:</span><span class="sxs-lookup"><span data-stu-id="6f29b-123">For the structured storage client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

<span data-ttu-id="6f29b-124">Для примеров "клиент-сервер постоянных объектов":</span><span class="sxs-lookup"><span data-stu-id="6f29b-124">For the persistent object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

<span data-ttu-id="6f29b-125">Примеры для клиента/сервера безопасности DCOM:</span><span class="sxs-lookup"><span data-stu-id="6f29b-125">For the DCOM security client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




