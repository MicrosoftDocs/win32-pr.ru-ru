---
title: Интерфейсы Иавистреам и Иавифиле
description: Интерфейсы Иавистреам и Иавифиле
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Интерфейс Иавистреам
- Интерфейс Иавифиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888595"
---
# <a name="iavistream-and-iavifile-interfaces"></a><span data-ttu-id="4e082-105">Интерфейсы Иавистреам и Иавифиле</span><span class="sxs-lookup"><span data-stu-id="4e082-105">IAVIStream and IAVIFile Interfaces</span></span>

<span data-ttu-id="4e082-106">Интерфейсы [**иавистреам**](/windows/desktop/api/Vfw/nn-vfw-iavistream) и [**иавифиле**](/windows/desktop/api/Vfw/nn-vfw-iavifile) содержат методы, используемые обработчиками файлов и потоков.</span><span class="sxs-lookup"><span data-stu-id="4e082-106">The [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) and [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) interfaces contain the methods used by file and stream handlers.</span></span> <span data-ttu-id="4e082-107">Тип данных **павистреам** — это указатель на объект потока AVI (через интерфейс **иавистреам** ), а тип данных **павифиле** — это указатель на объект AVI-файла (через интерфейс **иавифиле** ).</span><span class="sxs-lookup"><span data-stu-id="4e082-107">The **PAVISTREAM** data type is a pointer to an AVI stream object (through the **IAVIStream** interface) and the **PAVIFILE** data type is a pointer to an AVI file object (through the **IAVIFile** interface).</span></span>

<span data-ttu-id="4e082-108">Чтобы создать указатель на объект в языке C, сначала нужно выделить пространство для структуры, достаточно большой для размещения указателя на таблицу виртуальной функции и других элементов данных.</span><span class="sxs-lookup"><span data-stu-id="4e082-108">To create an object pointer in C, first allocate space for a structure that is large enough to contain the pointer to the virtual function table and the other data members.</span></span> <span data-ttu-id="4e082-109">Создайте таблицу виртуальной функции для методов вашего типа потока, а затем установите указатель на таблицу виртуальной функции в адрес таблицы виртуальной функции.</span><span class="sxs-lookup"><span data-stu-id="4e082-109">Create a virtual function table for the methods for your type of stream, then set the pointer to the virtual function table to the address of the virtual function table.</span></span>

 

 




