---
description: Устанавливает файл каталога.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: Функция Псетупинсталлкаталог
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648873"
---
# <a name="psetupinstallcatalog-function"></a>Функция Псетупинсталлкаталог

\[Эта функция больше не поддерживается корпорацией Майкрософт. Разработчики должны использовать **крипткатадминаддкаталог**.\]

Устанавливает файл каталога.

## <a name="syntax"></a>Синтаксис


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Каталогфуллпас* \[ окне\]
</dt> <dd>

Полный путь к каталогу, который должен быть установлен в системе.

</dd> <dt>

*Невбасенаме* \[ окне\]
</dt> <dd>

Новое базовое имя, используемое при копировании файла каталога в хранилище каталога.

</dd> <dt>

*Невкаталогфуллпас* \[ out, необязательно\]
</dt> <dd>

При необходимости получает полный путь к файлу каталога в хранилище каталога. Этот буфер должен содержать по крайней мере **максимальный размер \_ пути** (версия ANSI) или символы (версия Юникода).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, она **не возвращает \_ ошибку**. в противном случае она возвращает код ошибки Win32, указывающий на причину сбоя.

## <a name="remarks"></a>Комментарии

Файл копируется системой в специальный каталог и при необходимости переименовывается.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**крипткатадминаддкаталог**](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
