---
description: Методы курсора мыши позволяют приложению указывать цветовой курсор, предоставляя поверхность, которая содержит изображение.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Работа с курсорами мыши (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999bd324c8c3a1a2c743b5417f5d316a9d0f9493ccb4b749545e53e23e58917f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518922"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Работа с курсорами мыши (Direct3D 9)

Методы курсора мыши позволяют приложению указывать цветовой курсор, предоставляя поверхность, которая содержит изображение. Система гарантирует, что этот курсор будет обновляться с половиной скорости дисплея или более, если частота кадров приложения замедлена. Однако курсор никогда не будет обновляться чаще, чем частота обновления дисплея.

Расположение курсора мыши привязано к системному курсору, соответствующим образом масштабируется для режима пространственного разрешения экрана, но его можно напрямую переместить в приложении. Это аналогично поведению системного курсора мыши, поддерживаемого API Win32. Дополнительные сведения об использовании курсора мыши в приложении Direct3D см. в следующих справочных разделах.

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D гарантирует, что мышь поддерживается либо с помощью аппаратных реализаций, либо с помощью времени выполнения Direct3D, выполняющего блиттинг операции аппаратного ускорения при вызове [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)повторно.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Советы программирования](programming-tips.md)
</dt> </dl>

 

 
