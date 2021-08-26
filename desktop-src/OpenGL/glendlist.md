---
title: Функция Глендлист (GL. h)
description: Функции Глневлист и Глендлист создают или заменяют список отображений. | Функция Глендлист (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- Функция Глендлист OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad75f62b3b049f2244b6e701f69654d110c559b337c0d4bb72da75af93f954f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081524"
---
# <a name="glendlist-function"></a>Функция Глендлист

Функции [**глневлист**](glnewlist.md) и **глендлист** создают или заменяют список отображений.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.



| Имя                                                                                                  | Значение                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Недопустимая \_ Операция GL**</dt> </dl> | **глендлист** был вызван без предшествующего **глневлист** или если **глневлист** был вызван во время определения списка отображений.<br/> |



## <a name="remarks"></a>Remarks

Списки отображений — это группы команд OpenGL, которые были сохранены для последующего выполнения. Списки отображений создаются с помощью [**глневлист**](glnewlist.md). Все последующие команды помещаются в список просмотра в заданном порядке до вызова **глендлист** .

Функция [**глневлист**](glnewlist.md) имеет два параметра. Первый параметр, *List*, представляет собой положительное целое число, которое становится уникальным именем для списка отображений. Имена могут быть созданы и зарезервированы с помощью [**глженлистс**](glgenlists.md) и проверены на уникальность с помощью [**глислист**](glislist.md). Второй параметр *mode*— это символьная константа, которая может принимать одно из двух приведенных выше значений.

Некоторые команды не компилируются в список просмотра, но выполняются немедленно, независимо от режима просмотра списка. Эти команды являются [**глколорпоинтер**](glcolorpointer.md), [**глделетелистс**](gldeletelists.md), [**глдисаблеклиентстате**](gldisableclientstate.md), [**гледжефлагпоинтер**](gledgeflagpointer.md), [**гленаблеклиентстате**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList,**](glislist.md), [**glNormalPointer**](glpopclientattrib.md), [**glPopClientAttrib**](glpixelstore-functions.md), [**glPixelStore**](glpushclientattrib.md), [**glPushClientAttrib**](glreadpixels.md), [**glReadPixels**](glrendermode.md), [**glRenderMode**](glselectbuffer.md), [**glSelectBuffer**](gltexcoordpointer.md), [**glTexCoordPointer**](glvertexpointer.md)и все подпрограммы [**glVertexPointer**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . [](glnormalpointer.md)

Аналогичным образом, [**glTexImage2D**](glteximage2d.md) и [**glTexImage1D**](glteximage1d.md) выполняются немедленно и не компилируются в список вывода, если их первый аргумент имеет \_ значение \_ 2D-текстура \_ двухмерной текстуры или плоская \_ текстура прокси-сервера GL \_ \_ , соответственно.

При обнаружении функции **глендлист** определение списка отображается с помощью *сопоставления списка с уникальным именем (* указанным в команде [**глневлист**](glnewlist.md) ). Если *список просмотра с именем уже* существует, он заменяется только при вызове **глендлист** .

Функции [**глкалллист**](glcalllist.md) и [**глкалллистс**](glcalllists.md) можно указать в списках вывода. Команды в списке отображаемых списков или списках, выполняемых **глкалллист** или **глкалллистс** , не включаются в создаваемый список просмотра, даже если в качестве режима создания списка используется значение GL \_ Compile \_ и \_ EXECUTE.

Следующая функция получает сведения, связанные с [**глневлист**](glnewlist.md):

[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Библиотека<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**глбегин**](glbegin.md)
</dt> <dt>

[**глкалллист**](glcalllist.md)
</dt> <dt>

[**глкалллистс**](glcalllists.md)
</dt> <dt>

[**глделетелистс**](gldeletelists.md)
</dt> <dt>

[**гленд**](glend.md)
</dt> <dt>

[**глженлистс**](glgenlists.md)
</dt> <dt>

[**глислист**](glislist.md)
</dt> <dt>

[**глневлист**](glnewlist.md)
</dt> </dl>

 

 





