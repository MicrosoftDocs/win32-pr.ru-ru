---
description: Открывает существующую символьную ссылку.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: Функция Нтопенсимболиклинкобжект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668693"
---
# <a name="ntopensymboliclinkobject-function"></a>Функция Нтопенсимболиклинкобжект

\[Эта функция может быть изменена или недоступна в будущем.\]

Открывает существующую символьную ссылку.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Линкхандле* \[ заполняет\]
</dt> <dd>

Маркер вновь открытого объекта символьной ссылки.

</dd> <dt>

*Десиредакцесс* \[ окне\]
</dt> <dd>

[**\_ Маска доступа**](../secauthz/access-mask.md) , указывающая запрошенный доступ к объекту каталога. Обычно используется универсальный метод Read, \_ поэтому этот обработчик может быть передан в функцию [**нткуеридиректорйобжект**](ntquerydirectoryobject.md) .

</dd> <dt>

*Обжектаттрибутес* \[ окне\]
</dt> <dd>

Атрибуты для объекта каталога. Чтобы инициализировать структуру **\_ атрибутов объекта** , используйте макрос **инитиализеобжектаттрибутес** . Если вызывающий объект не выполняется в системном контексте потока, он должен указать флаг " **obj \_ kernel \_ Handle** " при инициализации структуры. Дополнительные сведения см. в документации по этим элементам в документации по WDK.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает состояние **\_ Success** или Error.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**нткуеридиректорйобжект**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
