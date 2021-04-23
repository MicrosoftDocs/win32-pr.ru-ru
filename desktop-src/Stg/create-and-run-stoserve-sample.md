---
title: Создание и запуск примера Стосерве
description: Перед запуском клиента необходимо скомпилировать образец клиента и другие связанные образцы.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661539"
---
# <a name="create-and-run-stoserve-sample"></a><span data-ttu-id="dae63-103">Создание и запуск примера Стосерве</span><span class="sxs-lookup"><span data-stu-id="dae63-103">Create and Run StoServe Sample</span></span>

<span data-ttu-id="dae63-104">Перед запуском клиента необходимо скомпилировать образец клиента и другие связанные образцы.</span><span class="sxs-lookup"><span data-stu-id="dae63-104">The client sample and other related samples must be compiled before you can run the client.</span></span> <span data-ttu-id="dae63-105">Дополнительные сведения о построении образцов см. в разделе Создание [образцов](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="dae63-105">For more details on building the samples, see [How to Build Samples](how-to-build-samples.md).</span></span> <span data-ttu-id="dae63-106">Если вы уже создали соответствующие примеры, STOCLIEN.EXE — клиентский исполняемый файл для выполнения примера **стосерве** .</span><span class="sxs-lookup"><span data-stu-id="dae63-106">If you have already built the appropriate samples, STOCLIEN.EXE is the client executable to run for the **StoServe** sample.</span></span>

## <a name="code-tour"></a><span data-ttu-id="dae63-107">Обзор кода</span><span class="sxs-lookup"><span data-stu-id="dae63-107">Code Tour</span></span>

<span data-ttu-id="dae63-108">В следующей таблице перечислены файлы, относящиеся к примеру **стосерве** .</span><span class="sxs-lookup"><span data-stu-id="dae63-108">The following table lists the files pertinent to the **StoServe** sample.</span></span>



| <span data-ttu-id="dae63-109">Файлы</span><span class="sxs-lookup"><span data-stu-id="dae63-109">Files</span></span>        | <span data-ttu-id="dae63-110">Описание</span><span class="sxs-lookup"><span data-stu-id="dae63-110">Description</span></span>                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae63-111">STOSERVE.TXT</span><span class="sxs-lookup"><span data-stu-id="dae63-111">STOSERVE.TXT</span></span> | <span data-ttu-id="dae63-112">Краткое описание образца</span><span class="sxs-lookup"><span data-stu-id="dae63-112">Short sample description</span></span>                                                                                                  |
| <span data-ttu-id="dae63-113">ФАЙЛЫ</span><span class="sxs-lookup"><span data-stu-id="dae63-113">MAKEFILE</span></span>     | <span data-ttu-id="dae63-114">Универсальный файл makefile для создания образца кода STOSERVE.DLL этого занятия.</span><span class="sxs-lookup"><span data-stu-id="dae63-114">The generic makefile for building the STOSERVE.DLL code sample of this lesson.</span></span>                                            |
| <span data-ttu-id="dae63-115">СТОСЕРВЕ. Высоты</span><span class="sxs-lookup"><span data-stu-id="dae63-115">STOSERVE.H</span></span>   | <span data-ttu-id="dae63-116">Включаемый файл для объявления как импортированного или определяющего экспортирования функций службы в STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="dae63-116">The include file for declaring as imported or defining as exported the service functions in STOSERVE.DLL.</span></span>                 |
| <span data-ttu-id="dae63-117">СТОСЕРВЕ. CPP</span><span class="sxs-lookup"><span data-stu-id="dae63-117">STOSERVE.CPP</span></span> | <span data-ttu-id="dae63-118">Основной файл реализации для STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="dae63-118">The main implementation file for STOSERVE.DLL.</span></span> <span data-ttu-id="dae63-119">Имеет функцию DllMain и функции сервера COM (например, DllGetClassObject).</span><span class="sxs-lookup"><span data-stu-id="dae63-119">Has DllMain and the COM server functions (for example, DllGetClassObject).</span></span> |
| <span data-ttu-id="dae63-120">СТОСЕРВЕ. DEF</span><span class="sxs-lookup"><span data-stu-id="dae63-120">STOSERVE.DEF</span></span> | <span data-ttu-id="dae63-121">Файл определения модуля.</span><span class="sxs-lookup"><span data-stu-id="dae63-121">The module definition file.</span></span> <span data-ttu-id="dae63-122">Экспортирует функции серверного корпуса.</span><span class="sxs-lookup"><span data-stu-id="dae63-122">Exports server housing functions.</span></span>                                                             |
| <span data-ttu-id="dae63-123">СТОСЕРВЕ. RC</span><span class="sxs-lookup"><span data-stu-id="dae63-123">STOSERVE.RC</span></span>  | <span data-ttu-id="dae63-124">Файл определения ресурса DLL для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="dae63-124">The DLL resource definition file for the executable.</span></span>                                                                      |
| <span data-ttu-id="dae63-125">СТОСЕРВЕ. ICO</span><span class="sxs-lookup"><span data-stu-id="dae63-125">STOSERVE.ICO</span></span> | <span data-ttu-id="dae63-126">Ресурс значка для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="dae63-126">The icon resource for the executable.</span></span>                                                                                     |
| <span data-ttu-id="dae63-127">Сервером. Высоты</span><span class="sxs-lookup"><span data-stu-id="dae63-127">SERVER.H</span></span>     | <span data-ttu-id="dae63-128">Включаемый файл для объекта серверного элемента управления C++.</span><span class="sxs-lookup"><span data-stu-id="dae63-128">The include file for the server control C++ object.</span></span>                                                                       |
| <span data-ttu-id="dae63-129">Сервером. CPP</span><span class="sxs-lookup"><span data-stu-id="dae63-129">SERVER.CPP</span></span>   | <span data-ttu-id="dae63-130">Файл реализации для объекта серверного элемента управления C++.</span><span class="sxs-lookup"><span data-stu-id="dae63-130">The implementation file for the server control C++ object.</span></span>                                                                |
| <span data-ttu-id="dae63-131">Установлен. Высоты</span><span class="sxs-lookup"><span data-stu-id="dae63-131">FACTORY.H</span></span>    | <span data-ttu-id="dae63-132">Включаемый файл для COM-объектов фабрики класса сервера.</span><span class="sxs-lookup"><span data-stu-id="dae63-132">The include file for the server's class factory COM objects.</span></span>                                                              |
| <span data-ttu-id="dae63-133">Установлен. CPP</span><span class="sxs-lookup"><span data-stu-id="dae63-133">FACTORY.CPP</span></span>  | <span data-ttu-id="dae63-134">Файл реализации фабрик класса сервера.</span><span class="sxs-lookup"><span data-stu-id="dae63-134">The implementation file for the server's class factories.</span></span>                                                                 |
| <span data-ttu-id="dae63-135">Соединиться. Высоты</span><span class="sxs-lookup"><span data-stu-id="dae63-135">CONNECT.H</span></span>    | <span data-ttu-id="dae63-136">Включаемый файл для классов перечислителя точек соединения, точек соединения и перечислителей подключений.</span><span class="sxs-lookup"><span data-stu-id="dae63-136">The include file for the connection point enumerator, connection point, and connection enumerator classes.</span></span>                |
| <span data-ttu-id="dae63-137">Соединиться. CPP</span><span class="sxs-lookup"><span data-stu-id="dae63-137">CONNECT.CPP</span></span>  | <span data-ttu-id="dae63-138">Файл реализации для перечислителя точки соединения, точки соединения и объектов перечислителя подключений.</span><span class="sxs-lookup"><span data-stu-id="dae63-138">The implementation file for the connection point enumerator, connection point, and connection enumerator objects.</span></span>         |
| <span data-ttu-id="dae63-139">Letter. Высоты</span><span class="sxs-lookup"><span data-stu-id="dae63-139">PAPER.H</span></span>      | <span data-ttu-id="dae63-140">Включаемый файл для класса кобумажного COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="dae63-140">The include file for the COPaper COM object class.</span></span>                                                                        |
| <span data-ttu-id="dae63-141">Letter. CPP</span><span class="sxs-lookup"><span data-stu-id="dae63-141">PAPER.CPP</span></span>    | <span data-ttu-id="dae63-142">Файл реализации для класса кобумажного COM-объекта и точек соединения.</span><span class="sxs-lookup"><span data-stu-id="dae63-142">The implementation file for the COPaper COM object class and the connection points.</span></span>                                       |
| <span data-ttu-id="dae63-143">СТОСЕРВЕ. DSP</span><span class="sxs-lookup"><span data-stu-id="dae63-143">STOSERVE.DSP</span></span> | <span data-ttu-id="dae63-144">Microsoft Visual Studio файл проекта.</span><span class="sxs-lookup"><span data-stu-id="dae63-144">Microsoft Visual Studio Project file.</span></span>                                                                                     |



 

<span data-ttu-id="dae63-145">В этом обзоре кода рассматриваются следующие основные темы:</span><span class="sxs-lookup"><span data-stu-id="dae63-145">The major topics covered in this code tour are:</span></span>

-   <span data-ttu-id="dae63-146">Методы интерфейса [**ипапер**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="dae63-146">The [**IPaper**](ipaper-methods.md) interface methods.</span></span>
-   <span data-ttu-id="dae63-147">Использование интерфейса [**ипаперсинк**](ipapersink-methods.md) для клиентских уведомлений.</span><span class="sxs-lookup"><span data-stu-id="dae63-147">COPaper's use of the [**IPaperSink**](ipapersink-methods.md) interface for client notifications.</span></span>
-   <span data-ttu-id="dae63-148">[**Структуры**](structures---stoserve.md) в стосерве.</span><span class="sxs-lookup"><span data-stu-id="dae63-148">[**Structures**](structures---stoserve.md) in StoServe.</span></span>
-   <span data-ttu-id="dae63-149">[Рекомендации по Юникоду](unicode-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="dae63-149">[Unicode considerations](unicode-considerations.md).</span></span>

 

 




