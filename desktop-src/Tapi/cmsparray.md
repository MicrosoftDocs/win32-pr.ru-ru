---
description: Шаблон Кмспаррай реализует интеллектуальный массив, который будет расти по запросу.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: кмспаррай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998609"
---
# <a name="cmsparray"></a><span data-ttu-id="e4645-103">кмспаррай</span><span class="sxs-lookup"><span data-stu-id="e4645-103">CMSPArray</span></span>

<span data-ttu-id="e4645-104">Шаблон Кмспаррай реализует интеллектуальный массив, который будет расти по запросу.</span><span class="sxs-lookup"><span data-stu-id="e4645-104">The CMSPArray template implements a smart array that will grow on demand.</span></span> <span data-ttu-id="e4645-105">Он предназначен для хранения небольших массивов с простыми типами данных.</span><span class="sxs-lookup"><span data-stu-id="e4645-105">It is designed to hold small arrays with simple data types.</span></span> <span data-ttu-id="e4645-106">У него нет критической секции.</span><span class="sxs-lookup"><span data-stu-id="e4645-106">It doesn't have a critical section.</span></span> <span data-ttu-id="e4645-107">Его единственными зависимостями являются **realloc** и **memmove**.</span><span class="sxs-lookup"><span data-stu-id="e4645-107">Its only dependencies are **realloc** and **memmove**.</span></span> <span data-ttu-id="e4645-108">Он используется внутренним образом для сохранения списков указателей объектов.</span><span class="sxs-lookup"><span data-stu-id="e4645-108">It is used internally to keep lists of object pointers.</span></span> <span data-ttu-id="e4645-109">Он похож на реализацию **ксимплеаррай** в ATL, но более эффективен для первоначального выделения.</span><span class="sxs-lookup"><span data-stu-id="e4645-109">It is similar to ATL's **CSimpleArray** implementation, but it is more efficient for initial allocations.</span></span>

<span data-ttu-id="e4645-110">Этот шаблон определен в Мспутилс. h.</span><span class="sxs-lookup"><span data-stu-id="e4645-110">This template is defined in MSPutils.h.</span></span>

 

 



