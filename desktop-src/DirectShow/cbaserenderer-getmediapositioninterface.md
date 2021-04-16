---
description: Метод Жетмедиапоситионинтерфаце извлекает указатели интерфейса Имедиапоситион и Имедиасикинг фильтра.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Кбасерендерер. Жетмедиапоситионинтерфаце, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665301"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>Кбасерендерер. Жетмедиапоситионинтерфаце, метод

`GetMediaPositionInterface`Метод получает указатели интерфейса [**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) и [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) фильтра.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*riid* 
</dt> <dd>

Идентификатор ссылки интерфейса.

</dd> <dt>

*ппв* 
</dt> <dd>

Адрес переменной, получающей указатель интерфейса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                                   | Описание                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>     |
| <dl> <dt>**\_интерфейс E**</dt> </dl> | Интерфейс не поддерживается.<br/> |



 

## <a name="remarks"></a>Комментарии

Фильтр делегирует все команды поиска объекту [**крендерерпоспасссру**](crendererpospassthru.md) , который передает их восходящий поток. Этот метод создает объект **крендерерпоспасссру** , если он еще не существует, и запрашивает его для запрошенного интерфейса.

В переменной-члене [**кбасерендерер:: m \_ ппоситион**](cbaserenderer-m-pposition.md) хранится указатель на объект **крендерерпоспасссру** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




