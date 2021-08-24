---
title: Функция Глуеррорстринг (GLU. h)
description: Функция Глуеррорстринг выдает строку ошибки из кода ошибки OpenGL или GLU. Строка ошибки — только ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- Функция Глуеррорстринг OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beef90cfced2b33b612e15c1ef6918de81997520483acfb141f3a307ad64096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777654"
---
# <a name="gluerrorstring-function"></a>Функция Глуеррорстринг

Функция **глуеррорстринг** выдает строку ошибки из кода ошибки OpenGL или Glu. Строка ошибки — только ANSI.

## <a name="syntax"></a>Синтаксис


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ерркоде* 
</dt> <dd>

Код ошибки OpenGL или GLU.

</dd> </dl>

## <a name="remarks"></a>Remarks

Функция **глуеррорстринг** выдает строку ошибки из кода ошибки OpenGL или Glu. Строка имеет формат ISO Latin 1. Например, **глуеррорстринг**( \_ \_ \_ неиспользуемая память GL) возвращает строку "недостаточно памяти".

Стандартные коды ошибок GLU — GLU \_ недопустимое \_ перечисление, Glu \_ недопустимое \_ значение и Glu \_ нехватки \_ \_ памяти. Некоторые другие функции GLU могут возвращать специализированные коды ошибок с помощью обратных вызовов. Список кодов ошибок OpenGL см. в разделе [**глжетеррор**](glgeterror.md).

Функция **глуеррорстринг** создает строки ошибок только в ANSI. Везде, где это возможно, используйте **глуеррорстрингвин**, что позволяет использовать строки ошибок ANSI или Unicode. Это упрощает локализацию программы для использования с другим языком.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**глжетеррор**](glgeterror.md)
</dt> <dt>

[*глунурбскаллбакк*](glunurbs.md)
</dt> <dt>

[*глукуадриккаллбакк*](gluquadric.md)
</dt> <dt>

[*глутесскаллбакк*](glutess.md)
</dt> </dl>

 

 





