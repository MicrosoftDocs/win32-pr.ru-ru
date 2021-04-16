---
description: Методы курсора мыши позволяют приложению указывать цветовой курсор, предоставляя поверхность, которая содержит изображение.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Работа с курсорами мыши (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495564"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Работа с курсорами мыши (Direct3D 9)

Методы курсора мыши позволяют приложению указывать цветовой курсор, предоставляя поверхность, которая содержит изображение. Система гарантирует, что этот курсор будет обновляться с половиной скорости дисплея или более, если частота кадров приложения замедлена. Однако курсор никогда не будет обновляться чаще, чем частота обновления дисплея.

Расположение курсора мыши привязано к системному курсору, соответствующим образом масштабируется для режима пространственного разрешения экрана, но его можно напрямую переместить в приложении. Это аналогично поведению системного курсора мыши, поддерживаемого API Win32. Дополнительные сведения об использовании курсора мыши в приложении Direct3D см. в следующих справочных разделах.

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D гарантирует, что мышь поддерживается либо с помощью аппаратных реализаций, либо с помощью времени выполнения Direct3D, выполняющего блиттинг операции аппаратного ускорения при вызове [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)повторно.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Советы по программированию](programming-tips.md)
</dt> </dl>

 

 
