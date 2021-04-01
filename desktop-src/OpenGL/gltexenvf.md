---
title: Функция Глтексенвф (GL. h)
description: Функция Глтексенвф задает параметр среды текстуры.
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- Функция Глтексенвф OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1566378b6dcd2f91a2e2cd445f0ec39c0f6f6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801996"
---
# <a name="gltexenvf-function"></a>Функция Глтексенвф

Функция **глтексенвф** задает параметр среды текстуры.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*target* 
</dt> <dd>

Среда текстуры. Должна быть текстура GL в виде \_ \_ env.

</dd> <dt>

*pname* 
</dt> <dd>

Символьное имя однозначного параметра среды текстуры. Необходимо использовать \_ режим GL текстуры \_ env \_ .

</dd> <dt>

*param* 
</dt> <dd>

Одна символьная константа, одна из них: GL, GL \_ \_ ДЕКАЛ, GL \_ Blend или GL \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.



| Имя                                                                                                  | Значение                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_недействительное \_ перечисление GL**</dt> </dl>      | *Target* или *pname* не является одним из принятых значений, или если *Параметры* должны иметь определенное константное значение (на основе значения *pname*) и не было.<br/> |
| <dl> <dt>**\_Недопустимая \_ Операция GL**</dt> </dl> | Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).<br/>                                             |



## <a name="remarks"></a>Комментарии

В среде текстуры указывается способ интерпретации значений текстур при текстурировании фрагмента. *Целевой* параметр должен иметь значение GL \_ текстуры \_ env. Параметр *pname* имеет режим GL \_ текстуры \_ env \_ . Определены три функции текстуры: GL для \_ модуляции, GL \_ ДЕКАЛ и GL \_ Blend.

Функция текстуры работает с фрагментом, используя значение изображения текстуры, которое применяется к фрагменту (см. [**глтекспараметер**](gltexparameter-functions.md)) и создает для этого фрагмента цвет RGBA. В следующей таблице показано, как создается цвет RGBA для каждой из трех функций текстуры, которые можно выбрать. *C* — это тройной цвет значений (RGB), *а —* связанное альфа-значение. Значения RGBA, извлеченные из изображения текстуры, находятся в диапазоне \[ 0, 1 \] . Индекс *f* относится к входящему фрагменту, индексу *t* к изображению текстуры, индексу *c* на цветовую среду текстуры, а индекс *v* — значению, созданному функцией текстуры.

Изображение текстуры может содержать до четырех компонентов на элемент текстуры (см. раздел [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)). В образе с одним компонентом lt указывает на один компонент. В образе с двумя компонентами используется *L?*  и *?* . Изображение из трех компонентов имеет только значение цвета, *C?* . Образ из четырех компонентов имеет значение цвета *C?*  и альфа-значение *A?* .



<table>
<thead>
<tr class="header">
<th>Число компонентов</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">1 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">не определено $ {Remove} $<br />
</td>
<td><em>C</em> <em><sub>v</sub></em>  =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">не определено $ {Remove} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em></td>
<td rowspan="2">не определено $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1- <em>A?</em> <em>) C<sub>f</sub> </em> + <em>A?</em> <em>Ц?</em></td>
<td rowspan="2">не определено $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>А?</em> <em>A<sub>f</sub></em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

\_Режим текстуры в GL \_ \_ по умолчанию имеет значение GL \_ модуляции.

Следующая функция получает сведения, связанные с **глтексенвф**:

[**глтексжетенвфв**](glgettexenvfv.md)

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

[**глбегин**](glbegin.md)
</dt> <dt>

[**гленд**](glend.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**глтекспараметер**](gltexparameter-functions.md)
</dt> </dl>

 

 





