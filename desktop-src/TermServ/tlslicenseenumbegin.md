---
title: Функция Тлслиценсинумбегин
description: Начинает перечисление лицензий, выданных сервером лицензий удаленный рабочий стол на основе условий поиска.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлслиценсинумбегин
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803856"
---
# <a name="tlslicenseenumbegin-function"></a>Функция Тлслиценсинумбегин

Начинает перечисление лицензий, выданных сервером лицензий удаленный рабочий стол на основе условий поиска.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ххандле* \[ окне\]
</dt> <dd>

Обработчик на удаленный рабочий стол сервере лицензирования. Укажите маркер, Открытый функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .

</dd> <dt>

*двсеарчпарм* \[ окне\]
</dt> <dd>

Задает условия поиска. Параметр может быть одним или несколькими значениями, описанными в следующем списке. Параметр указывает тип пакета ключей и пакет ключей для поиска.

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**Лслиценсе \_ Поиск \_ лиценсеид** (0x00000001)


</dt> <dd>

Поиск по ИДЕНТИФИКАТОРу лицензии.

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**Лслиценсе \_ Поиск \_ кэйпаккид** (0x00000002)


</dt> <dd>

Поиск по ИДЕНТИФИКАТОРу пакета ключей.

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**Лслиценсе \_ Поиск \_ MachineName** (0x00000008)


</dt> <dd>

Поиск по имени компьютера.

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**Лслиценсе \_ Поиск \_ имени пользователя** (0x00000010)


</dt> <dd>

Поиск по имени пользователя.

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**Лслиценсе \_ Поиск \_ иссуедате** (0x00000080)


</dt> <dd>

Поиск по дате выпуска.

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**Лслиценсе \_ Поиск \_ ExpireDate** (0x00000100)


</dt> <dd>

Поиск по дате окончания срока действия.

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**Лслиценсе \_ Поиск \_ нумлиценсес** (0x00000200)


</dt> <dd>

Поиск по количеству лицензий.

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**Лслиценсе \_ \_ \_ Состояние записи поиска** (0x20000000)


</dt> <dd>

Поиск по состоянию записи.

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**Лслиценсе \_ ЕКССЕАРЧ \_ лиценсестатус** (0x00100000)


</dt> <dd>

Поиск по состоянию лицензии.

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**Лскэйпакк \_ ИСКАТЬ \_ все** (0xFFFFFFFF)


</dt> <dd>

Поиск по всем лицензиям.

</dd> </dl> </dd> <dt>

*бматчалл* \[ окне\]
</dt> <dd>

Указывает, следует ли сопоставлять все значения поиска.

</dd> <dt>

*лпсеарчпарм* \[ окне\]
</dt> <dd>

Указатель на структуру [**лслиценсе**](lslicense.md) , указывающую искомые параметры поиска.

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

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Лсервер \_ E, \_ Внутренняя \_ ошибка** (5001)


</dt> <dd>

Внутренняя ошибка на сервере лицензирования.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Лсервер \_ E \_ Недопустимая \_ последовательность** (5006)


</dt> <dd>

Недопустимая последовательность вызова. Скорее всего, предыдущее перечисление не завершено.

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

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Лсервер \_ E \_ недопустимые \_ данные** (5009)


</dt> <dd>

Недопустимые данные в параметре поиска.

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

[**лслиценсе**](lslicense.md)
</dt> <dt>

[**тлсконнекттолссервер**](tlsconnecttolsserver.md)
</dt> <dt>

[**тлслиценсинумнекст**](tlslicenseenumnext.md)
</dt> <dt>

[**тлслиценсинуменд**](tlslicenseenumend.md)
</dt> </dl>

 

