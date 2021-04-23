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
ms.openlocfilehash: 8bbd494ec539ee78008fa3df274282da1e9db6c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672827"
---
# <a name="tlslicenseenumend-function"></a><span data-ttu-id="3a04b-104">Функция Тлслиценсинуменд</span><span class="sxs-lookup"><span data-stu-id="3a04b-104">TLSLicenseEnumEnd function</span></span>

<span data-ttu-id="3a04b-105">Переходит от предыдущего вызова функции [**тлслиценсинумбегин**](tlslicenseenumbegin.md) и завершает перечисление.</span><span class="sxs-lookup"><span data-stu-id="3a04b-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="3a04b-106">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="3a04b-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="3a04b-107">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="3a04b-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3a04b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a04b-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="3a04b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a04b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a04b-110">*ххандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a04b-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a04b-111">Обработчик на удаленный рабочий стол сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="3a04b-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="3a04b-112">Укажите маркер, Открытый функцией [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="3a04b-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3a04b-113">*пдверркоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a04b-113">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a04b-114">Указатель на переменную, которая принимает один из следующих кодов ошибок при возврате.</span><span class="sxs-lookup"><span data-stu-id="3a04b-114">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="3a04b-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Лсервер \_ \_Успешно завершено** (0)</span><span class="sxs-lookup"><span data-stu-id="3a04b-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3a04b-116">Вызов успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="3a04b-116">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span data-ttu-id="3a04b-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**Лсервер \_ \_Недопустимый \_ маркер "E** " (5005)</span><span class="sxs-lookup"><span data-stu-id="3a04b-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER\_E\_INVALID\_HANDLE** (5005)</span></span>


</dt> <dd>

<span data-ttu-id="3a04b-118">Недопустимый маркер.</span><span class="sxs-lookup"><span data-stu-id="3a04b-118">The handle is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a04b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a04b-119">Return value</span></span>

<span data-ttu-id="3a04b-120">Эта функция возвращает следующие возможные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="3a04b-120">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="3a04b-121">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="3a04b-121">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="3a04b-122">Вызов прошел.</span><span class="sxs-lookup"><span data-stu-id="3a04b-122">The call succeeded.</span></span> <span data-ttu-id="3a04b-123">Проверьте значение параметра *пдверркоде* , чтобы получить код возврата для вызова.</span><span class="sxs-lookup"><span data-stu-id="3a04b-123">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="3a04b-124">**\_ \_ Недопустимый \_ аргумент RPC S**</span><span class="sxs-lookup"><span data-stu-id="3a04b-124">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="3a04b-125">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="3a04b-125">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a04b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3a04b-126">Requirements</span></span>



| <span data-ttu-id="3a04b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3a04b-127">Requirement</span></span> | <span data-ttu-id="3a04b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3a04b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a04b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a04b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3a04b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a04b-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a04b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a04b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3a04b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a04b-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a04b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3a04b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a04b-134"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a04b-134"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a04b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a04b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a04b-136">**лслиценсе**</span><span class="sxs-lookup"><span data-stu-id="3a04b-136">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="3a04b-137">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="3a04b-137">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="3a04b-138">**тлслиценсинумбегин**</span><span class="sxs-lookup"><span data-stu-id="3a04b-138">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="3a04b-139">**тлслиценсинумнекст**</span><span class="sxs-lookup"><span data-stu-id="3a04b-139">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> </dl>

 

