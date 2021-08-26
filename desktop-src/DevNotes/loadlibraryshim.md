---
description: загружает указанную версию библиотеки DLL платформа .NET Framework библиотеки.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: Функция Лоадлибраришим
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 123d4036713d6c1c5b7f7a08026d29d7d34126c28c5c2c1fceb94eb01baf9609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001244"
---
# <a name="loadlibraryshim-function"></a>Функция Лоадлибраришим

загружает указанную версию библиотеки DLL платформа .NET Framework библиотеки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сздллнаме* \[ окне\]
</dt> <dd>

имя библиотеки DLL, загружаемой из платформа .NET Framework.

</dd> <dt>

*сзверсион* \[ окне\]
</dt> <dd>

Версия загружаемой библиотеки DLL. Если *сзверсион* имеет **значение NULL**, загружается последняя версия указанной библиотеки DLL.

</dd> <dt>

*пвресервед* 
</dt> <dd>

Зарезервировано.

</dd> <dt>

*фмоддлл* \[ заполняет\]
</dt> <dd>

Обработчик для модуля.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

эта функция используется для загрузки библиотек dll библиотеки, включенных в распространяемый пакет платформа .NET Framework, а не для создаваемых пользователем библиотек dll.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
