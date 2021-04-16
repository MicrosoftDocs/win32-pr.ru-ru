---
description: Функция Жетенабледпротоколс возвращает таблицу всех протоколов, помеченных как включенные.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Функция Жетенабледпротоколс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650480"
---
# <a name="getenabledprotocols-function"></a>Функция Жетенабледпротоколс

Функция **жетенабледпротоколс** возвращает таблицу всех протоколов, помеченных как включенные.

## <a name="syntax"></a>Синтаксис


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хкаптуре* \[ окне\]
</dt> <dd>

Обработчик для записи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на структуру [протоколтабле](protocoltable.md) , в которой перечислены все включенные протоколы в записи.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="remarks"></a>Комментарии

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетенабледпротоколс** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[протоколтабле](protocoltable.md)
</dt> </dl>

 

 




