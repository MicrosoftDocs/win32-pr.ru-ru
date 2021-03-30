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
# <a name="tlslicenseenumbegin-function"></a><span data-ttu-id="af334-104">Функция Тлслиценсинумбегин</span><span class="sxs-lookup"><span data-stu-id="af334-104">TLSLicenseEnumBegin function</span></span>

<span data-ttu-id="af334-105">Начинает перечисление лицензий, выданных сервером лицензий удаленный рабочий стол на основе условий поиска.</span><span class="sxs-lookup"><span data-stu-id="af334-105">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="af334-106">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="af334-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="af334-107">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="af334-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="af334-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af334-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="af334-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="af334-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af334-110">*ххандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af334-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af334-111">Обработчик на удаленный рабочий стол сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="af334-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="af334-112">Укажите маркер, Открытый функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="af334-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="af334-113">*двсеарчпарм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af334-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af334-114">Задает условия поиска.</span><span class="sxs-lookup"><span data-stu-id="af334-114">Specifies the search criteria.</span></span> <span data-ttu-id="af334-115">Параметр может быть одним или несколькими значениями, описанными в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="af334-115">The parameter can be one or a combination of the values that are described in the following list.</span></span> <span data-ttu-id="af334-116">Параметр указывает тип пакета ключей и пакет ключей для поиска.</span><span class="sxs-lookup"><span data-stu-id="af334-116">The parameter specifies the type of key pack and which key pack to search.</span></span>

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span data-ttu-id="af334-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**Лслиценсе \_ Поиск \_ лиценсеид** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="af334-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE\_SEARCH\_LICENSEID** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="af334-118">Поиск по ИДЕНТИФИКАТОРу лицензии.</span><span class="sxs-lookup"><span data-stu-id="af334-118">Search by license ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span data-ttu-id="af334-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**Лслиценсе \_ Поиск \_ кэйпаккид** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="af334-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE\_SEARCH\_KEYPACKID** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="af334-120">Поиск по ИДЕНТИФИКАТОРу пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="af334-120">Search by key pack ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span data-ttu-id="af334-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**Лслиценсе \_ Поиск \_ MachineName** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="af334-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE\_SEARCH\_MACHINENAME** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="af334-122">Поиск по имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="af334-122">Search by machine name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span data-ttu-id="af334-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**Лслиценсе \_ Поиск \_ имени пользователя** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="af334-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE\_SEARCH\_USERNAME** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="af334-124">Поиск по имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="af334-124">Search by user name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span data-ttu-id="af334-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**Лслиценсе \_ Поиск \_ иссуедате** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="af334-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE\_SEARCH\_ISSUEDATE** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="af334-126">Поиск по дате выпуска.</span><span class="sxs-lookup"><span data-stu-id="af334-126">Search by issue date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span data-ttu-id="af334-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**Лслиценсе \_ Поиск \_ ExpireDate** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="af334-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE\_SEARCH\_EXPIREDATE** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="af334-128">Поиск по дате окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="af334-128">Search by expiration date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span data-ttu-id="af334-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**Лслиценсе \_ Поиск \_ нумлиценсес** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="af334-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE\_SEARCH\_ NUMLICENSES** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="af334-130">Поиск по количеству лицензий.</span><span class="sxs-lookup"><span data-stu-id="af334-130">Search by number of licenses.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span data-ttu-id="af334-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**Лслиценсе \_ \_ \_ Состояние записи поиска** (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="af334-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE\_SEARCH\_ ENTRY\_STATUS** (0x20000000)</span></span>


</dt> <dd>

<span data-ttu-id="af334-132">Поиск по состоянию записи.</span><span class="sxs-lookup"><span data-stu-id="af334-132">Search by entry status.</span></span>

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span data-ttu-id="af334-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**Лслиценсе \_ ЕКССЕАРЧ \_ лиценсестатус** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="af334-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE\_EXSEARCH\_LICENSESTATUS** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="af334-134">Поиск по состоянию лицензии.</span><span class="sxs-lookup"><span data-stu-id="af334-134">Search by license status.</span></span>

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span data-ttu-id="af334-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**Лскэйпакк \_ ИСКАТЬ \_ все** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="af334-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK\_SEARCH\_ALL** (0xFFFFFFFF)</span></span>


</dt> <dd>

<span data-ttu-id="af334-136">Поиск по всем лицензиям.</span><span class="sxs-lookup"><span data-stu-id="af334-136">Search all licenses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="af334-137">*бматчалл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af334-137">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af334-138">Указывает, следует ли сопоставлять все значения поиска.</span><span class="sxs-lookup"><span data-stu-id="af334-138">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="af334-139">*лпсеарчпарм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af334-139">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af334-140">Указатель на структуру [**лслиценсе**](lslicense.md) , указывающую искомые параметры поиска.</span><span class="sxs-lookup"><span data-stu-id="af334-140">Pointer to a [**LSLicense**](lslicense.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="af334-141">*пдверркоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af334-141">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af334-142">Указатель на переменную, которая принимает один из следующих кодов ошибок при возврате.</span><span class="sxs-lookup"><span data-stu-id="af334-142">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="af334-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Лсервер \_ \_Успешно завершено** (0)</span><span class="sxs-lookup"><span data-stu-id="af334-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="af334-144">Вызов успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="af334-144">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="af334-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Лсервер \_ E, \_ Внутренняя \_ ошибка** (5001)</span><span class="sxs-lookup"><span data-stu-id="af334-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="af334-146">Внутренняя ошибка на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="af334-146">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="af334-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Лсервер \_ E \_ Недопустимая \_ последовательность** (5006)</span><span class="sxs-lookup"><span data-stu-id="af334-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="af334-148">Недопустимая последовательность вызова.</span><span class="sxs-lookup"><span data-stu-id="af334-148">The calling sequence was not valid.</span></span> <span data-ttu-id="af334-149">Скорее всего, предыдущее перечисление не завершено.</span><span class="sxs-lookup"><span data-stu-id="af334-149">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="af334-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Лсервер \_ \_Сервер E \_ занят** (5007)</span><span class="sxs-lookup"><span data-stu-id="af334-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="af334-151">Сервер лицензирования слишком занят для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="af334-151">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="af334-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Лсервер \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="af334-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="af334-153">Не удается обработать запрос из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="af334-153">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="af334-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Лсервер \_ E \_ недопустимые \_ данные** (5009)</span><span class="sxs-lookup"><span data-stu-id="af334-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="af334-155">Недопустимые данные в параметре поиска.</span><span class="sxs-lookup"><span data-stu-id="af334-155">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af334-156">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af334-156">Return value</span></span>

<span data-ttu-id="af334-157">Эта функция возвращает следующие возможные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="af334-157">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="af334-158">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="af334-158">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="af334-159">Вызов прошел.</span><span class="sxs-lookup"><span data-stu-id="af334-159">The call succeeded.</span></span> <span data-ttu-id="af334-160">Проверьте значение параметра *пдверркоде* , чтобы получить код возврата для вызова.</span><span class="sxs-lookup"><span data-stu-id="af334-160">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="af334-161">**\_ \_ Недопустимый \_ аргумент RPC S**</span><span class="sxs-lookup"><span data-stu-id="af334-161">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="af334-162">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="af334-162">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af334-163">Требования</span><span class="sxs-lookup"><span data-stu-id="af334-163">Requirements</span></span>



| <span data-ttu-id="af334-164">Требование</span><span class="sxs-lookup"><span data-stu-id="af334-164">Requirement</span></span> | <span data-ttu-id="af334-165">Значение</span><span class="sxs-lookup"><span data-stu-id="af334-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af334-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af334-166">Minimum supported client</span></span><br/> | <span data-ttu-id="af334-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af334-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af334-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af334-168">Minimum supported server</span></span><br/> | <span data-ttu-id="af334-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af334-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af334-170">DLL</span><span class="sxs-lookup"><span data-stu-id="af334-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af334-171"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af334-171"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af334-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af334-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af334-173">**лслиценсе**</span><span class="sxs-lookup"><span data-stu-id="af334-173">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="af334-174">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="af334-174">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="af334-175">**тлслиценсинумнекст**</span><span class="sxs-lookup"><span data-stu-id="af334-175">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="af334-176">**тлслиценсинуменд**</span><span class="sxs-lookup"><span data-stu-id="af334-176">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

