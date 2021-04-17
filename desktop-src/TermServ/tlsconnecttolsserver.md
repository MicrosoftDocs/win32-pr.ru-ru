---
title: Функция Тлсконнекттолссервер
description: Открывает маркер указанного сервера лицензий удаленный рабочий стол.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлсконнекттолссервер
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415740"
---
# <a name="tlsconnecttolsserver-function"></a>Функция Тлсконнекттолссервер

Открывает маркер указанного сервера лицензий удаленный рабочий стол.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзлссервер* \[ окне\]
</dt> <dd>

Указатель на строку, завершающуюся **нулем**, которая указывает NetBIOS-имя сервера лицензий удаленный рабочий стол. Если значение этого параметра равно **null**, то указанный сервер является локальным компьютером.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена, возвращаемое значение является обработчиком указанного сервера.

Если функция завершается ошибкой, возвращается значение **null**. Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Комментарии

После завершения использования маркера, возвращаемого функцией **тлсконнекттолссервер** , выпустите его, вызвав функцию [**тлсдисконнектфромсервер**](tlsdisconnectfromserver.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_маркер TLS**](tls-handle.md)
</dt> <dt>

[**тлсдисконнектфромсервер**](tlsdisconnectfromserver.md)
</dt> </dl>

 

