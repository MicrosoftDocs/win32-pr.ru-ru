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
# <a name="frame-direct3d-9-graphics"></a>Рамка (графика Direct3D 9)

Определяет кадр координат или "кадр ссылки". Шаблон фрейма открыт и может содержать любой объект. Функции загрузки сетки D3DX распознают экземпляры шаблонов [**сетки**](mesh.md), [**фраметрансформматрикс**](frametransformmatrix.md)и **фреймов** как дочерние объекты при загрузке экземпляра **Frame** .

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

Шаблон Frame распознает дочерние **фреймы** и узлы [**сетки**](mesh.md) внутри фрейма и может распознать определяемые пользователем шаблоны с помощью функции обратного вызова.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



