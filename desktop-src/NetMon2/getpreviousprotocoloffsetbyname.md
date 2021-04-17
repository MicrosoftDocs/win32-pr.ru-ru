---
description: Функция Жетпревиауспротоколоффсетбинаме возвращает предыдущий экземпляр данного протокола.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Функция Жетпревиауспротоколоффсетбинаме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673183"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a>Функция Жетпревиауспротоколоффсетбинаме

Функция **жетпревиауспротоколоффсетбинаме** возвращает предыдущий экземпляр данного протокола.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфраме* \[ окне\]
</dt> <dd>

Обработчик для фрейма.

</dd> <dt>

*двстартоффсет* \[ окне\]
</dt> <dd>

Смещение в кадре.

</dd> <dt>

*сзпротоколнаме* \[ окне\]
</dt> <dd>

Имя протокола, который нужно найти.

</dd> <dt>

*пдвпревиаусоффсет* \[ заполняет\]
</dt> <dd>

Указатель на **DWORD** , содержащий смещение к предыдущему протоколу (если функция выполнена).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершилась неудачно, возвращаемое значение — НМЕРР \_ Protocol \_ не \_ найдено.

## <a name="remarks"></a>Комментарии

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать **жетпревиауспротоколоффсетбинаме**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




