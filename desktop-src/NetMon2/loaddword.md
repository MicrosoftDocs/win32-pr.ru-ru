---
description: Функция Лоаддворд вызывается монитором для задания переменной типа DWORD значения, взятого из строковой переменной конфигурации HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Функция Лоаддворд (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8fa0477122548dad30911948a3581d269b22d8d6eb866273f32aa40a9b427545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778764"
---
# <a name="loaddword-function"></a>Функция Лоаддворд

Функция **лоаддворд** вызывается монитором для задания переменной **типа DWORD** значения, взятого из строковой переменной конфигурации HTML.

## <a name="syntax"></a>Синтаксис


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pConfig* \[ окне\]
</dt> <dd>

Указатель на строку конфигурации HTML, переданную в монитор методом [имонитор::D оконфигуре](imonitor-doconfigure.md) .

</dd> <dt>

*пварнаме* \[ окне\]
</dt> <dd>

Указатель на имя переменной в строке конфигурации.

</dd> <dt>

*pValue* \[ окне\]
</dt> <dd>

Указатель на переменную **DWORD** , для которой задано значение переменной строки конфигурации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно (если имя переменной было обнаружено и имело строку, отличную от нулевой длины), то вставляется **параметр DWORD** , а возвращаемое значение — **true**.

Если функция завершается неудачно, возвращается значение **false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




