---
description: Метод "получить \_ частоту кадров" получает скорость кадров текущего потока. Поток должен представлять собой поток видео.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Метод Имедиадет:: get_FrameRate (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a22be2caf5a66447c9c772861918f1a5dcfe7bc2c81bfdba4f1fefb59f89565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154430"
---
# <a name="imediadetget_framerate-method"></a>Метод Имедиадет:: Get \_ частоты кадров

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_FrameRate`Метод получает частоту кадров текущего потока. Поток должен представлять собой поток видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает частоту кадров в кадрах в секунду.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения:



| Код возврата                                                                                             | Описание                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                 | В заголовке формата видео не указана частота кадров.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>                    | Успешно.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Недопустимый аргумент.<br/>                                  |
| <dl> <dt>**\_указатель E**</dt> </dl>               | **Пустой** аргумент указателя.<br/>                         |
| <dl> <dt>**VFW \_ E \_ инвалидмедиатипе**</dt> </dl> | Недопустимый тип носителя.<br/>                                |



 

## <a name="remarks"></a>Remarks

Этот метод не может получить частоту кадров из ASF – файла.

Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).

Если средство обнаружения мультимедиа находится в режиме захвата растрового изображения, этот метод возвращает E \_ INVALIDARG. Дополнительные сведения см. в разделе [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md).

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Имедиадет**](imediadet.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




