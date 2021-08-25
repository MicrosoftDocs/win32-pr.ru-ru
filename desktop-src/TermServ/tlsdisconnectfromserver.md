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
ms.openlocfilehash: 95911536eda4bd87e45fd034626cf83d88f4d9fc768e4837316ee93abfe3c3d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869414"
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

## <a name="remarks"></a>Remarks

Вызовите функцию **тлсдисконнектфромсервер** в рамках программы очистки программы, чтобы закрыть все дескрипторы сервера, открытые с помощью вызовов функции [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_маркер TLS**](tls-handle.md)
</dt> <dt>

[**тлсконнекттолссервер**](tlsconnecttolsserver.md)
</dt> </dl>

 

