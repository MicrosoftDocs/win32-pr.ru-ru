---
description: Монопольный режим DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Монопольный режим DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673109"
---
# <a name="directdraw-exclusive-mode"></a><span data-ttu-id="66b4e-103">Монопольный режим DirectDraw</span><span class="sxs-lookup"><span data-stu-id="66b4e-103">DirectDraw Exclusive Mode</span></span>

> [!Note]  
> <span data-ttu-id="66b4e-104">Этот раздел относится только к VMR-7.</span><span class="sxs-lookup"><span data-stu-id="66b4e-104">This topic applies to the VMR-7 only.</span></span> <span data-ttu-id="66b4e-105">В VMR-9 вы включаете монопольный режим, предоставляя собственный механизм выделения-выступающего в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="66b4e-105">In the VMR-9, you enable exclusive mode by supplying your own exclusive mode allocator-presenter.</span></span> <span data-ttu-id="66b4e-106">Это относительно просто, если используется метод [**IVMRSurfaceAllocatorNotify9:: аллокатесурфацехелпер**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) .</span><span class="sxs-lookup"><span data-stu-id="66b4e-106">This is relatively straightforward if you use the [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) method.</span></span> <span data-ttu-id="66b4e-107">В примере VMR9Allocator показано, как реализовать пользовательский распределитель-представление.</span><span class="sxs-lookup"><span data-stu-id="66b4e-107">The VMR9Allocator sample shows how to implement a custom allocator-presenter.</span></span>

 

<span data-ttu-id="66b4e-108">В режиме монопольного режима DirectDraw приложение получает эксклюзивный контроль над графическим оборудованием.</span><span class="sxs-lookup"><span data-stu-id="66b4e-108">In DirectDraw Exclusive Mode, an application takes exclusive control of the graphics hardware.</span></span> <span data-ttu-id="66b4e-109">Это полезно для таких приложений, как игры или полноэкранные видео-приложения.</span><span class="sxs-lookup"><span data-stu-id="66b4e-109">This is useful for applications such as games, or perhaps full-screen video applications.</span></span> <span data-ttu-id="66b4e-110">Как правило, VMR создает объекты DirectDraw и устанавливает для уровня совместного функционирования значение обычный.</span><span class="sxs-lookup"><span data-stu-id="66b4e-110">Normally, the VMR creates the DirectDraw objects and sets the cooperative level to normal.</span></span> <span data-ttu-id="66b4e-111">Однако для запуска VMR в режиме монопольного режима DirectDraw приложение должно создать объект DirectDraw и основную поверхность, а также вызвать **сеткуперативелевел** , чтобы указать монопольный режим.</span><span class="sxs-lookup"><span data-stu-id="66b4e-111">However, to run the VMR in DirectDraw Exclusive Mode, the application itself must create the DirectDraw object and the primary surface, and call **SetCooperativeLevel** to specify exclusive mode.</span></span>

<span data-ttu-id="66b4e-112">VMR имеет специальный механизм распределителя-Presenter, который позволяет запускать его в режиме монопольного доступа DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="66b4e-112">The VMR has a special allocator-presenter that enables it to run in DirectDraw Exclusive Mode.</span></span> <span data-ttu-id="66b4e-113">Чтобы настроить VMR для использования этого распределителя-Presenter, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="66b4e-113">To configure the VMR to use this allocator-presenter:</span></span>

1.  <span data-ttu-id="66b4e-114">Создайте граф фильтра и добавьте в него фильтр VMR с помощью метода [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) .</span><span class="sxs-lookup"><span data-stu-id="66b4e-114">Create the Filter Graph and add the VMR to it using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="66b4e-115">Пример кода см. в разделе [режим без окон VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="66b4e-115">For a code example, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span>
2.  <span data-ttu-id="66b4e-116">Создайте монопольный режим распределителя-Presenter:</span><span class="sxs-lookup"><span data-stu-id="66b4e-116">Create the Exclusive Mode allocator-presenter:</span></span>
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  <span data-ttu-id="66b4e-117">Настройте новый распределитель-выступающий:</span><span class="sxs-lookup"><span data-stu-id="66b4e-117">Configure the new allocator-presenter:</span></span>
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  <span data-ttu-id="66b4e-118">Подключите новый распределитель-представление к VMR.</span><span class="sxs-lookup"><span data-stu-id="66b4e-118">Plug the new allocator-presenter into the VMR.</span></span>
5.  <span data-ttu-id="66b4e-119">Создайте остальную часть графа фильтра обычным образом.</span><span class="sxs-lookup"><span data-stu-id="66b4e-119">Build the rest of the filter graph in the usual ways.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66b4e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="66b4e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66b4e-121">Режимы VMR в операции</span><span class="sxs-lookup"><span data-stu-id="66b4e-121">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
</dt> </dl>

 

 



