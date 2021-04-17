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
# <a name="directdraw-exclusive-mode"></a>Монопольный режим DirectDraw

> [!Note]  
> Этот раздел относится только к VMR-7. В VMR-9 вы включаете монопольный режим, предоставляя собственный механизм выделения-выступающего в монопольном режиме. Это относительно просто, если используется метод [**IVMRSurfaceAllocatorNotify9:: аллокатесурфацехелпер**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) . В примере VMR9Allocator показано, как реализовать пользовательский распределитель-представление.

 

В режиме монопольного режима DirectDraw приложение получает эксклюзивный контроль над графическим оборудованием. Это полезно для таких приложений, как игры или полноэкранные видео-приложения. Как правило, VMR создает объекты DirectDraw и устанавливает для уровня совместного функционирования значение обычный. Однако для запуска VMR в режиме монопольного режима DirectDraw приложение должно создать объект DirectDraw и основную поверхность, а также вызвать **сеткуперативелевел** , чтобы указать монопольный режим.

VMR имеет специальный механизм распределителя-Presenter, который позволяет запускать его в режиме монопольного доступа DirectDraw. Чтобы настроить VMR для использования этого распределителя-Presenter, сделайте следующее:

1.  Создайте граф фильтра и добавьте в него фильтр VMR с помощью метода [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Пример кода см. в разделе [режим без окон VMR](vmr-windowless-mode.md).
2.  Создайте монопольный режим распределителя-Presenter:
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

    

3.  Настройте новый распределитель-выступающий:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Подключите новый распределитель-представление к VMR.
5.  Создайте остальную часть графа фильтра обычным образом.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Режимы VMR в операции](vmr-modes-of-operation.md)
</dt> </dl>

 

 



