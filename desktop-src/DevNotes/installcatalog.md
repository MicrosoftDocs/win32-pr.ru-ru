---
description: Устанавливает каталог в каталог.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: Функция Инсталлкаталог
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669068"
---
# <a name="installcatalog-function"></a>Функция Инсталлкаталог

\[Эта функция не поддерживается и не должна использоваться.\]

Устанавливает каталог в каталог.

## <a name="syntax"></a>Синтаксис


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Каталогфуллпас* \[ окне\]
</dt> <dd>

Указатель на строку, представляющую полный путь к каталогу перед установкой.

</dd> <dt>

*Невбасенаме* \[ в необязательное\]
</dt> <dd>

Указатель на новое базовое имя.

</dd> <dt>

*Невкаталогфуллпас* \[ out, необязательно\]
</dt> <dd>

Указатель на строку, представляющую полный путь к каталогу после установки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция в настоящее время не реализована, поэтому она не возвращает фактическое значение.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
