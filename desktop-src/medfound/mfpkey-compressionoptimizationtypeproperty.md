---
description: задает оптимальные параметры качества визуального элемента, используемые для кодировщика расширенного профиля Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Свойство MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7171990280fe004b12c306a09af3b617ba2de0a7cfa274edb3d9191b16a886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242883"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>МФПКЭЙ \_ компрессионоптимизатионтипе, свойство

задает оптимальные параметры качества визуального элемента, используемые для кодировщика расширенного профиля Windows Media Video 9.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвккомпрессионоптимизатионтипе

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="remarks"></a>Remarks

Это свойство предоставляет быстрый способ настройки ряда параметров кодирования видео. Для него может быть задано одно из следующих значений.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Кодек не будет выполнять принудительную оптимизацию и будет использовать все функции, заданные другими свойствами. Во многих случаях кодек будет использовать внутреннюю логику для определения параметров, если они не указаны. Это значение по умолчанию.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Включает функции, которые обеспечивают наилучшее качество визуального элемента. При использовании этого значения кодек настраивается так, как если бы были заданы следующие свойства:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Если задать любое из свойств в приведенном выше списке, заданное значение переопределит значения, связанные с этим параметром, за исключением <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
</tbody>
</table>



 

Установка для свойства МФПКЭЙ компрессионоптимизатионтипе значения \_ 1 также влияет на установку параметра реестра дкуант в значение 2, а параметру реестра для метода стоимости вектора движения — значение 1. дополнительные сведения см. в статье [использование расширенного Windows Параметры видеокодека расширенного профиля Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




