---
description: 'Метод «Показать» показывает или скрывает диалоговое окно. Этот метод реализует метод Ипропертипаже:: демонстрации.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Метод Кбасепропертипаже. показывать (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668937"
---
# <a name="cbasepropertypageshow-method"></a>Кбасепропертипаже. отобразить метод

`Show`Метод показывает или скрывает диалоговое окно. Этот метод реализует метод [ипропертипаже:: демонстрации](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="syntax"></a>Синтаксис

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a>Параметры

*нкмдшов*

Тип: **[uint](../winprog/windows-data-types.md)**

Значение, указывающее, следует ли отображать или скрывать окно. Дополнительные сведения см. в описании метода [ипропертипаже:: Показать](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.

| Код возврата                                                                                  | Описание                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Успешно.<br/>            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый аргумент.<br/>   |
| <dl> <dt>**\_непредвиденная E**</dt> </dl> | Непредвиденный сбой.<br/> |

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |

## <a name="see-also"></a>См. также раздел

[Класс Кбасепропертипаже](cbasepropertypage.md)
