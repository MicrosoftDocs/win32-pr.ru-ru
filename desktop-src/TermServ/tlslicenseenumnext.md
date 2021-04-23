---
title: Функция Тлслиценсинумнекст
description: Продолжение предыдущего вызова функции Тлслиценсинумбегин и возврат следующей лицензии, установленной на сервере лицензирования удаленный рабочий стол, соответствующем условиям поиска.
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлслиценсинумнекст
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c13b0a3137258015fe311c49b2cc9b999e3a13f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416129"
---
# <a name="tlslicenseenumnext-function"></a><span data-ttu-id="fa3f2-104">Функция Тлслиценсинумнекст</span><span class="sxs-lookup"><span data-stu-id="fa3f2-104">TLSLicenseEnumNext function</span></span>

<span data-ttu-id="fa3f2-105">Продолжение предыдущего вызова функции [**тлслиценсинумбегин**](tlslicenseenumbegin.md) и возврат следующей лицензии, установленной на сервере лицензирования удаленный рабочий стол, соответствующем условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="fa3f2-106">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="fa3f2-107">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fa3f2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa3f2-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="fa3f2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa3f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa3f2-110">*ххандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa3f2-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa3f2-111">Обработчик на удаленный рабочий стол сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="fa3f2-112">Укажите маркер, Открытый функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="fa3f2-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="fa3f2-113">*лплиценсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa3f2-113">*lpLicense* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa3f2-114">Указатель на структуру [**лслиценсе**](lslicense.md) , которая получает следующую лицензию, которая соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-114">Pointer to a [**LSLicense**](lslicense.md) structure that receives the next license that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="fa3f2-115">*пдверркоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fa3f2-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa3f2-116">Указатель на переменную, которая принимает один из следующих кодов ошибок при возврате.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="fa3f2-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Лсервер \_ \_Успешно завершено** (0)</span><span class="sxs-lookup"><span data-stu-id="fa3f2-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f2-118">Вызов успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="fa3f2-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**Лсервер \_ \_Нет \_ \_ данных** (4001)</span><span class="sxs-lookup"><span data-stu-id="fa3f2-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f2-120">Больше нет лицензий, соответствующих условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-120">No more licenses match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="fa3f2-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Лсервер \_ E, \_ Внутренняя \_ ошибка** (5001)</span><span class="sxs-lookup"><span data-stu-id="fa3f2-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f2-122">Внутренняя ошибка на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="fa3f2-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Лсервер \_ E \_ Недопустимая \_ последовательность** (5006)</span><span class="sxs-lookup"><span data-stu-id="fa3f2-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f2-124">Недопустимая последовательность вызова.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-124">The calling sequence was not valid.</span></span> <span data-ttu-id="fa3f2-125">Перед этим необходимо вызвать функцию [**тлслиценсинумбегин ()**](tlslicenseenumbegin.md) .</span><span class="sxs-lookup"><span data-stu-id="fa3f2-125">Must call the [**TLSLicenseEnumBegin()**](tlslicenseenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="fa3f2-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Лсервер \_ \_Сервер E \_ занят** (5007)</span><span class="sxs-lookup"><span data-stu-id="fa3f2-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f2-127">Сервер лицензирования слишком занят для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="fa3f2-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Лсервер \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="fa3f2-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f2-129">Не удается обработать запрос из-за нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa3f2-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa3f2-130">Return value</span></span>

<span data-ttu-id="fa3f2-131">Эта функция возвращает следующие возможные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="fa3f2-132">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="fa3f2-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="fa3f2-133">Вызов прошел.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-133">The call succeeded.</span></span> <span data-ttu-id="fa3f2-134">Проверьте значение параметра *пдверркоде* , чтобы получить код возврата для вызова.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="fa3f2-135">**\_ \_ Недопустимый \_ аргумент RPC S**</span><span class="sxs-lookup"><span data-stu-id="fa3f2-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="fa3f2-136">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="fa3f2-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa3f2-137">Требования</span><span class="sxs-lookup"><span data-stu-id="fa3f2-137">Requirements</span></span>



| <span data-ttu-id="fa3f2-138">Требование</span><span class="sxs-lookup"><span data-stu-id="fa3f2-138">Requirement</span></span> | <span data-ttu-id="fa3f2-139">Значение</span><span class="sxs-lookup"><span data-stu-id="fa3f2-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3f2-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa3f2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fa3f2-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa3f2-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa3f2-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa3f2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fa3f2-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa3f2-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa3f2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fa3f2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa3f2-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa3f2-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa3f2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa3f2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa3f2-147">**лслиценсе**</span><span class="sxs-lookup"><span data-stu-id="fa3f2-147">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="fa3f2-148">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="fa3f2-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="fa3f2-149">**тлслиценсинумбегин**</span><span class="sxs-lookup"><span data-stu-id="fa3f2-149">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="fa3f2-150">**тлслиценсинуменд**</span><span class="sxs-lookup"><span data-stu-id="fa3f2-150">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

