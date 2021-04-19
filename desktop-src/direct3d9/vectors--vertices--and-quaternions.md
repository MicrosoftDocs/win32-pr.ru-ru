---
description: В Direct3D вершины описывают положение и ориентацию. Каждая вершина в примитиве описывается вектором, который сообщает ее положение, цвет, координаты текстуры, и вектором нормали, который позволяет узнать ее ориентацию.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Векторы, вершины и кватернион (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e6e6e316b633359205ffd24a64aa349eeec74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537025"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a>Векторы, вершины и кватернион (Direct3D 9)

В Direct3D вершины описывают положение и ориентацию. Каждая вершина в примитиве описывается вектором, который сообщает ее положение, цвет, координаты текстуры, и вектором нормали, который позволяет узнать ее ориентацию.

Кватернион добавляет четвертый элемент к \[ значениям x, y, z \] , которые определяют вектор с тремя компонентами. Кватернионы представляют собой альтернативу матричным методам, обычно используемым для 3D-вращения. Кватернион представляет ось в 3D-пространстве и поворот вокруг этой оси. Например, кватернион может представлять ось (1,1,2) и поворот на 1 радиан. Кватернионы содержат полезную информацию, однако их истинная ценность заключается в двух операциях, которые можно выполнять над ними: композиции и интерполяции.

Выполнение композиции над кватернионами аналогично их объединению. Записывается композиция двух кватернионов так, как показано на следующем рисунке.

![иллюстрация записи кватернионов](images/quateq.png)

Композиция двух кватернионов, применяемая к геометрии, означает "повернуть геометрию вокруг оси₂ на поворот₂, затем повернуть ее вокруг оси₁ на поворот₁". В данном случае Q представляет поворот вокруг одной оси, который является результатом применения q₂ и затем q₁ к геометрии.

С помощью интерполяции кватернионов приложение может рассчитать плавный и рациональный путь от одной оси и ориентации к другой. Таким образом, интерполяция между q₁ и q₂ — это простой способ анимировать движение от одной ориентации к другой.

При совместном использовании композиция и интерполяция дают возможность без труда манипулировать геометрией так, что манипуляции будут казаться сложными. Например, предположим, что у вас есть геометрия, которую вы хотите повернуть для придания ей определенной ориентации. Вам известно, что нужно повернуть ее на r₂ градусов вокруг оси₂, а затем на r₁ градусов вокруг оси₁, однако окончательный кватернион вам не известен. Используя композицию, вы можете объединить два поворота применительно к геометрии и получить один кватернион, который будет представлять собой результат. Затем можно выполнить интерполяцию из исходного кватерниона в составной для получения плавного перехода от одного к другому.

Библиотека служебной программы D3DX включает функции, помогающие работать с кватернион. Например, функция [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) добавляет значение вращения к вектору, который определяет ось вращения, и возвращает результат в кватернион, определенный структурой [**D3DXQUATERNION**](d3dxquaternion.md) . Кроме того, функция [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) формирует кватернионs, а [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) выполняет сферовую линейную интерполяцию между двумя кватерниона.

Приложения Direct3D могут использовать следующие функции, чтобы упростить задачу работы с кватерниона.

-   [**D3DXQuaternionBaryCentric**](d3dxquaternionbarycentric.md)
-   [**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
-   [**D3DXQuaternionDot**](d3dxquaterniondot.md)
-   [**D3DXQuaternionExp**](d3dxquaternionexp.md)
-   [**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
-   [**D3DXQuaternionInverse**](d3dxquaternioninverse.md)
-   [**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
-   [**D3DXQuaternionLength**](d3dxquaternionlength.md)
-   [**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
-   [**D3DXQuaternionLn**](d3dxquaternionln.md)
-   [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
-   [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
-   [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
-   [**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
-   [**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
-   [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md)
-   [**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
-   [**D3DXQuaternionToAxisAngle**](d3dxquaterniontoaxisangle.md)

Приложения Direct3D могут использовать следующие функции, чтобы упростить задачу работы с тремя компонентными векторами.

-   [**D3DXVec3Add**](d3dxvec3add.md)
-   [**D3DXVec3BaryCentric**](d3dxvec3barycentric.md)
-   [**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
-   [**D3DXVec3Cross**](d3dxvec3cross.md)
-   [**D3DXVec3Dot**](d3dxvec3dot.md)
-   [**D3DXVec3Hermite**](d3dxvec3hermite.md)
-   [**D3DXVec3Length**](d3dxvec3length.md)
-   [**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
-   [**D3DXVec3Lerp**](d3dxvec3lerp.md)
-   [**D3DXVec3Maximize**](d3dxvec3maximize.md)
-   [**D3DXVec3Minimize**](d3dxvec3minimize.md)
-   [**D3DXVec3Normalize**](d3dxvec3normalize.md)
-   [**D3DXVec3Project**](d3dxvec3project.md)
-   [**D3DXVec3Scale**](d3dxvec3scale.md)
-   [**D3DXVec3Subtract**](d3dxvec3subtract.md)
-   [**D3DXVec3Transform**](d3dxvec3transform.md)
-   [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md)
-   [**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
-   [**D3DXVec3Unproject**](d3dxvec3unproject.md)

Многие дополнительные функции, упрощающие задачи с использованием двух-и четырех компонентных векторов, включены в [математические функции](dx9-graphics-reference-d3dx-functions-math.md) , предоставляемые библиотекой служебной программы D3DX.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Системы координат и геометрия](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



