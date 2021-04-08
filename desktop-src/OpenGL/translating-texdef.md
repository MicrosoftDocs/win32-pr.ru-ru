---
title: Преобразование тексдеф
description: Следующий пример кода является определением текстуры ДИАФРАГМы в ГК
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Перенос GL по IRI, текстура
- Перенос из ДИАФРАГМы в ГК, текстура
- Перенос на OpenGL из IRI GL, текстура
- Перенос по стандарту OpenGL из IRI GL, текстура
- текстура
- Перенос GL в ГК, тексдеф
- Перенос из IRI GL, тексдеф
- перенос в OpenGL из IRI GL, тексдеф
- Перенос по стандарту OpenGL из IRI GL, тексдеф
- тексдеф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889047"
---
# <a name="translating-texdef"></a>Преобразование тексдеф

В следующем примере кода демонстрируется определение текстуры ДИАФРАГМы в ГК:


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



В предыдущем примере **тексдеф** указывает фильтр точек TX как как увеличение, так и как \_ Фильтр минимизации, а TX \_ Repeat — как механизм упаковки. Он также указывает изображение текстуры: **Granite \_ текстура**.

В OpenGL [**глтексимаже**](glteximage1d.md) указывает образ, а [глтекспараметер](gltexparameter-functions.md) задает свойство. Для преобразования определений текстур IRI GL замените функцию **текстдеф** на **глтексимаже** и один или несколько вызовов **глтекспараметер**.

Предыдущий код IRI GL выглядит следующим образом при переводе в OpenGL:


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



В следующей таблице перечислены параметры текстуры диафрагмы IRI и их эквивалентные параметры OpenGL.



| Параметр текстуры IRI GL | Параметр текстуры OpenGL                                  |
|---------------------------|-----------------------------------------------------------|
| \_МИНФИЛТЕР TX             | \_ \_ Фильтр min текстуры \_ GL                                  |
| \_МАГФИЛТЕР TX             | \_ \_ Фильтр MAG текстуры \_ GL                                  |
| \_Перенос переноса, передача \_ переносов по словам \_ S     | \_Перенос текстуры в ГК \_ \_                                      |
| \_Перенос переноса, передача по \_ словам \_ T     | \_текстура GL — \_ Перенос \_ \_ \_ цвета границы текстуры тгл \_<br/> |



 

В следующей таблице перечислены возможные значения параметров текстуры диафрагмы IRI и их эквивалентные параметры OpenGL.



| Параметр текстуры IRI GL | Параметр текстуры OpenGL     |
|---------------------------|------------------------------|
| \_точка передачи                 | \_Ближайшая к GL                  |
| \_БИЛИНЕЙНОЙ TX              | Линейная (GL) \_                   |
| \_точка mipmap \_ TX         | Ближайшая к GL Ближайшая \_ \_ mipmap \_ |
| TX \_ mipmap \_ билинейной      | \_Линейная \_ MIPMAPа GL \_  |
| \_ \_ Линейная mipmap TX        | \_Ближайшая \_ Линейная MIPMAPа GL \_  |
| \_ТРИЛИНЕЙНОЙ TX             | линейное \_ \_ MIPMAPе GL \_   |



 

 

 





