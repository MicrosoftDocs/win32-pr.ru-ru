---
description: Метод Get \_ Size возвращает текущий размер выходных данных и режим Stretch.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Метод Иресизе:: get_Size (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 747ca8d7fd839321a9dbf4403c503652b932403e49bb964ae6148da2f49c5ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818215"
---
# <a name="iresizeget_size-method"></a>Метод Иресизе:: Get \_ size

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_Size`Метод возвращает текущий размер выходных данных и режим Stretch.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пихеигхт* \[ заполняет\]
</dt> <dd>

Получает высоту видео в пикселях.

</dd> <dt>

*пивидс* \[ заполняет\]
</dt> <dd>

Получает ширину видео в пикселях.

</dd> <dt>

*пфлаг* \[ заполняет\]
</dt> <dd>

Получает флаг, задающий режим растяжения. Возможные значения см. в разделе [**изменение размера флагов**](resize-flags.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если тип выходных данных не задан, фильтр должен вернуть значения по умолчанию. Эти значения можно произвольно выбрать во время разработки.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | DirectX 9,0 или более поздней версии<br/>                                                         |
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> <dt>

[**Интерфейс Иресизе**](iresize.md)
</dt> </dl>

 

 




