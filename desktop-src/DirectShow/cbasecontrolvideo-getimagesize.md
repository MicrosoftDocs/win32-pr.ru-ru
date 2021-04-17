---
description: Метод Жетимажесизе извлекает сведения о размере изображения видео.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Кбасеконтролвидео. Жетимажесизе, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689521"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>Кбасеконтролвидео. Жетимажесизе, метод

`GetImageSize`Метод получает сведения о размере изображения видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвидеоинфо* 
</dt> <dd>

Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) для заполнения.

</dd> <dt>

*пбуфферсизе* 
</dt> <dd>

Указатель на размер буфера видео.

</dd> <dt>

*псаурцерект* 
</dt> <dd>

Указатель на размеры прямоугольника исходного видео.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.



| Код возврата                                                                                  | Описание                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_Ошибка E**</dt> </dl>       | Ошибка.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый аргумент. Формат данных несовместим.<br/>           |
| <dl> <dt>**\_непредвиденная E**</dt> </dl> | Произошла непредвиденная ошибка. Один или несколько аргументов имеют **значение NULL**.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | Успешно.<br/>                                                       |



 

## <a name="remarks"></a>Комментарии

Эта функция-член является вспомогательной функцией, используемой для создания изображений изображений DIB. Он вызывается из реализации базового класса [**кбасеконтролвидео:: жеткуррентимаже**](cbasecontrolvideo-getcurrentimage.md) , когда в эту функцию-член передается параметр _пвидеоимаже_ **null**. В результате эта функция-член конструирует и возвращает структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , используя сведения в *пбуфферсизе* и *псаурцерект*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




