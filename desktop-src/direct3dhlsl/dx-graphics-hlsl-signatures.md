---
title: Сигнатуры
description: Сигнатура шейдера — это список параметров, которые либо являются входными, либо выводяти из функции шейдера.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996795"
---
# <a name="signatures"></a>Сигнатуры

Сигнатура шейдера — это список параметров, которые либо являются входными, либо выводяти из функции шейдера. В Direct3D 10 смежные этапы эффективно совместно используют массив регистров, где шейдер выходных данных (или стадия конвейера) записывает данные в определенные места в массиве Register, и входной шейдер должен считываться из тех же расположений. API использует подписи шейдера для привязки выходных данных шейдера с входными данными без издержек семантического разрешения.

В Direct3D 10 входные подписи формируются из объявления ввода шейдера, а выходная подпись формируется из объявления вывода шейдера. Говорят, что входная сигнатура совместима с выходной сигнатурой, когда выходная подпись является строго подмножеством (типом аргумента и порядком совпадений) входной сигнатуры. Самый простой способ добиться этого — связать соответствующие входные и выходные данные шейдера с тем же типом структуры.

Ниже приведен пример совместимых подписей.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



Ниже приведен пример несовместимых подписей. порядок параметров во входной подписи не соответствует порядку в выходной подписи.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



Псинворкс является совместимым подмножеством Всаут (первые две записи соответствуют типу и порядку с первыми двумя записями в Всаут). Однако Псинфаилс несовместима, так как порядок не соответствует Всаут.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




