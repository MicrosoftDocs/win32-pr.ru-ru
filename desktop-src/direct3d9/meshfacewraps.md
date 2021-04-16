---
description: Используется для определения топологии текстуры каждой грани в оболочке. Значение элемента Нфацеврапвалуес должно быть равно числу граней в сети.
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: мешфацеврапс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ba55db3dc2c0733d66f5a9e4589937258324b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536515"
---
# <a name="meshfacewraps"></a><span data-ttu-id="244e7-104">мешфацеврапс</span><span class="sxs-lookup"><span data-stu-id="244e7-104">MeshFaceWraps</span></span>

<span data-ttu-id="244e7-105">Используется для определения топологии текстуры каждой грани в оболочке.</span><span class="sxs-lookup"><span data-stu-id="244e7-105">Used to define the texture topology of each face in a wrap.</span></span> <span data-ttu-id="244e7-106">Значение элемента Нфацеврапвалуес должно быть равно числу граней в сети.</span><span class="sxs-lookup"><span data-stu-id="244e7-106">The value of the nFaceWrapValues member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshFaceWraps
{
    < ED1EC5C0-C0A8-11D0-941C-0080C80CFA7B >
    DWORD nFaceWrapValues;
    array Boolean2d faceWrapValues[nFaceWrapValues];
} 
```

<span data-ttu-id="244e7-107">Этот шаблон больше не используется.</span><span class="sxs-lookup"><span data-stu-id="244e7-107">This template is no longer used.</span></span>

## <a name="see-also"></a><span data-ttu-id="244e7-108">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="244e7-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244e7-109">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="244e7-109">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



