---
description: Константы шейдера вершин. Эти константы используются членом VS20Caps объекта D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342949"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

Константы шейдера вершин. Эти константы используются членом VS20Caps объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).



| \#определенно                              | Значение          | Описание                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVS20CAPS \_ затенения              | (1 << 0) | Инструкция затенения поддерживается. См. раздел [сетп \_ comp-VS](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ Max \_ динамикфловконтролдепс | 24             | Максимальный уровень вложенности инструкций динамического управления потоками ([break-VS](../direct3dhlsl/break---vs.md)и [break \_ -VS](../direct3dhlsl/break-comp---vs.md), [бреакп-VS](../direct3dhlsl/breakp---vs.md), [Если \_ comp-](../direct3dhlsl/if-comp---vs.md)VS, if-VS, если \_ " [пред](../direct3dhlsl/if-pred---vs.md)-VS"). |
| D3DVS20 \_ min \_ динамикфловконтролдепс | 0              | Минимальный уровень вложенности инструкций динамического управления потоками ([break-VS](../direct3dhlsl/break---vs.md)и [break \_ -VS](../direct3dhlsl/break-comp---vs.md), [бреакп-VS](../direct3dhlsl/breakp---vs.md), [Если \_ comp-](../direct3dhlsl/if-comp---vs.md)VS, if-VS, если \_ " [пред](../direct3dhlsl/if-pred---vs.md)-VS"). |
| D3DVS20 \_ Max \_ нумтемпс                | 32             | Максимальное число поддерживаемых временных регистров.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ min \_ нумтемпс                | 12             | Поддерживаемое минимальное количество временных регистров.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Max \_ статикфловконтролдепс  | 4              | Максимальная глубина вложенности инструкций « [цикл](../direct3dhlsl/loop---vs.md)-представителя-VS / [»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».                                                                                           |
| D3DVS20 \_ min \_ статикфловконтролдепс  | 1              | Минимальная глубина вложенности инструкций «цикл- [](../direct3dhlsl/loop---vs.md) / [представителя-VS»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».                                                                                           |



 

## <a name="constant-information"></a>Сведения о константе



| Требование                         | Значение           |
|--------------------------|------------|
| Заголовок                   | d3d9caps. h |
| Минимальная операционная система | Windows 98 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
