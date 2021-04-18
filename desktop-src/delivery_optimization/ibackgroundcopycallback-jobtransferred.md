---
title: Метод Ибаккграундкопикаллбакк Жобтрансферред (Deliveryoptimization. h)
description: Оптимизация доставки (DO) вызывает реализацию метода Жобтрансферред, когда все файлы в задании были успешно переданы.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Метод Жобтрансферред
- Метод Жобтрансферред, интерфейс Ибаккграундкопикаллбакк
- Интерфейс Ибаккграундкопикаллбакк, метод Жобтрансферред
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135747"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>Метод Ибаккграундкопикаллбакк:: Жобтрансферред

Оптимизация доставки (DO) вызывает реализацию метода **жобтрансферред** , когда все файлы в задании были успешно переданы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пжоб* \[ окне\]
</dt> <dd>

Содержит сведения, связанные с заданиями, такие как время завершения задания, число переданных байтов и число переданных файлов. Не освобождайте *пжоб*; Выпускайте интерфейс, когда метод возвращает значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод должен возвращать S_OK.

## <a name="remarks"></a>Комментарии

Как правило, ваша реализация должна вызвать метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) , чтобы подтвердить, что файлы успешно переданы. Загружаемые файлы и файл ответов недоступны на клиенте до тех пор, пока не будет вызван **полный** метод.

Если не вызвать метод [**Complete**](ibackgroundcopyjob-complete.md) или метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) отменяет задание по истечении 30 дней и удаляет незавершенные файлы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback определен как 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





