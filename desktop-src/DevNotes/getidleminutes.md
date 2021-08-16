---
description: Возвращает продолжительность времени (в минутах) с момента последнего действия пользователя.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: Функция Жетидлеминутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: d3397de5d792181958891eef9693d29b2d7d4e56f9bbc7f7e1cfef19171625b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404587"
---
# <a name="getidleminutes-function"></a>Функция Жетидлеминутес

\[Эта функция не поддерживается и может быть изменена или недоступна в будущем. Вместо этого используйте функцию **жетластинпутинфо** .\]

Возвращает продолжительность времени (в минутах) с момента последнего действия пользователя.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двресервед* 
</dt> <dd>

Этот параметр должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает количество минут с момента последнего действия пользователя.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Эта функция не экспортируется по имени; При вызове **GetProcAddress** укажите порядковый номер 8.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетластинпутинфо**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
