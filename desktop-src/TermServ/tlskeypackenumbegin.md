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
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341255"
---
# <a name="tlskeypackenumbegin-function"></a><span data-ttu-id="90c73-104">Функция Тлскэйпаккенумбегин</span><span class="sxs-lookup"><span data-stu-id="90c73-104">TLSKeyPackEnumBegin function</span></span>

<span data-ttu-id="90c73-105">Начинает перечисление всех ключевых пакетов, установленных на сервере лицензий удаленный рабочий стол на основе условий поиска.</span><span class="sxs-lookup"><span data-stu-id="90c73-105">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="90c73-106">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="90c73-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="90c73-107">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="90c73-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="90c73-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90c73-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="90c73-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90c73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c73-110">*ххандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90c73-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90c73-111">Обработчик на удаленный рабочий стол сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="90c73-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="90c73-112">Укажите маркер, Открытый функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="90c73-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="90c73-113">*двсеарчпарм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90c73-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90c73-114">Задает условия поиска.</span><span class="sxs-lookup"><span data-stu-id="90c73-114">Specifies the search criteria.</span></span> <span data-ttu-id="90c73-115">Этот параметр зарезервирован для будущего использования и должен содержать 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="90c73-115">This parameter is reserved for future use and must contain 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="90c73-116">*бматчалл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90c73-116">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90c73-117">Указывает, следует ли сопоставлять все значения поиска.</span><span class="sxs-lookup"><span data-stu-id="90c73-117">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="90c73-118">*лпсеарчпарм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90c73-118">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90c73-119">Указатель на структуру [**лскэйпакк**](lskeypack.md) , указывающую искомые параметры поиска.</span><span class="sxs-lookup"><span data-stu-id="90c73-119">Pointer to a [**LSKeyPack**](lskeypack.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="90c73-120">*пдверркоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="90c73-120">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90c73-121">Указатель на переменную, которая принимает один из следующих кодов ошибок при возврате.</span><span class="sxs-lookup"><span data-stu-id="90c73-121">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="90c73-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Лсервер \_ \_Успешно завершено** (0)</span><span class="sxs-lookup"><span data-stu-id="90c73-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="90c73-123">Вызов успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="90c73-123">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="90c73-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Лсервер \_ E, \_ Внутренняя \_ ошибка** (5001)</span><span class="sxs-lookup"><span data-stu-id="90c73-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="90c73-125">Внутренняя ошибка на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="90c73-125">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="90c73-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Лсервер \_ E \_ Недопустимая \_ последовательность** (5006)</span><span class="sxs-lookup"><span data-stu-id="90c73-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="90c73-127">Недопустимая последовательность вызова.</span><span class="sxs-lookup"><span data-stu-id="90c73-127">The calling sequence was not valid.</span></span> <span data-ttu-id="90c73-128">Скорее всего, предыдущее перечисление не завершено.</span><span class="sxs-lookup"><span data-stu-id="90c73-128">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="90c73-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Лсервер \_ \_Сервер E \_ занят** (5007)</span><span class="sxs-lookup"><span data-stu-id="90c73-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="90c73-130">Сервер лицензирования слишком занят для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="90c73-130">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="90c73-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Лсервер \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="90c73-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="90c73-132">Не удается обработать запрос из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="90c73-132">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="90c73-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Лсервер \_ E \_ недопустимые \_ данные** (5009)</span><span class="sxs-lookup"><span data-stu-id="90c73-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="90c73-134">Недопустимые данные в параметре поиска.</span><span class="sxs-lookup"><span data-stu-id="90c73-134">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90c73-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90c73-135">Return value</span></span>

<span data-ttu-id="90c73-136">Эта функция возвращает следующие возможные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="90c73-136">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="90c73-137">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="90c73-137">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="90c73-138">Вызов прошел.</span><span class="sxs-lookup"><span data-stu-id="90c73-138">The call succeeded.</span></span> <span data-ttu-id="90c73-139">Проверьте значение параметра *пдверркоде* , чтобы получить код возврата для вызова.</span><span class="sxs-lookup"><span data-stu-id="90c73-139">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="90c73-140">**\_ \_ Недопустимый \_ аргумент RPC S**</span><span class="sxs-lookup"><span data-stu-id="90c73-140">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="90c73-141">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="90c73-141">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90c73-142">Требования</span><span class="sxs-lookup"><span data-stu-id="90c73-142">Requirements</span></span>



| <span data-ttu-id="90c73-143">Требование</span><span class="sxs-lookup"><span data-stu-id="90c73-143">Requirement</span></span> | <span data-ttu-id="90c73-144">Значение</span><span class="sxs-lookup"><span data-stu-id="90c73-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90c73-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90c73-145">Minimum supported client</span></span><br/> | <span data-ttu-id="90c73-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90c73-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90c73-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90c73-147">Minimum supported server</span></span><br/> | <span data-ttu-id="90c73-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90c73-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90c73-149">DLL</span><span class="sxs-lookup"><span data-stu-id="90c73-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90c73-150"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90c73-150"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90c73-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90c73-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c73-152">**лскэйпакк**</span><span class="sxs-lookup"><span data-stu-id="90c73-152">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="90c73-153">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="90c73-153">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="90c73-154">**тлскэйпаккенумнекст**</span><span class="sxs-lookup"><span data-stu-id="90c73-154">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="90c73-155">**тлскэйпаккенуменд**</span><span class="sxs-lookup"><span data-stu-id="90c73-155">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

