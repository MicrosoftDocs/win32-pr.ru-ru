---
description: задает оптимальные параметры качества визуального элемента, используемые для кодировщика расширенного профиля Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Свойство MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e140a854999a5c634620d98958e40832acbe9439
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471730"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>МФПКЭЙ \_ компрессионоптимизатионтипе, свойство

задает оптимальные параметры качества визуального элемента, используемые для кодировщика расширенного профиля Windows Media Video 9.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвккомпрессионоптимизатионтипе

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="remarks"></a>Комментарии

Это свойство предоставляет быстрый способ настройки ряда параметров кодирования видео. Для него может быть задано одно из следующих значений.




| Значение | Описание | 
|-------|-------------|
| 0 | Кодек не будет выполнять принудительную оптимизацию и будет использовать все функции, заданные другими свойствами. Во многих случаях кодек будет использовать внутреннюю логику для определения параметров, если они не указаны. Это значение по умолчанию. | 
| 1 | Включает функции, которые обеспечивают наилучшее качество визуального элемента. При использовании этого значения кодек настраивается так, как если бы были заданы следующие свойства:<br /><ul><li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li><li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li><li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li><li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li><li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li><li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li><li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li></ul>Если задать любое из свойств в приведенном выше списке, заданное значение переопределит значения, связанные с этим параметром, за исключением <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br /> | 




 

Установка для свойства МФПКЭЙ компрессионоптимизатионтипе значения \_ 1 также влияет на установку параметра реестра дкуант в значение 2, а параметру реестра для метода стоимости вектора движения — значение 1. дополнительные сведения см. в статье [использование расширенного Windows Параметры видеокодека расширенного профиля Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




