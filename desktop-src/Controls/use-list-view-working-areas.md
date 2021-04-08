---
title: Использование List-View рабочих областей
description: В этом разделе показано, как работать с рабочими областями в представлении списка. Рабочие области представляют собой прямоугольные виртуальные области, которые можно использовать для упорядочения элементов в элементе управления List-представление.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067806"
---
# <a name="how-to-use-list-view-working-areas"></a>Использование List-View рабочих областей

В этом разделе показано, как работать с рабочими областями в представлении списка. Рабочие области представляют собой прямоугольные виртуальные области, которые можно использовать для упорядочения элементов в элементе управления List-представление. Рабочая область не является окном и не может иметь видимую границу. По умолчанию элемент управления "представление списка" не имеет рабочих областей. Создавая рабочую область, можно создать пустую границу слева, сверху или справа от элементов или вызвать горизонтальную полосу прокрутки, если обычно это не будет.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="create-a-working-area"></a>Создание рабочей области

В следующем примере кода C++ показано, как создать рабочую область с пустой границей размером 25 пикселей в верхней, левой и правой частях.


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a>Создание нескольких рабочих областей

В следующем примере кода C++ показано, как создать две рабочие области в элементе управления. Каждая Рабочая область использует около половины клиентской области и окружена пустой границей размером в 25 пикселей.


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a>Определение рабочей области, к которой принадлежит элемент

Одним из способов определения рабочей области, к которой принадлежит элемент, является выполнение следующих действий.

-   Получение списка координат всех рабочих областей в элементе управления "представление списка".
-   Получение координат элемента.
-   Определите, находятся ли координаты элемента в координатах одной из рабочих областей.

Определяемая приложением функция в следующем примере кода C++ возвращает индекс рабочей области, к которой принадлежит элемент. Если функция завершается с ошибкой, возвращается значение – 1. Если функция завершается с ошибкой, но элемент не входит в рабочие области, функция возвращает 0, так как все элементы, которые находятся вне рабочей области, автоматически становятся членами нулевой области.


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по элементу управления представления списка](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Сведения об элементах управления List-View](list-view-controls-overview.md)
</dt> <dt>

[Использование элементов управления List-View](using-list-view-controls.md)
</dt> </dl>

 

 




