---
title: Управление памятью в эмуляторе WOW64
description: Управление памятью в эмуляторе WOW64 зависит от архитектуры процессора.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64-разрядное программирование Windows, управление памятью
- Управление памятью 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413521"
---
# <a name="memory-management-under-wow64"></a><span data-ttu-id="9ddfb-105">Управление памятью в эмуляторе WOW64</span><span class="sxs-lookup"><span data-stu-id="9ddfb-105">Memory Management Under WOW64</span></span>

<span data-ttu-id="9ddfb-106">Управление памятью в эмуляторе WOW64 зависит от архитектуры процессора.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-106">Memory management under WOW64 depends on the processor architecture.</span></span>

## <a name="itanium-support"></a><span data-ttu-id="9ddfb-107">Поддержка Itanium</span><span class="sxs-lookup"><span data-stu-id="9ddfb-107">Itanium Support</span></span>

<span data-ttu-id="9ddfb-108">WOW64 имитирует 4 КБ страниц поверх собственных 8 КБ страниц, используемых процессором Itanium.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-108">WOW64 simulates 4 KB pages on top of the native 8 KB pages that the Itanium processor uses.</span></span> <span data-ttu-id="9ddfb-109">Это помогает процессору, обеспечивая отличное моделирование с низкими издержками.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-109">The processor assists by providing excellent simulation with low overhead.</span></span> <span data-ttu-id="9ddfb-110">Код моделирования не может работать в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="9ddfb-110">The simulation code cannot handle the following cases:</span></span>

-   <span data-ttu-id="9ddfb-111">Отслеживание записи.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-111">Write tracking.</span></span> <span data-ttu-id="9ddfb-112">Функции [**жетвритеватч**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) и [**ресетвритеватч**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) реализуются в ядре с использованием собственной гранулярности размера страницы, что означает, что имитация страницы WOW64 4 КБ не может определить, какие из них будут записаны на странице размером 8 КБ.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-112">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are implemented in the kernel using native page-size granularity, which means the WOW64 4 KB page simulation cannot determine which simulated 4 KB pages are written within the underlying 8 KB page.</span></span>
-   <span data-ttu-id="9ddfb-113">[Расширения AWE](/windows/desktop/Memory/address-windowing-extensions).</span><span class="sxs-lookup"><span data-stu-id="9ddfb-113">[Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span></span> <span data-ttu-id="9ddfb-114">Функции AWE работают с номерами страниц, и не существует способа сопоставлять 64-разрядные номера страниц с номерами страниц 32-бит.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-114">The AWE functions operate on page numbers, and there is no way to map 64-bit page numbers to 32-bit page numbers.</span></span>
-   <span data-ttu-id="9ddfb-115">Выравнивание раздела.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-115">Section alignment.</span></span> <span data-ttu-id="9ddfb-116">Для исполняемых образов с выравниванием разделов менее 8 КБ (значение по умолчанию — 4 КБ для образов x86), WOW64 должен быть грязным для всех страниц изображений.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-116">For executable images with section alignment smaller than 8 KB (the default is 4 KB for x86 images), WOW64 must dirty all image pages.</span></span> <span data-ttu-id="9ddfb-117">Это эффективно копирует каждую страницу в файл подкачки и предотвращает совместное применение страниц изображений только для чтения между процессами.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-117">This effectively copies each page to the page file, and prevents read-only image pages from being shared between processes.</span></span>
-   <span data-ttu-id="9ddfb-118">Функции [**реадфилескаттер**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) и [**вритефилегасер**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-118">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are not supported.</span></span>

## <a name="x64-and-arm64-support"></a><span data-ttu-id="9ddfb-119">Поддержка x64 и ARM64</span><span class="sxs-lookup"><span data-stu-id="9ddfb-119">x64 and ARM64 Support</span></span>

<span data-ttu-id="9ddfb-120">Собственный размер страницы — 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-120">The native page size is 4 KB.</span></span> <span data-ttu-id="9ddfb-121">Таким образом, поддерживаются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-121">Therefore, the following are supported:</span></span>

-   <span data-ttu-id="9ddfb-122">Поддерживаются функции [**жетвритеватч**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) и [**ресетвритеватч**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) .</span><span class="sxs-lookup"><span data-stu-id="9ddfb-122">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are supported.</span></span>
-   <span data-ttu-id="9ddfb-123">Поддерживаются функции [**реадфилескаттер**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) и [**вритефилегасер**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="9ddfb-123">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are supported.</span></span>
-   <span data-ttu-id="9ddfb-124">Использование больших адресов имеет свои преимущества, так как x64 WOW64 поддерживает виртуальное адресное пространство размером 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-124">There are advantages to using large addresses because x64 WOW64 supports a 4 GB virtual address space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ddfb-125">См. также</span><span class="sxs-lookup"><span data-stu-id="9ddfb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ddfb-126">Ограничения памяти для выпусков Windows</span><span class="sxs-lookup"><span data-stu-id="9ddfb-126">Memory Limits for Windows Releases</span></span>](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[<span data-ttu-id="9ddfb-127">Настройка ОЗУ 4GT</span><span class="sxs-lookup"><span data-stu-id="9ddfb-127">4GT RAM Tuning</span></span>](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 