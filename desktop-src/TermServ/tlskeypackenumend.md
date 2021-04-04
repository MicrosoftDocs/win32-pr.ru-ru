---
title: Функция Тлскэйпаккенуменд
description: Переходит от предыдущего вызова функции Тлскэйпаккенумбегин и завершает перечисление.
ms.assetid: 3434e18d-54c9-46ed-b6a5-bc174b63a152
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлскэйпаккенуменд
topic_type:
- apiref
api_name:
- TLSKeyPackEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04723318b29adff7a647fe2cab39fb0b16f3f5a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802105"
---
# <a name="tlskeypackenumend-function"></a>Функция Тлскэйпаккенуменд

Переходит от предыдущего вызова функции [**тлскэйпаккенумбегин**](tlskeypackenumbegin.md) и завершает перечисление.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI TLSKeyPackEnumEnd(
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**лскэйпакк**](lskeypack.md)
</dt> <dt>

[**тлсконнекттолссервер**](tlsconnecttolsserver.md)
</dt> <dt>

[**тлскэйпаккенумбегин**](tlskeypackenumbegin.md)
</dt> <dt>

[**тлскэйпаккенумнекст**](tlskeypackenumnext.md)
</dt> </dl>

 

