---
title: Функция glTexCoord1iv (GL. h)
description: Задает текущие координаты текстуры. | Функция glTexCoord1iv (GL. h)
ms.assetid: 88d35f55-01a5-492d-9d6c-21ee0ce7bfa3
keywords:
- Функция glTexCoord1iv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord1iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 317b8d9168e9b3c7fe22adc7aae728e6cd3bdc3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674609"
---
# <a name="gltexcoord1iv-function"></a>Функция glTexCoord1iv

Задает текущие координаты текстуры.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glTexCoord1iv(
   const GLint *v
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*3,3* 
</dt> <dd>

Указатель на массив координат текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Функция [**глтекскурд**](gltexcoord-functions.md) задает текущие координаты текстуры, которые являются частью данных, связанных с вершинами многоугольников. Функция **глтекскурд** задает координаты текстуры в одном, двух, трех или четырех измерениях. Функция glTexCoord1 устанавливает для текущих координат текстуры значение (s, 0, 0, 1); вызов glTexCoord2 задает для них значение (s, t, 0, 1). Аналогичным образом glTexCoord3 определяет координаты текстуры как (s, t, r, 1), а glTexCoord4 определяет все четыре компонента явным образом (s, t, r, q). Текущие координаты текстуры можно обновить в любое время. В частности, можно вызвать Глтекскурд между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md). Следующая функция получает сведения, связанные с **глтекскурд**:

[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в качестве \_ \_ координат текущей текстуры главной книги \_

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Библиотека<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[глвертекс](glvertex-functions.md)
</dt> </dl>

 

 





