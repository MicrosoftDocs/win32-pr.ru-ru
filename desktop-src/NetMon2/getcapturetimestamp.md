---
description: Функция Жеткаптуретиместамп возвращает дату и время начала записи кадров записью.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Функция Жеткаптуретиместамп (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 93ae1c94a5e83d0029aba4403ad4ba23db0f4006bb5b9be68cc469939e63c734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366639"
---
# <a name="getcapturetimestamp-function"></a>Функция Жеткаптуретиместамп

Функция **жеткаптуретиместамп** возвращает дату и время начала записи кадров записью.

## <a name="syntax"></a>Синтаксис


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хкаптуре* \[ окне\]
</dt> <dd>

Обработчик для записи. Дополнительные сведения о получении маркера записи см. в подразделе "Примечания" этой статьи **жеткаптуретиместамп** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на структуру [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="remarks"></a>Remarks

Функция **жеткаптуретиместамп** Возвращает время, когда поставщик сетевых пакетов (НПП) начинает сбор данных, а не когда эксперт загружает запись для анализа.

Не перезаписывайте данные в структуре **SYSTEMTIME** . Данные являются частью записи. Попытка изменить данные приведет к нарушению прав доступа.

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жеткаптуретиместамп** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

