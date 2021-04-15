---
description: Регистрирует приложение в качестве клиента CTL3D сегодня.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Функция Ctl3dRegister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648971"
---
# <a name="ctl3dregister-function"></a>Функция Ctl3dRegister

Регистрирует приложение в качестве клиента CTL3D сегодня.

## <a name="syntax"></a>Синтаксис


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хинстапп* 
</dt> <dd>

Описатель приложения, регистрируемого в качестве клиента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если трехмерные эффекты активны; в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Приложение, использующее CTL3D сегодня, должно вызывать эту функцию в WinMain.

Объемные эффекты недоступны в системах, которые имеют меньшее разрешение VGA.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
