---
title: Метод использованием метода ibackgroundcopyjob Жетнопрогресстимеаут (Deliveryoptimization. h)
description: Возвращает время, в течение которого служба пытается переместить файл после возникновения временной ошибки. Если происходит выполнение, таймер сбрасывается.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Метод Жетнопрогресстимеаут
- Метод Жетнопрогресстимеаут, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Жетнопрогресстимеаут
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490926"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a>Метод использованием метода ibackgroundcopyjob:: Жетнопрогресстимеаут

Возвращает время, в течение которого служба пытается переместить файл после возникновения временной ошибки. Если происходит выполнение, таймер сбрасывается.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*претрипериод* \[ окне\]
</dt> <dd>

Время в секундах, в течение которого служба пытается переместить файл после возникновения временной ошибки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                              | Описание                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Время ожидания было успешно получено.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Сетнопрогресстимеаут**](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





