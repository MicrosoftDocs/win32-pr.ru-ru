---
description: Метод Get \_ инпутсизе возвращает текущий размер входных данных фильтра изменения.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Метод Иресизе:: get_InputSize (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3b862237f8c51bdf6c22ca9acb667199fadee33b37e425efabfe25bdb8a20dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078934"
---
# <a name="iresizeget_inputsize-method"></a>Метод Иресизе:: Get \_ инпутсизе

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_InputSize`Метод возвращает текущий размер входных данных фильтра изменения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
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

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если входной ПИН-код фильтра не подключен, возвращается код ошибки. В противном случае верните ширину и высоту видео в соответствии с типом носителя входного контакта.

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

 

 




