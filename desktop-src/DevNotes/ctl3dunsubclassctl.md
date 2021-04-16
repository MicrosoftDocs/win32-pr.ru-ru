---
description: Отключает подкласс для указанного элемента управления.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Функция Ctl3dUnsubclassCtl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648993"
---
# <a name="ctl3dunsubclassctl-function"></a>Функция Ctl3dUnsubclassCtl

Отключает подкласс для указанного элемента управления.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер окна управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если элемент управления успешно подклассаен; в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ctl3dSubclassCtl**](ctl3dsubclassctl.md)
</dt> </dl>

 

 
