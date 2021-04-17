---
description: Метод Сетдефаултфпс задает частоту кадров исходного объекта по умолчанию.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'Метод Иамтимелинесрк:: Сетдефаултфпс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675885"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a>Метод Иамтимелинесрк:: Сетдефаултфпс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetDefaultFPS`Метод задает частоту кадров исходного объекта по умолчанию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кадры в секунду* 
</dt> <dd>

Частота кадров по умолчанию в кадрах в секунду.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК в случае успеха или E \_ INVALIDARG, если указанная частота кадров меньше нуля.

## <a name="remarks"></a>Комментарии

Модуль подготовки отчетов использует это значение, если не может определить частоту кадров из исходного файла.

Вызывайте этот метод только для исходных файлов без стандартной частоты кадров. Для растровых и JPEG-файлов частота кадров по умолчанию равна нулю, что приводит к отображению источника в виде изображения по-прежнему. Чтобы использовать изображение в качестве первого кадра в последовательности DIB, задайте для параметра Частота кадров значение больше нуля. Дополнительные сведения см. в разделе [Работа с источниками](working-with-sources.md).

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелинесрк**](iamtimelinesrc.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




