---
description: Метод получения \_ фильтра получает указатель на фильтр источника, который сейчас используется средством обнаружения мультимедиа.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Метод Имедиадет:: get_Filter (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679712"
---
# <a name="imediadetget_filter-method"></a>Метод фильтра Имедиадет:: Get \_

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_Filter`Метод получает указатель на фильтр источника, который сейчас используется средством обнаружения мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппвал* \[ out, retval\]
</dt> <dd>

Получает указатель на интерфейс **IUnknown** фильтра. Если фильтр источника не используется, устанавливается значение **null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Если метод возвращает значение, если *\* ппвал* не равен **null**, то интерфейс **IUnknown** имеет необработанный счетчик ссылок. Освободите интерфейс по окончании его использования.

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

[**Интерфейс Имедиадет**](imediadet.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




