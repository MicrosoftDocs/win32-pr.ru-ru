---
description: Проверяет, могут ли элементы управления использовать объемные эффекты.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Функция Ctl3dEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657831"
---
# <a name="ctl3denabled-function"></a>Функция Ctl3dEnabled

Проверяет, могут ли элементы управления использовать объемные эффекты.

## <a name="syntax"></a>Синтаксис


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если элементы управления могут использовать трехмерные эффекты; в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

В Windows 4,0 или более поздней версии **Ctl3dEnabled** и [**Ctl3dRegister**](ctl3dregister.md) возвращают **значение false**.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
