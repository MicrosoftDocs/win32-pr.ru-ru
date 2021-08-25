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
ms.openlocfilehash: 12e15b297f78b3386ae9ad31e749858bad14b87e59e938ac02a3cf3a9ca002a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872334"
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



 

## <a name="remarks"></a>Remarks

Фильтр делегирует все команды поиска объекту [**крендерерпоспасссру**](crendererpospassthru.md) , который передает их восходящий поток. Этот метод создает объект **крендерерпоспасссру** , если он еще не существует, и запрашивает его для запрошенного интерфейса.

В переменной-члене [**кбасерендерер:: m \_ ппоситион**](cbaserenderer-m-pposition.md) хранится указатель на объект **крендерерпоспасссру** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




