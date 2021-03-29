---
description: Проверяет один файл каталога.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: Функция Верификаталогфиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647933"
---
# <a name="verifycatalogfile-function"></a>Функция Верификаталогфиле

\[Эта функция не поддерживается и не должна использоваться.\]

Проверяет один файл каталога.

## <a name="syntax"></a>Синтаксис


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*каталогфуллпас* 
</dt> <dd>

Полный путь к файлу каталога, который необходимо проверить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается **сообщение об \_ ошибке**; в противном случае возвращается ошибка от [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

Если каталог является каталогом с подписью Authenticode, эта функция возвращает **сообщение об ошибке \_ \_ доверенный \_ Издатель Authenticode** , если он завершается. в противном случае возвращается **сообщение об ошибке " \_ \_ доверие Authenticode \_ не \_ установлено**".

Если функция не может определить, является ли издатель доверенной, он также может возвращать **ошибку \_ неопознанные \_** ошибки.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
