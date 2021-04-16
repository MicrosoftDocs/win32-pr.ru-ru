---
description: Метод Чекквидеотипе проверяет, совместим ли указанный формат ВИДЕОИНФО с форматом вывода.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Цимажедисплай. Чекквидеотипе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657817"
---
# <a name="cimagedisplaycheckvideotype-method"></a>Цимажедисплай. Чекквидеотипе, метод

`CheckVideoType`Метод проверяет, совместим ли указанный формат [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) с форматом вывода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинпут* 
</dt> <dd>

Указатель на структуру **видеоинфо** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ , если формат совместим, или E \_ INVALIDARG в противном случае.

## <a name="remarks"></a>Комментарии

Этот метод возвращает значение \_ ОК, если предложенный тип можно легко отобразить в текущих параметрах отображения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




