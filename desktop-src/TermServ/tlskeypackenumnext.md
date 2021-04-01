---
title: Функция Тлскэйпаккенумнекст
description: Переходит от предыдущего вызова функции Тлскэйпаккенумбегин и возвращает следующий пакет ключей, установленный на сервере лицензирования удаленный рабочий стол, который соответствует условиям поиска.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлскэйпаккенумнекст
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897874f333ed7933ea1616f7f5ba5f1686736d0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071218"
---
# <a name="tlskeypackenumnext-function"></a>Функция Тлскэйпаккенумнекст

Переходит от предыдущего вызова функции [**тлскэйпаккенумбегин**](tlskeypackenumbegin.md) и возвращает следующий пакет ключей, установленный на сервере лицензирования удаленный рабочий стол, который соответствует условиям поиска.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ххандле* \[ окне\]
</dt> <dd>

Обработчик на удаленный рабочий стол сервере лицензирования. Укажите маркер, Открытый функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .

</dd> <dt>

*лпкэйпакк* \[ окне\]
</dt> <dd>

Указатель на структуру [**лскэйпакк**](lskeypack.md) , которая получает следующий пакет ключей, соответствующий условиям поиска.

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

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**Лсервер \_ \_Нет \_ \_ данных** (4001)


</dt> <dd>

Дополнительные ключевые пакеты не соответствуют условиям поиска.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Лсервер \_ E, \_ Внутренняя \_ ошибка** (5001)


</dt> <dd>

Внутренняя ошибка на сервере лицензирования.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Лсервер \_ E \_ Недопустимая \_ последовательность** (5006)


</dt> <dd>

Недопустимая последовательность вызова. Перед этим необходимо вызвать функцию [**тлскэйпаккенумбегин ()**](tlskeypackenumbegin.md) .

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Лсервер \_ \_Сервер E \_ занят** (5007)


</dt> <dd>

Сервер лицензирования слишком занят для обработки запроса.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Лсервер \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

Не удается обработать запрос из-за нехватки памяти.

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

[**тлскэйпаккенуменд**](tlskeypackenumend.md)
</dt> </dl>

 

