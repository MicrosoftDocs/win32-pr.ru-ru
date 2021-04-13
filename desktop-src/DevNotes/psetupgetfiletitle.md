---
description: Возвращает заголовок файла для указанного пути к файлу.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: Функция Псетупжетфилетитле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647977"
---
# <a name="psetupgetfiletitle-function"></a>Функция Псетупжетфилетитле

\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]

Возвращает заголовок файла для указанного пути к файлу.

## <a name="syntax"></a>Синтаксис


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь к файлу* \[ окне\]
</dt> <dd>

Путь к файлу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Указатель на строку, которая получает заголовок файла.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
