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
# <a name="tlskeypackenumnext-function"></a><span data-ttu-id="0977e-104">Функция Тлскэйпаккенумнекст</span><span class="sxs-lookup"><span data-stu-id="0977e-104">TLSKeyPackEnumNext function</span></span>

<span data-ttu-id="0977e-105">Переходит от предыдущего вызова функции [**тлскэйпаккенумбегин**](tlskeypackenumbegin.md) и возвращает следующий пакет ключей, установленный на сервере лицензирования удаленный рабочий стол, который соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="0977e-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="0977e-106">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="0977e-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="0977e-107">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="0977e-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0977e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0977e-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="0977e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0977e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0977e-110">*ххандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0977e-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0977e-111">Обработчик на удаленный рабочий стол сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0977e-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="0977e-112">Укажите маркер, Открытый функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="0977e-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0977e-113">*лпкэйпакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0977e-113">*lpKeyPack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0977e-114">Указатель на структуру [**лскэйпакк**](lskeypack.md) , которая получает следующий пакет ключей, соответствующий условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="0977e-114">Pointer to a [**LSKeyPack**](lskeypack.md) structure that receives the next key pack that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="0977e-115">*пдверркоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0977e-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0977e-116">Указатель на переменную, которая принимает один из следующих кодов ошибок при возврате.</span><span class="sxs-lookup"><span data-stu-id="0977e-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="0977e-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Лсервер \_ \_Успешно завершено** (0)</span><span class="sxs-lookup"><span data-stu-id="0977e-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0977e-118">Вызов успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="0977e-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="0977e-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**Лсервер \_ \_Нет \_ \_ данных** (4001)</span><span class="sxs-lookup"><span data-stu-id="0977e-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="0977e-120">Дополнительные ключевые пакеты не соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="0977e-120">No more key packs match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="0977e-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Лсервер \_ E, \_ Внутренняя \_ ошибка** (5001)</span><span class="sxs-lookup"><span data-stu-id="0977e-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="0977e-122">Внутренняя ошибка на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0977e-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="0977e-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Лсервер \_ E \_ Недопустимая \_ последовательность** (5006)</span><span class="sxs-lookup"><span data-stu-id="0977e-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="0977e-124">Недопустимая последовательность вызова.</span><span class="sxs-lookup"><span data-stu-id="0977e-124">The calling sequence was not valid.</span></span> <span data-ttu-id="0977e-125">Перед этим необходимо вызвать функцию [**тлскэйпаккенумбегин ()**](tlskeypackenumbegin.md) .</span><span class="sxs-lookup"><span data-stu-id="0977e-125">Must call the [**TLSKeyPackEnumBegin()**](tlskeypackenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="0977e-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Лсервер \_ \_Сервер E \_ занят** (5007)</span><span class="sxs-lookup"><span data-stu-id="0977e-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="0977e-127">Сервер лицензирования слишком занят для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="0977e-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="0977e-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Лсервер \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="0977e-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="0977e-129">Не удается обработать запрос из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="0977e-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0977e-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0977e-130">Return value</span></span>

<span data-ttu-id="0977e-131">Эта функция возвращает следующие возможные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="0977e-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="0977e-132">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="0977e-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="0977e-133">Вызов прошел.</span><span class="sxs-lookup"><span data-stu-id="0977e-133">The call succeeded.</span></span> <span data-ttu-id="0977e-134">Проверьте значение параметра *пдверркоде* , чтобы получить код возврата для вызова.</span><span class="sxs-lookup"><span data-stu-id="0977e-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="0977e-135">**\_ \_ Недопустимый \_ аргумент RPC S**</span><span class="sxs-lookup"><span data-stu-id="0977e-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="0977e-136">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="0977e-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0977e-137">Требования</span><span class="sxs-lookup"><span data-stu-id="0977e-137">Requirements</span></span>



| <span data-ttu-id="0977e-138">Требование</span><span class="sxs-lookup"><span data-stu-id="0977e-138">Requirement</span></span> | <span data-ttu-id="0977e-139">Значение</span><span class="sxs-lookup"><span data-stu-id="0977e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0977e-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0977e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0977e-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0977e-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0977e-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0977e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0977e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0977e-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0977e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0977e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0977e-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0977e-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0977e-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0977e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0977e-147">**лскэйпакк**</span><span class="sxs-lookup"><span data-stu-id="0977e-147">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="0977e-148">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="0977e-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="0977e-149">**тлскэйпаккенумбегин**</span><span class="sxs-lookup"><span data-stu-id="0977e-149">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="0977e-150">**тлскэйпаккенуменд**</span><span class="sxs-lookup"><span data-stu-id="0977e-150">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

