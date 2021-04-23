---
description: Определяет кадр координат или &\# 0034; кадр ссылки. &\# 0034; Шаблон фрейма открыт и может содержать любой объект. Функции загрузки сетки D3DX распознают экземпляры шаблонов сетки, Фраметрансформматрикс и фреймов как дочерние объекты при загрузке экземпляра Frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Рамка (графика Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894321"
---
# <a name="frame-direct3d-9-graphics"></a><span data-ttu-id="a5cf5-104">Рамка (графика Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5cf5-104">Frame (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="a5cf5-105">Определяет кадр координат или "кадр ссылки".</span><span class="sxs-lookup"><span data-stu-id="a5cf5-105">Defines a coordinate frame, or "frame of reference."</span></span> <span data-ttu-id="a5cf5-106">Шаблон фрейма открыт и может содержать любой объект.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-106">The Frame template is open and can contain any object.</span></span> <span data-ttu-id="a5cf5-107">Функции загрузки сетки D3DX распознают экземпляры шаблонов [**сетки**](mesh.md), [**фраметрансформматрикс**](frametransformmatrix.md)и **фреймов** как дочерние объекты при загрузке экземпляра **Frame** .</span><span class="sxs-lookup"><span data-stu-id="a5cf5-107">The D3DX mesh-loading functions recognize [**Mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md), and **Frame** template instances as child objects when loading a **Frame** instance.</span></span>

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

<span data-ttu-id="a5cf5-108">Шаблон Frame распознает дочерние **фреймы** и узлы [**сетки**](mesh.md) внутри фрейма и может распознать определяемые пользователем шаблоны с помощью функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-108">The frame template recognizes child **Frame** and [**Mesh**](mesh.md) nodes inside a frame and can recognize user-defined templates through a callback function.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5cf5-109">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5cf5-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5cf5-110">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="a5cf5-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



