---
description: Начинает мониторинг неактивности.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: Функция Бегинидледетектион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668847"
---
# <a name="beginidledetection-function"></a>Функция Бегинидледетектион

\[Эта функция не поддерживается и может быть изменена или недоступна в будущем. Вместо этого используйте функцию **жетластинпутинфо** .\]

Начинает мониторинг неактивности.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфнкаллбакк* 
</dt> <dd>

Функция, которая вызывается при изменении состояния простоя. Этот обратный вызов определяется следующим образом:

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

*двидлемин* 
</dt> <dd>

Число минут бездействия до вызова функции обратного вызова.

</dd> <dt>

*двресервед* 
</dt> <dd>

Этот параметр должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0, если функция выполнена. в противном случае возвращается код ошибки. Например, если *двресервед* имеет значение, отличное от 0, **возвращаются \_ недопустимые \_ данные** .

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Эта функция не экспортируется по имени; Укажите порядковый номер 3 при вызове **GetProcAddress**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетластинпутинфо**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
