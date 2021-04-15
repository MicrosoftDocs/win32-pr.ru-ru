---
title: Печать изображения OpenGL
description: Вы можете печатать изображения OpenGL, подготовленные в виде расширенных метафайлов.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL в Windows, печать
- Печать изображений OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661774"
---
# <a name="printing-an-opengl-image"></a>Печать изображения OpenGL

Вы можете печатать изображения OpenGL, подготовленные в виде расширенных метафайлов. При подготовке к просмотру на устройстве печати (HDC) оно должно поддерживаться диспетчером очереди метафайлов. OpenGL использует память для глубины, цвета и других буферов для хранения выходных данных графики на принтере. Так как для обычного разрешения принтера требуется значительный объем памяти для хранения графических данных, печать изображения OpenGL может потребовать больше памяти, чем доступно в системе. Чтобы преодолеть это ограничение, текущая реализация OpenGL печатает графики OpenGL в полосах. Однако это увеличивает время, затрачиваемое на печать изображений OpenGL.

Перед печатью образа OpenGL необходимо вызвать функцию [стартдок](/windows/desktop/api/wingdi/nf-wingdi-startdoca) для завершения инициализации контекста устройства печати (DC). После вызова **стартдок** можно создать контексты отрисовки (хглрк) для подготовки к просмотру на устройстве принтера. Если вы создаете контексты подготовки к просмотру перед вызовом **стартдок**, не существует способа определить, помещен ли в очередь метафайл.

В следующем примере кода показано, как напечатать изображение OpenGL:

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

Дополнительные сведения об использовании метафайлов см. в разделе [операции расширенного метафайла](/windows/desktop/gdi/enhanced-metafile-operations).

 

 