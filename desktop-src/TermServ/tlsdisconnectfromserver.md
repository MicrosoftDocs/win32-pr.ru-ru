---
title: Функция Тлсдисконнектфромсервер
description: Закрывает открытый маркер для сервера лицензий удаленный рабочий стол.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлсдисконнектфромсервер
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682110"
---
# <a name="tlsdisconnectfromserver-function"></a>Функция Тлсдисконнектфромсервер

Закрывает открытый маркер для сервера лицензий удаленный рабочий стол.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ххандле* \[ окне\]
</dt> <dd>

Обработчик на удаленный рабочий стол сервере лицензирования, который открыт при вызове функции [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Вызовите функцию **тлсдисконнектфромсервер** в рамках программы очистки программы, чтобы закрыть все дескрипторы сервера, открытые с помощью вызовов функции [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .

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

[**тлсконнекттолссервер**](tlsconnecttolsserver.md)
</dt> </dl>

 

