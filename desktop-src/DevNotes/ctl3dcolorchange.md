---
description: Обрабатывает изменения системного цвета для приложений, использующих CTL3D сегодня.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Функция Ctl3dColorChange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657424"
---
# <a name="ctl3dcolorchange-function"></a>Функция Ctl3dColorChange

Обрабатывает изменения системного цвета для приложений, использующих CTL3D сегодня.

## <a name="syntax"></a>Синтаксис


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Эта функция должна вызываться в главном окне приложения для сообщения **WM \_ сисколорчанже** , как показано ниже.

## <a name="examples"></a>Примеры

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
