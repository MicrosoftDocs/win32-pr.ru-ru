---
title: Адресное пространство, доступное для мозаичного заполнения ресурсов
description: В этом разделе указывается виртуальное адресное пространство, доступное для мозаичного заполнения ресурсов.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2019
ms.locfileid: "103784863"
---
# <a name="address-space-available-for-tiled-resources"></a><span data-ttu-id="64d84-103">Адресное пространство, доступное для мозаичного заполнения ресурсов</span><span class="sxs-lookup"><span data-stu-id="64d84-103">Address space available for tiled resources</span></span>

<span data-ttu-id="64d84-104">В этом разделе указывается виртуальное адресное пространство, доступное для мозаичного заполнения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64d84-104">This section specifies the virtual address space that is available for tiled resources.</span></span>

<span data-ttu-id="64d84-105">В 64-разрядных операционных системах доступно не менее 40 бит виртуального адресного пространства (1 ТБ).</span><span class="sxs-lookup"><span data-stu-id="64d84-105">On 64-bit operating systems, at least 40 bits of virtual address space (1 Terabyte) is available.</span></span>

<span data-ttu-id="64d84-106">В 32-разрядных операционных системах адресное пространство составляет 32 бит (4 ГБ).</span><span class="sxs-lookup"><span data-stu-id="64d84-106">For 32-bit operating systems, the address space is 32 bit (4 GB).</span></span> <span data-ttu-id="64d84-107">Для 32-разрядных систем ARM может произойти сбой отдельного создания ресурсов, если распределение будет использовать более 27 бит адресного пространства (128 МБ).</span><span class="sxs-lookup"><span data-stu-id="64d84-107">For 32-bit ARM systems, individual tiled resource creation can fail if the allocation would use more than 27 bits of address space (128 MB).</span></span> <span data-ttu-id="64d84-108">Сюда относятся и все скрытые отбивки в адресном пространстве, которые оборудование может использовать для текстур, отбивки упакованных плиток и, возможно, измерений поверхности отбивки, кратных 2.</span><span class="sxs-lookup"><span data-stu-id="64d84-108">This includes any hidden padding in the address space the hardware may use for mipmaps, packed tile padding, and possibly padding surface dimensions to powers of 2.</span></span>

<span data-ttu-id="64d84-109">В графических системах с отдельной таблицей страниц для графического процессора большая часть этого адресного пространства будет доступна ресурсам графического процессора, созданным приложением, несмотря на то что выделенные ресурсы графического процессора для видеодрайвера размещаются там же.</span><span class="sxs-lookup"><span data-stu-id="64d84-109">On graphics systems with a separate page table for the graphics processing unit (GPU), most of this address space will be available to GPU resources made by the application, though GPU allocations made by the display driver fit in the same space.</span></span>

<span data-ttu-id="64d84-110">В будущем в системах, где таблица страниц совместно используется ЦП и графическим процессором, доступное адресное пространство будет совместно использоваться всеми выделениями ЦП и графического процессора в рамках процесса.</span><span class="sxs-lookup"><span data-stu-id="64d84-110">On future systems with a page table shared between the CPU and GPU, the available address space is shared between all CPU and GPU allocations in a process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64d84-111">См. также</span><span class="sxs-lookup"><span data-stu-id="64d84-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64d84-112">Параметры создания мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="64d84-112">Tiled resource creation parameters</span></span>](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




