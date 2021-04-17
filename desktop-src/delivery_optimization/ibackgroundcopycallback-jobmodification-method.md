---
title: Метод Ибаккграундкопикаллбакк Жобмодификатион (Deliveryoptimization. h)
description: Оптимизация доставки (DO) вызывает реализацию метода Жобмодификатион, когда задание было изменено.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Метод Жобмодификатион
- Метод Жобмодификатион, интерфейс Ибаккграундкопикаллбакк
- Интерфейс Ибаккграундкопикаллбакк, метод Жобмодификатион
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710482"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>Метод Ибаккграундкопикаллбакк:: Жобмодификатион

Оптимизация доставки (DO) вызывает реализацию метода [**жобмодификатион**](https://www.bing.com/search?q=**JobModification**) , когда задание было изменено. Служба создает это событие, когда передаются байты, в задание добавляются файлы, свойства были изменены или изменилось состояние задания.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пжоб* \[ окне\]
</dt> <dd>

Содержит методы для доступа к сведениям о свойстве, ходе выполнения и состоянии задания. Не освобождайте *пжоб*; Выпускайте интерфейс, когда метод [**жобмодификатион**](https://www.bing.com/search?q=**JobModification**) возвращает значение.

</dd> <dt>

*двресервед* \[ окне\]
</dt> <dd>

Зарезервировано для последующего использования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод должен возвращать S_OK.

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
</dt> </dl>

 

 





