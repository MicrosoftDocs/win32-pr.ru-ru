---
title: Функция Тлскэйпаккенумбегин
description: Начинает перечисление всех ключевых пакетов, установленных на сервере лицензий удаленный рабочий стол на основе условий поиска.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлскэйпаккенумбегин
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469e4e255f3bdd64749060fcb712df480a8a1f6fc3683ebb25916be44856e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869334"
---
# <a name="tlskeypackenumbegin-function"></a>Функция Тлскэйпаккенумбегин

Начинает перечисление всех ключевых пакетов, установленных на сервере лицензий удаленный рабочий стол на основе условий поиска.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
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

Задает условия поиска. Этот параметр зарезервирован для будущего использования и должен содержать 0xFFFFFFFF.

</dd> <dt>

*бматчалл* \[ окне\]
</dt> <dd>

Указывает, следует ли сопоставлять все значения поиска.

</dd> <dt>

*лпсеарчпарм* \[ окне\]
</dt> <dd>

Указатель на структуру [**лскэйпакк**](lskeypack.md) , указывающую искомые параметры поиска.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**лскэйпакк**](lskeypack.md)
</dt> <dt>

[**тлсконнекттолссервер**](tlsconnecttolsserver.md)
</dt> <dt>

[**тлскэйпаккенумнекст**](tlskeypackenumnext.md)
</dt> <dt>

[**тлскэйпаккенуменд**](tlskeypackenumend.md)
</dt> </dl>

 

