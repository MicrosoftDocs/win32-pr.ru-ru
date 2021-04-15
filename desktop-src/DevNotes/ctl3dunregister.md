---
description: Отменяет регистрацию приложения в качестве клиента CTL3D сегодня.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Функция Ctl3dUnregister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648994"
---
# <a name="ctl3dunregister-function"></a>Функция Ctl3dUnregister

Отменяет регистрацию приложения в качестве клиента CTL3D сегодня.

## <a name="syntax"></a>Синтаксис


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хинстапп* 
</dt> <dd>

Маркер для отмены регистрации приложения в качестве клиента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если регистрация приложения в качестве клиента CTL3D сегодня отменена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Приложение, использующее CTL3D сегодня, должно вызывать эту функцию в WinMain.

Объемные эффекты недоступны в системах, которые имеют меньшее разрешение VGA.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
