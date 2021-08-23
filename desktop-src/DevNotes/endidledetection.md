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
ms.openlocfilehash: a2ba6732b9221d4d4d43e670d0d42d39363d50dffc0d2d4b0daf378b10dd292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691414"
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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Эта функция не экспортируется по имени; Укажите порядковый номер 4 при вызове **GetProcAddress**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**жетластинпутинфо**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
