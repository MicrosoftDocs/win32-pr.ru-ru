---
title: Функция Расадминжетусераккаунтсервер (Рассапи. h)
description: Функция Расадминжетусераккаунтсервер извлекает имя сервера, на котором находится база данных учетных записей пользователей. Используйте возвращенное имя сервера в функциях Расадминусержетинфо и Расадминусерсетинфо, чтобы получить или задать сведения об указанном пользователе.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RAS функции Расадминжетусераккаунтсервер
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675458"
---
# <a name="rasadmingetuseraccountserver-function"></a><span data-ttu-id="1770b-105">Функция Расадминжетусераккаунтсервер</span><span class="sxs-lookup"><span data-stu-id="1770b-105">RasAdminGetUserAccountServer function</span></span>

<span data-ttu-id="1770b-106">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="1770b-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="1770b-107">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1770b-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="1770b-108">Приложения должны использовать функцию [**мпрадминжетпдксервер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]</span><span class="sxs-lookup"><span data-stu-id="1770b-108">Applications should use the [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) function.\]</span></span>

<span data-ttu-id="1770b-109">Функция **расадминжетусераккаунтсервер** извлекает имя сервера, на котором находится база данных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="1770b-109">The **RasAdminGetUserAccountServer** function retrieves the name of the server that has the user account database.</span></span> <span data-ttu-id="1770b-110">Используйте возвращенное имя сервера в функциях [**расадминусержетинфо**](rasadminusergetinfo.md) и [**расадминусерсетинфо**](rasadminusersetinfo.md) , чтобы получить или задать сведения об указанном пользователе.</span><span class="sxs-lookup"><span data-stu-id="1770b-110">Use the returned server name in the [**RasAdminUserGetInfo**](rasadminusergetinfo.md) and [**RasAdminUserSetInfo**](rasadminusersetinfo.md) functions to get or set information about a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="1770b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1770b-111">Syntax</span></span>


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a><span data-ttu-id="1770b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1770b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1770b-113">*лпсздомаин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1770b-113">*lpszDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1770b-114">Указатель на строку в Юникоде, заканчивающуюся **нулем,** которая указывает имя домена, к которому принадлежит RAS-сервер.</span><span class="sxs-lookup"><span data-stu-id="1770b-114">Pointer to a **null**-terminated Unicode string that specifies the name of the domain to which the RAS server belongs.</span></span> <span data-ttu-id="1770b-115">Этот параметр имеет **значение NULL** для приложений администрирования RAS, выполняемых на рабочих станциях или серверах, которые не являются членами домена.</span><span class="sxs-lookup"><span data-stu-id="1770b-115">This parameter is **NULL** for the RAS administration applications running on workstations or servers that are not members of a domain.</span></span> <span data-ttu-id="1770b-116">Если этот параметр имеет **значение NULL**, параметр *Лпсзсервер* должен иметь значение, отличное от **null**.</span><span class="sxs-lookup"><span data-stu-id="1770b-116">If this parameter is **NULL**, the *lpszServer* parameter must be non-**NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1770b-117">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1770b-117">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1770b-118">Указатель на строку **в Юникоде**, заканчивающуюся нулем и указывающую имя сервера RAS.</span><span class="sxs-lookup"><span data-stu-id="1770b-118">Pointer to a **null**-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="1770b-119">Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="1770b-119">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span> <span data-ttu-id="1770b-120">Этот параметр может иметь **значение NULL** , если параметр *лпсздомаин* имеет **значение**, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="1770b-120">This parameter can be **NULL** if the *lpszDomain* parameter is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1770b-121">*лпсзусераккаунтсервер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1770b-121">*lpszUserAccountServer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1770b-122">Указатель на буфер, который получает строку в Юникоде, заканчивающуюся **нулем**, которая указывает имя контроллера домена с базой данных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="1770b-122">Pointer to a buffer that receives a **null**-terminated Unicode string that specifies the name of a domain controller that has the user account database.</span></span> <span data-ttu-id="1770b-123">Буфер должен быть достаточно большим, чтобы вместить имя сервера (УНКЛЕН + 1).</span><span class="sxs-lookup"><span data-stu-id="1770b-123">The buffer should be big enough to hold the server name (UNCLEN +1).</span></span> <span data-ttu-id="1770b-124">Функция добавляет префикс к возвращенному имени сервера с ведущими \\ \\ символами "" в формате \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="1770b-124">The function prefixes the returned server name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1770b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1770b-125">Return value</span></span>

<span data-ttu-id="1770b-126">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1770b-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="1770b-127">Если функция завершается ошибкой, возвращаемое значение может быть следующим кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="1770b-127">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="1770b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="1770b-128">Value</span></span>                                                                                                    | <span data-ttu-id="1770b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1770b-129">Meaning</span></span>                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="1770b-130"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="1770b-130"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="1770b-131">*Лпсздомаин* и *Лпсзсервер* имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1770b-131">Both *lpszDomain* and *lpszServer* are **NULL**.</span></span><br/> |



 

<span data-ttu-id="1770b-132">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="1770b-132">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="1770b-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1770b-133">Remarks</span></span>

<span data-ttu-id="1770b-134">Функция **расадминжетусераккаунтсервер** получает имя сервера с базой данных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="1770b-134">The **RasAdminGetUserAccountServer** function obtains the name of the server with the user accounts database.</span></span> <span data-ttu-id="1770b-135">Для этой функции требуется имя сервера RAS или имя домена, в котором находится сервер удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="1770b-135">This function requires the name of the RAS server or the name of the domain in which the RAS server resides.</span></span>

<span data-ttu-id="1770b-136">Параметр *лпсздомаин* должен указывать допустимое имя домена.</span><span class="sxs-lookup"><span data-stu-id="1770b-136">The *lpszDomain* parameter should specify a valid domain name.</span></span> <span data-ttu-id="1770b-137">Этот параметр имеет **значение NULL** для приложений администрирования RAS, работающих на серверах, которые не являются членами домена (например, сервер находится в собственной рабочей группе).</span><span class="sxs-lookup"><span data-stu-id="1770b-137">This parameter is **NULL** for RAS administration applications running on servers that are not members of a domain (for example, the server is in its own workgroup).</span></span> <span data-ttu-id="1770b-138">В этом случае в параметре *лпсзсервер* должно быть указано имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1770b-138">In this case, the *lpszServer* parameter must specify the server name.</span></span> <span data-ttu-id="1770b-139">Чтобы получить имя сервера, вызовите функцию [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) .</span><span class="sxs-lookup"><span data-stu-id="1770b-139">To get the server name, call the [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) function.</span></span> <span data-ttu-id="1770b-140">Обязательно добавьте в имя сервера \\ \\ символы "".</span><span class="sxs-lookup"><span data-stu-id="1770b-140">Be sure to prefix the server name with the "\\\\" characters.</span></span>

<span data-ttu-id="1770b-141">Если имя сервера, указанное параметром *лпсзсервер* , является изолированным сервером (то есть сервер или рабочая станция не является членом домена), то имя сервера возвращается в буфер *лпсзусераккаунтсервер* .</span><span class="sxs-lookup"><span data-stu-id="1770b-141">If the server name specified by *lpszServer* is a stand-alone server (that is, the server or workstation is not a member of a domain), then the server name itself is returned in the *lpszUserAccountServer* buffer.</span></span>

<span data-ttu-id="1770b-142">Затем используйте имя сервера учетных записей пользователей в вызове функции [**неткуеридисплайинформатион**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) , чтобы перечислить пользователей в базе данных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="1770b-142">Then use the name of the user account server in a call to the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function to enumerate the users in the user account database.</span></span>

## <a name="requirements"></a><span data-ttu-id="1770b-143">Требования</span><span class="sxs-lookup"><span data-stu-id="1770b-143">Requirements</span></span>



| <span data-ttu-id="1770b-144">Требование</span><span class="sxs-lookup"><span data-stu-id="1770b-144">Requirement</span></span> | <span data-ttu-id="1770b-145">Значение</span><span class="sxs-lookup"><span data-stu-id="1770b-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1770b-146">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1770b-146">End of client support</span></span><br/> | <span data-ttu-id="1770b-147">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1770b-147">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="1770b-148">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1770b-148">End of server support</span></span><br/> | <span data-ttu-id="1770b-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1770b-149">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="1770b-150">Header</span><span class="sxs-lookup"><span data-stu-id="1770b-150">Header</span></span><br/>                | <dl> <span data-ttu-id="1770b-151"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="1770b-151"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="1770b-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1770b-152">Library</span></span><br/>               | <dl> <span data-ttu-id="1770b-153"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1770b-153"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1770b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="1770b-154">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1770b-155"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1770b-155"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1770b-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1770b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1770b-157">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="1770b-157">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="1770b-158">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="1770b-158">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="1770b-159">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="1770b-159">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[<span data-ttu-id="1770b-160">**расадминусержетинфо**</span><span class="sxs-lookup"><span data-stu-id="1770b-160">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="1770b-161">**расадминусерсетинфо**</span><span class="sxs-lookup"><span data-stu-id="1770b-161">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

