---
title: Функция Тлслиценсинуменд
description: Переходит от предыдущего вызова функции Тлслиценсинумбегин и завершает перечисление.
ms.assetid: b9cba03c-0f5a-41e8-ae13-bcdd0ac6dd99
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлслиценсинуменд
topic_type:
- apiref
api_name:
- TLSLicenseEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0518b9c27b01484b7fb92dd254ae6f1ccdf01d36ef602541209b9f38abd205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869214"
---
# <a name="tlslicenseenumend-function"></a>Функция Тлслиценсинуменд

Переходит от предыдущего вызова функции [**тлслиценсинумбегин**](tlslicenseenumbegin.md) и завершает перечисление.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ххандле* \[ окне\]
</dt> <dd>

Обработчик на удаленный рабочий стол сервере лицензирования. Укажите маркер, Открытый функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .

</dd> <dt>

*пдверркоде* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая принимает один из следующих кодов ошибок при возврате.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Лсервер \_ \_Успешно завершено** (0)


</dt> <dd>

Вызов успешно выполнен.

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**Лсервер \_ \_Недопустимый \_ маркер "E** " (5005)


</dt> <dd>

Недопустимый маркер.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает следующие возможные возвращаемые значения.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

Вызов прошел. Проверьте значение параметра *пдверркоде* , чтобы получить код возврата для вызова.

</dd> <dt>

**\_ \_ Недопустимый \_ аргумент RPC S**
</dt> <dd>

Недопустимый аргумент.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**лслиценсе**](lslicense.md)
</dt> <dt>

[**тлсконнекттолссервер**](tlsconnecttolsserver.md)
</dt> <dt>

[**тлслиценсинумбегин**](tlslicenseenumbegin.md)
</dt> <dt>

[**тлслиценсинумнекст**](tlslicenseenumnext.md)
</dt> </dl>

 

