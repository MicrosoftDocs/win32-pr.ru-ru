---
description: Метод Уопвалид извлекает значение, указывающее, является ли указанная пользовательская операция (УОП) в настоящее время допустимой.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Метод Уопвалид (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685343"
---
# <a name="uopvalid-method"></a>Метод Уопвалид

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`UOPValid`Метод получает значение, указывающее, допустима ли в настоящее время указанная пользовательская операция (УОП).

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*иуоп*
</dt> <dd>

Задает пользовательскую операцию (УОП) в виде целого числа.



| Значение | Описание                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**Плайтитле**](playtitle-method.md), [**плайаттиме**](playattime-method.md)[**плайаттимеинтитле**](playattimeintitle-method.md)                                                                                      |
| 1     | [**плайчаптер**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**плайтитле**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Stop**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ретурнфромсубмену**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**плайчаптер**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**Плайпревчаптер**](playprevchapter-method.md), [ **реплайчаптер**](replaychapter-method.md)                                                                                                                         |
| 7     | [**плайнекстчаптер**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**плайфорвардс**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**плайбакквардс**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**Шовмену**](showmenu-method.md) со значением параметра 2 ( \_ Название меню DVD \_ )                                                                                                                                       |
| 11    | [**Шовмену**](showmenu-method.md) со значением параметра 3 ( \_ корень меню DVD \_ )                                                                                                                                        |
| 12    | [**Шовмену**](showmenu-method.md) со значением параметра 4 ( \_ \_ подизображением меню DVD)                                                                                                                                  |
| 13    | [**Шовмену**](showmenu-method.md) со значением параметра 5 ( \_ аудио меню DVD \_ )                                                                                                                                       |
| 14    | [**Шовмену**](showmenu-method.md) со значением параметра 6 ( \_ угол меню DVD \_ )                                                                                                                                       |
| 15    | [**Шовмену**](showmenu-method.md) со значением параметра 7 ( \_ глава меню DVD \_ )                                                                                                                                     |
| 16    | [**Возобновить**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**Селектлефтбуттон**](selectleftbutton-method.md), [**селектригхтбуттон**](selectrightbutton-method.md), [**селектуппербуттон**](selectupperbutton-method.md), [**селектловербуттон**](selectlowerbutton-method.md) |
| 18    | [**стиллофф**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Пауза**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**куррентаудиостреам**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**куррентсубпиктурестреам**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**Куррентангле**](currentangle-property.md), [ **селектпаренталлевел**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**караокеаудиопресентатионмоде**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Выберите параметр видеорежим.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает логическое значение, указывающее, разрешена ли указанная операция элементом управления УОП.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Сегмент. h</dt> </dl> |



 

 




