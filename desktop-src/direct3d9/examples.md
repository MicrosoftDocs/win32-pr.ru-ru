---
description: Далее следуют два примера определений двоичных шаблонов и пример двоичного объекта данных.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Примеры (графика Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8b8e2a9c500042e9b8d7c7fd911ab74b2f428d1ef814aca9e5fda1be7dcab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523101"
---
# <a name="examples-direct3d-9-graphics"></a>Примеры (графика Direct3D 9)

Далее следуют два примера определений двоичных шаблонов и пример двоичного объекта данных.

> [!Note]  
> Данные хранятся в формате с прямым порядком байтов, который не показан в этих примерах.

 

Закрытый шаблон RGB определяется UUID {55b6d780-37ec-11D0-ab39-0020af71e433} и имеет три элемента: r, g и b-each типа float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



Закрытый шаблон Matrix4x4 идентифицируется с помощью UUID {55b6d781-37ec-11D0-ab39-0020af71e433} и имеет один элемент — двухмерный массив с именем матрица типа float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



В приведенном ниже объекте двоичных данных показан экземпляр шаблона RGB, определенный ранее. Пример объекта имеет имя Blue, а его три элемента — r, g и b — имеют значения 0,0, 0,0 и 1,0 соответственно.


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Двоичное кодирование](binary-encoding.md)
</dt> </dl>

 

 



