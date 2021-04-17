---
title: Метод Ивмдрмевентженератор Канцеласинкоператион (Вмдрмсдк. h)
description: Метод Канцеласинкоператион отменяет асинхронную операцию.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Формат Windows Media, Канцеласинкоператион метод
- Канцеласинкоператион метод Windows Media Format, интерфейс Ивмдрмевентженератор
- Интерфейс Ивмдрмевентженератор Windows Media Format, метод Канцеласинкоператион
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657373"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>Метод Ивмдрмевентженератор:: Канцеласинкоператион

Метод **канцеласинкоператион** отменяет асинхронную операцию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пункканцелатионкукие* \[ окне\]
</dt> <dd>

Указатель на файл cookie отмены, определяющий асинхронную операцию, которая должна быть отменена. Этот файл cookie предоставляется методом, используемым для запуска операции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмевентженератор**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





