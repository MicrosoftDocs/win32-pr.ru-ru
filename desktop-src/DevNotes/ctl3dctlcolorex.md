---
description: Обрабатывает сообщение WM \_ ктлколор для приложений, использующих CTL3D сегодня.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Функция Ctl3dCtlColorEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648953"
---
# <a name="ctl3dctlcolorex-function"></a>Функция Ctl3dCtlColorEx

Обрабатывает сообщение **WM \_ ктлколор** для приложений, использующих CTL3D сегодня.

## <a name="syntax"></a>Синтаксис


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wm* 
</dt> <dd>

Сообщение **WM \_ ктлколор** для приложения.

</dd> <dt>

*wParam* 
</dt> <dd>

Маркер контекста отображаемого содержимого (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер дочернего окна (элемента управления).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает дескриптор соответствующей кисти, если функция выполнена. в противном случае возвращается значение, `(HBRUSH)(0)` указывающее, что произошла ошибка.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
