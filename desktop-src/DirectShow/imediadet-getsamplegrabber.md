---
description: Метод Жетсамплеграббер извлекает указатель на интерфейс Исамплеграббер, который позволяет приложению получать отдельные выборки из потока мультимедиа.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'Метод Имедиадет:: Жетсамплеграббер (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675441"
---
# <a name="imediadetgetsamplegrabber-method"></a>Метод Имедиадет:: Жетсамплеграббер

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetSampleGrabber`Метод получает указатель на интерфейс [**исамплеграббер**](isamplegrabber.md) , который позволяет приложению получать отдельные выборки из потока мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппвал* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**исамплеграббер**](isamplegrabber.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода вызовите метод [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md) . Интерфейс [**исамплеграббер**](isamplegrabber.md) позволяет извлекать отдельные примеры мультимедиа из потока. Если требуется только точечный рисунок из видеокадра, вызовите вместо этого метод [**имедиадет:: жетбитмапбитс**](imediadet-getbitmapbits.md) . Интерфейс **исамплеграббер** является более гибким, но требует больше работы для приложения.

Если этот метод завершается успешно, интерфейс [**исамплеграббер**](isamplegrabber.md) , который он возвращает, имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

 

 




