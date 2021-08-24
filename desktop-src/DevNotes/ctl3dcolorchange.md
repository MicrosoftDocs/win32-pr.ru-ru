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
ms.openlocfilehash: c9c3032bb7105a27b995c236e01ce5fc5c304de4108f6c996a5cbb5799be496d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654604"
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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Эта функция должна вызываться в главном окне приложения для сообщения **WM \_ сисколорчанже** , как показано ниже.

## <a name="examples"></a>Примеры

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
