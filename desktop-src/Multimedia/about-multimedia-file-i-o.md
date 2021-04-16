---
title: О файловых операциях ввода-вывода мультимедиа
description: О файловых операциях ввода-вывода мультимедиа
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Мультимедиа Windows, файловый ввод-вывод
- мультимедиа, файловый ввод-вывод
- входные данные мультимедиа, файловый ввод-вывод
- Ввод-вывод файлов мультимедиа, о программе
- Ввод-вывод файлов, сведения
- входные и выходные данные (ввод-вывод), сведения
- Ввод-вывод (входные и выходные данные), сведения
- Базовый ввод-вывод
- формат файла обмена ресурсами (Metallica)
- Metallica (формат файла обмена ресурсами)
- ВВОД-ВЫВОД METALLICA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672069"
---
# <a name="about-multimedia-file-io"></a><span data-ttu-id="82d59-114">О файловых операциях ввода-вывода мультимедиа</span><span class="sxs-lookup"><span data-stu-id="82d59-114">About Multimedia File I/O</span></span>

<span data-ttu-id="82d59-115">Большинству приложений для мультимедиа требуется ввод-вывод файлов (I/O), то есть возможность создавать, читать и записывать файлы на диске.</span><span class="sxs-lookup"><span data-stu-id="82d59-115">Most multimedia applications require file input and output (I/O) — that is, the ability to create, read, and write disk files.</span></span> <span data-ttu-id="82d59-116">Службы файлового ввода-вывода предоставляют буферизованные и небуферизованные файловые операции ввода-вывода и поддерживают файлы Metallica.</span><span class="sxs-lookup"><span data-stu-id="82d59-116">Multimedia file I/O services provide buffered and unbuffered file I/O and support for RIFF files.</span></span> <span data-ttu-id="82d59-117">Службы расширяются с помощью пользовательских процедур ввода-вывода, которые могут совместно использоваться различными приложениями.</span><span class="sxs-lookup"><span data-stu-id="82d59-117">The services are extensible with custom I/O procedures that can be shared among applications.</span></span>

<span data-ttu-id="82d59-118">Большинству приложений требуются только базовые службы файлового ввода-вывода и службы файлового ввода-вывода Metallica.</span><span class="sxs-lookup"><span data-stu-id="82d59-118">Most applications need only the basic file I/O services and the RIFF file I/O services.</span></span> <span data-ttu-id="82d59-119">Приложения, учитывающие производительность операций ввода-вывода файлов, таких как приложения, которые потоковая передача данных с компакт-диска в режиме реального времени, могут оптимизировать производительность, используя службы для прямого доступа к буферу файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="82d59-119">Applications sensitive to file I/O performance, such as applications that stream data from compact disc in real time, can optimize performance by using services to directly access the file I/O buffer.</span></span> <span data-ttu-id="82d59-120">Приложения, обращающиеся к пользовательским системам хранения, таким как архивы файлов и базы данных, могут предоставлять собственную процедуру ввода-вывода, которая считывает и записывает элементы системы хранения.</span><span class="sxs-lookup"><span data-stu-id="82d59-120">Applications that access custom storage systems, such as file archives and databases, can provide their own I/O procedure that reads and writes elements of the storage system.</span></span>

 

 




