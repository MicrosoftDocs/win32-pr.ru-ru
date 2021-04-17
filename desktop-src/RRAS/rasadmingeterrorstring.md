---
title: Функция Расадминжетеррорстринг (Рассапи. h)
description: Функция Расадминжетеррорстринг извлекает строку сообщения, соответствующую коду ошибки RAS, возвращенному одной из функций администрирования сервера RAS (Расадмин).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RAS функции Расадминжетеррорстринг
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651877"
---
# <a name="rasadmingeterrorstring-function"></a><span data-ttu-id="81eaf-104">Функция Расадминжетеррорстринг</span><span class="sxs-lookup"><span data-stu-id="81eaf-104">RasAdminGetErrorString function</span></span>

<span data-ttu-id="81eaf-105">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="81eaf-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="81eaf-106">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="81eaf-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="81eaf-107">Приложения должны использовать функцию [**мпрадминжетеррорстринг**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]</span><span class="sxs-lookup"><span data-stu-id="81eaf-107">Applications should use the [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) function.\]</span></span>

<span data-ttu-id="81eaf-108">Функция **расадминжетеррорстринг** извлекает строку сообщения, соответствующую коду ошибки RAS, возвращенному одной из функций администрирования сервера RAS (расадмин).</span><span class="sxs-lookup"><span data-stu-id="81eaf-108">The **RasAdminGetErrorString** function retrieves a message string that corresponds to a RAS error code returned by one of the RAS server administration (RasAdmin) functions.</span></span> <span data-ttu-id="81eaf-109">Эти строки сообщений извлекаются из Rasmsg.dll, который устанавливается в составе службы удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="81eaf-109">These message strings are retrieved from the Rasmsg.dll that is installed as part of RAS.</span></span>

## <a name="syntax"></a><span data-ttu-id="81eaf-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81eaf-110">Syntax</span></span>


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="81eaf-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="81eaf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81eaf-112">*ResourceId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81eaf-112">*ResourceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81eaf-113">Указывает код ошибки, возвращенный одной из функций Расадмин.</span><span class="sxs-lookup"><span data-stu-id="81eaf-113">Specifies an error code returned by one of the RasAdmin functions.</span></span> <span data-ttu-id="81eaf-114">Это значение должно находиться в диапазоне кодов ошибок от РАСБАСЕ до РАСБАСИНД.</span><span class="sxs-lookup"><span data-stu-id="81eaf-114">This value must be in the range of error codes from RASBASE to RASBASEEND.</span></span> <span data-ttu-id="81eaf-115">Они определены в Расеррор. h.</span><span class="sxs-lookup"><span data-stu-id="81eaf-115">These are defined in Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="81eaf-116">*лпсзстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81eaf-116">*lpszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81eaf-117">Указатель на буфер, который получает сообщение об ошибке, соответствующее указанному коду ошибки.</span><span class="sxs-lookup"><span data-stu-id="81eaf-117">Pointer to a buffer that receives the error message that corresponds to the specified error code.</span></span>

</dd> <dt>

<span data-ttu-id="81eaf-118">*Инбуфсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81eaf-118">*InBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81eaf-119">Задает размер буфера *лпсзстринг* в символах.</span><span class="sxs-lookup"><span data-stu-id="81eaf-119">Specifies the size, in characters, of the *lpszString* buffer.</span></span> <span data-ttu-id="81eaf-120">Сообщения об ошибках обычно 80 символов или меньше; Размер буфера, равный 512 символам, всегда является достаточным.</span><span class="sxs-lookup"><span data-stu-id="81eaf-120">Error messages are typically 80 characters or less; a buffer size of 512 characters is always adequate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81eaf-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81eaf-121">Return value</span></span>

<span data-ttu-id="81eaf-122">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="81eaf-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="81eaf-123">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="81eaf-123">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="81eaf-124">Это значение может быть последним значением ошибки, установленным функциями [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)или [**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa) . или может быть одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="81eaf-124">This value can be a last error value set by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc), or [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) functions; or it can be one of the following error codes.</span></span>



| <span data-ttu-id="81eaf-125">Значение</span><span class="sxs-lookup"><span data-stu-id="81eaf-125">Value</span></span>                                                                                                      | <span data-ttu-id="81eaf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="81eaf-126">Meaning</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81eaf-127"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="81eaf-127"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="81eaf-128">Недопустимые параметры *ResourceId* или *лпсзстринг* .</span><span class="sxs-lookup"><span data-stu-id="81eaf-128">The *ResourceId* or *lpszString* parameters are invalid.</span></span><br/>      |
| <dl> <span data-ttu-id="81eaf-129"><dt>**Ошибка \_ недостаточного \_ буфера**</dt></span><span class="sxs-lookup"><span data-stu-id="81eaf-129"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="81eaf-130">Размер, указанный в параметре *инбуфсизе* , слишком мал.</span><span class="sxs-lookup"><span data-stu-id="81eaf-130">The size specified by the *InBufSize* parameter is too small.</span></span><br/> |



 

<span data-ttu-id="81eaf-131">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="81eaf-131">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="81eaf-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81eaf-132">Remarks</span></span>

<span data-ttu-id="81eaf-133">Функции Расадмин могут возвращать коды ошибок, которые не находятся в диапазоне, поддерживаемом функцией **расадминжетеррорстринг** .</span><span class="sxs-lookup"><span data-stu-id="81eaf-133">The RasAdmin functions can return error codes that are not in the range supported by the **RasAdminGetErrorString** function.</span></span> <span data-ttu-id="81eaf-134">Например, функции Расадмин могут возвращать коды ошибок, определенные в Лмерр. h и Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="81eaf-134">For example, the RasAdmin functions can return error codes that are defined in Lmerr.h and Winerror.h.</span></span> <span data-ttu-id="81eaf-135">Перед вызовом **расадминжетеррорстринг** убедитесь, что код ошибки находится в диапазоне от РАСБАСЕ до расбасинд, как определено в расеррор. h.</span><span class="sxs-lookup"><span data-stu-id="81eaf-135">Before calling **RasAdminGetErrorString**, verify that the error code is in the range RASBASE to RASBASEEND, as defined in Raserror.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="81eaf-136">Требования</span><span class="sxs-lookup"><span data-stu-id="81eaf-136">Requirements</span></span>



| <span data-ttu-id="81eaf-137">Требование</span><span class="sxs-lookup"><span data-stu-id="81eaf-137">Requirement</span></span> | <span data-ttu-id="81eaf-138">Значение</span><span class="sxs-lookup"><span data-stu-id="81eaf-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81eaf-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="81eaf-139">End of client support</span></span><br/> | <span data-ttu-id="81eaf-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="81eaf-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="81eaf-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="81eaf-141">End of server support</span></span><br/> | <span data-ttu-id="81eaf-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81eaf-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="81eaf-143">Header</span><span class="sxs-lookup"><span data-stu-id="81eaf-143">Header</span></span><br/>                | <dl> <span data-ttu-id="81eaf-144"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="81eaf-144"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="81eaf-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81eaf-145">Library</span></span><br/>               | <dl> <span data-ttu-id="81eaf-146"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81eaf-146"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="81eaf-147">DLL</span><span class="sxs-lookup"><span data-stu-id="81eaf-147">DLL</span></span><br/>                   | <dl> <span data-ttu-id="81eaf-148"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81eaf-148"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81eaf-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81eaf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81eaf-150">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="81eaf-150">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="81eaf-151">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="81eaf-151">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="81eaf-152">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="81eaf-152">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="81eaf-153">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="81eaf-153">**GlobalAlloc**</span></span>](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[<span data-ttu-id="81eaf-154">**лоадстринг**</span><span class="sxs-lookup"><span data-stu-id="81eaf-154">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

