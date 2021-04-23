---
title: Функция Тлсжетсерверцертификате
description: Возвращает сертификат сервера лицензирования удаленный рабочий стол.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлсжетсерверцертификате
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672569"
---
# <a name="tlsgetservercertificate-function"></a><span data-ttu-id="2aab3-104">Функция Тлсжетсерверцертификате</span><span class="sxs-lookup"><span data-stu-id="2aab3-104">TLSGetServerCertificate function</span></span>

<span data-ttu-id="2aab3-105">Возвращает сертификат сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="2aab3-105">Returns the certificate of the Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="2aab3-106">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="2aab3-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="2aab3-107">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="2aab3-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2aab3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2aab3-108">Syntax</span></span>


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="2aab3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2aab3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aab3-110">*ххандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-111">Обработчик на удаленный рабочий стол сервере лицензирования, который открыт при вызове функции [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="2aab3-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2aab3-112">*бсигнцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-112">*bSignCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-113">**True** , если сертификат подписи, **значение false** , если сертификат Exchange.</span><span class="sxs-lookup"><span data-stu-id="2aab3-113">**TRUE** if signature certificate, **FALSE** if exchange certificate.</span></span>

</dd> <dt>

<span data-ttu-id="2aab3-114">*ппбцертблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-114">*ppbCertBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-115">Указатель на переменную, которая получает указатель на буфер, содержащий сертификат.</span><span class="sxs-lookup"><span data-stu-id="2aab3-115">Pointer to a variable that receives a pointer to a buffer that contains the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="2aab3-116">*лпдвцертблоблен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-116">*lpdwCertBlobLen* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-117">Указатель на переменную, которая получает размер возвращаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="2aab3-117">Pointer to a variable that receives the size of the certificate that is returned.</span></span>

</dd> <dt>

<span data-ttu-id="2aab3-118">*пдверркоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-118">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-119">Указатель на переменную, которая получает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2aab3-119">Pointer to a variable that receives the error code.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="2aab3-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Лсервер \_ \_Успешно завершено** (0)</span><span class="sxs-lookup"><span data-stu-id="2aab3-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2aab3-121">Вызов успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="2aab3-121">Call is successful.</span></span>

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span data-ttu-id="2aab3-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**Протокол TLS \_ \_ \_ Сертификат селфсигн** (4007)</span><span class="sxs-lookup"><span data-stu-id="2aab3-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS\_W\_SELFSIGN\_CERTIFICATE** (4007)</span></span>


</dt> <dd>

<span data-ttu-id="2aab3-123">Возвращенный сертификат является самозаверяющим.</span><span class="sxs-lookup"><span data-stu-id="2aab3-123">Certificate returned is a self-signed certificate.</span></span>

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span data-ttu-id="2aab3-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**Протокол TLS \_ W \_ temp \_ селфсигн \_ CERT** (4009)</span><span class="sxs-lookup"><span data-stu-id="2aab3-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS\_W\_TEMP\_SELFSIGN\_CERT** (4009)</span></span>


</dt> <dd>

<span data-ttu-id="2aab3-125">Возвращенный сертификат является временным.</span><span class="sxs-lookup"><span data-stu-id="2aab3-125">Certificate returned is temporary.</span></span>

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span data-ttu-id="2aab3-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**Протокол TLS \_ \_Доступ к E \_ запрещен** (5003)</span><span class="sxs-lookup"><span data-stu-id="2aab3-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS\_E\_ACCESS\_DENIED** (5003)</span></span>


</dt> <dd>

<span data-ttu-id="2aab3-127">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2aab3-127">Access denied.</span></span>

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span data-ttu-id="2aab3-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**Протокол TLS \_ \_ \_ Маркер выделения "E** " (5007)</span><span class="sxs-lookup"><span data-stu-id="2aab3-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS\_E\_ALLOCATE\_HANDLE** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="2aab3-129">Сервер слишком занят, чтобы обработать запрос.</span><span class="sxs-lookup"><span data-stu-id="2aab3-129">Server is too busy to process the request.</span></span>

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span data-ttu-id="2aab3-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**Протокол TLS \_ E \_ без \_ сертификата** (5022)</span><span class="sxs-lookup"><span data-stu-id="2aab3-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS\_E\_NO\_CERTIFICATE** (5022)</span></span>


</dt> <dd>

<span data-ttu-id="2aab3-131">Не удается получить сертификат.</span><span class="sxs-lookup"><span data-stu-id="2aab3-131">Cannot retrieve a certificate.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aab3-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2aab3-132">Return value</span></span>

<span data-ttu-id="2aab3-133">Эта функция возвращает следующие возможные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="2aab3-133">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="2aab3-134">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="2aab3-134">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-135">Вызов прошел.</span><span class="sxs-lookup"><span data-stu-id="2aab3-135">The call succeeded.</span></span> <span data-ttu-id="2aab3-136">Проверьте значение параметра *пдверркоде* , чтобы получить код возврата для вызова.</span><span class="sxs-lookup"><span data-stu-id="2aab3-136">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="2aab3-137">**\_ \_ Недопустимый \_ аргумент RPC S**</span><span class="sxs-lookup"><span data-stu-id="2aab3-137">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-138">Недопустимое значение аргумента.</span><span class="sxs-lookup"><span data-stu-id="2aab3-138">The argument was invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2aab3-139">Требования</span><span class="sxs-lookup"><span data-stu-id="2aab3-139">Requirements</span></span>



| <span data-ttu-id="2aab3-140">Требование</span><span class="sxs-lookup"><span data-stu-id="2aab3-140">Requirement</span></span> | <span data-ttu-id="2aab3-141">Значение</span><span class="sxs-lookup"><span data-stu-id="2aab3-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aab3-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2aab3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2aab3-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2aab3-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2aab3-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2aab3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2aab3-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2aab3-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2aab3-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2aab3-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aab3-147"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aab3-147"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aab3-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2aab3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aab3-149">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="2aab3-149">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

