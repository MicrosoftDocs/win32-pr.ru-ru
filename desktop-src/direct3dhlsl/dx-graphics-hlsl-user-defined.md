---
title: Определяемый пользователем тип
description: Чтобы объявить определяемый пользователем тип, используйте следующий синтаксис.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee73cd5afcda15bcc821d7fea5b648924829d483a33b9c67c140eed0b100e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789314"
---
# <a name="user-defined-type"></a>Определяемый пользователем тип

Чтобы объявить определяемый пользователем тип, используйте следующий синтаксис.



|                                           |
|-------------------------------------------|
| typedef **\[ const \] имя типа \[ , \] индекс**; |



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                         | Описание                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[постоянного\]**<br/>                 | Необязательный элемент. Это ключевое слово явно помечает тип как константу.<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Тип**<br/>     | Определяет тип данных; должен быть одним из встроенных типов данных HLSL.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**<br/>     | Строка ASCII, однозначно определяющая имя переменной.<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Номер**<br/> | Необязательный размер массива. Значение должно быть целым числом без знака от 1 до 4 включительно.<br/> |



 

В дополнение к встроенным внутренним типам данных HLSL поддерживает определяемые пользователем или пользовательские типы, которые следуют этому синтаксису:

## <a name="remarks"></a>Remarks

В определяемых пользователем типах регистр символов не учитывается. Для удобства следующие типы автоматически определяются в области супер-Глобальная.


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



Знак решетки ( \# ) представляет собой целую цифру от 1 до 4.

Для совместимости с эффектами DirectX 8 следующие типы автоматически определяются в глобальной области.


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Типы данных (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





