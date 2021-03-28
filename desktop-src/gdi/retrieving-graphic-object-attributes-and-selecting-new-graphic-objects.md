---
title: Получение атрибутов объекта, выбор новых объектов
description: Приложение может извлекать атрибуты для пера, кисти, палитры, шрифта или точечного рисунка путем вызова функций Жеткуррентобжект и GetObject.
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18dcef03bf769e8b2d11574429b64f481b1a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984812"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>Получение атрибутов объекта, выбор новых объектов

Приложение может извлекать атрибуты для пера, кисти, палитры, шрифта или точечного рисунка путем вызова функций [**жеткуррентобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) и [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . Функция **жеткуррентобжект** возвращает маркер, идентифицирующий объект, выбранный в данный момент в контроллере домена. Функция **GetObject** возвращает структуру, описывающую атрибуты объекта.

В следующем примере показано, как приложение может извлекать текущие атрибуты кисти и использовать полученные данные, чтобы определить, нужно ли выбрать новую кисть.


```C++
    HDC hdc;                     // display DC handle  
    HBRUSH hbrushNew, hbrushOld; // brush handles  
    HBRUSH hbrush;               // brush handle  
    LOGBRUSH lb;                 // logical-brush structure  
 
    // Retrieve a handle identifying the current brush.  
 
    hbrush = GetCurrentObject(hdc, OBJ_BRUSH); 
 
    // Retrieve a LOGBRUSH structure that contains the  
    // current brush attributes.  
 
    GetObject(hbrush, sizeof(LOGBRUSH), &lb); 
 
    // If the current brush is not a solid-black brush,  
    // replace it with the solid-black stock brush.  
 
    if ((lb.lbStyle != BS_SOLID) 
           || (lb.lbColor != 0x000000)) 
    { 
        hbrushNew = GetStockObject(BLACK_BRUSH); 
        hbrushOld = SelectObject(hdc, hbrushNew); 
    } 
 
    // Perform painting operations with the white brush.  
 
 
    // After completing the last painting operation with the new  
    // brush, the application should select the original brush back  
    // into the device context and delete the new brush.  
    // In this example, hbrushNew contains a handle to a stock object.  
    // It is not necessary (but it is not harmful) to call  
    // DeleteObject on a stock object. If hbrushNew contained a handle  
    // to a brush created by a function such as CreateBrushIndirect,  
    // it would be necessary to call DeleteObject.  
 
    SelectObject(hdc, hbrushOld); 
    DeleteObject(hbrushNew); 
```



> [!Note]
>
> Приложение сохранило исходный дескриптор кисти при первом вызове функции [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Этот дескриптор сохраняется таким образом, чтобы исходная кисть могла быть выбрана обратно в контроллер домена после завершения последней операции рисования с новой кистью. После того, как исходная кисть снова выбрана в контроллере домена, Новая кисть удаляется, освобождая память в куче GDI.

 

 

 



