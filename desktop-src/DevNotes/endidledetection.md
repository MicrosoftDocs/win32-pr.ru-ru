---
description: Завершает наблюдение за неактивностью.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: Функция Ендидледетектион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648771"
---
# <a name="endidledetection-function"></a>Функция Ендидледетектион

\[Эта функция не поддерживается и может быть изменена или недоступна в будущем. Вместо этого используйте функцию **жетластинпутинфо** .\]

Завершает наблюдение за неактивностью.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI EndIdleDetection(
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

Возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Эта функция не экспортируется по имени; Укажите порядковый номер 4 при вызове **GetProcAddress**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетластинпутинфо**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
