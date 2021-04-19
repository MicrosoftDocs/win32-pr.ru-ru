---
title: Функция Расадминусержетинфо (Рассапи. h)
description: Функция Расадминусержетинфо получает разрешения RAS и сведения о номере телефона обратного вызова для указанного пользователя.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RAS функции Расадминусержетинфо
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675457"
---
# <a name="rasadminusergetinfo-function"></a><span data-ttu-id="21a09-104">Функция Расадминусержетинфо</span><span class="sxs-lookup"><span data-stu-id="21a09-104">RasAdminUserGetInfo function</span></span>

<span data-ttu-id="21a09-105">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="21a09-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="21a09-106">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="21a09-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="21a09-107">Приложения должны использовать функцию [**мпрадминусержетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="21a09-107">Applications should use the [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) function.\]</span></span>

<span data-ttu-id="21a09-108">Функция **расадминусержетинфо** получает разрешения RAS и сведения о номере телефона обратного вызова для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="21a09-108">The **RasAdminUserGetInfo** function gets the RAS permissions and callback phone number information for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a09-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21a09-109">Syntax</span></span>


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="21a09-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="21a09-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21a09-111">*лпсзусераккаунтсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21a09-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21a09-112">Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя основного или резервного контроллера домена с базой данных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="21a09-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="21a09-113">Используйте функцию [**расадминжетусераккаунтсервер**](rasadmingetuseraccountserver.md) для получения имени этого сервера.</span><span class="sxs-lookup"><span data-stu-id="21a09-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="21a09-114">*лпсзусер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21a09-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21a09-115">Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя пользователя, для которого необходимо получить сведения об RAS.</span><span class="sxs-lookup"><span data-stu-id="21a09-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom to get RAS information.</span></span>

</dd> <dt>

<span data-ttu-id="21a09-116">*pRasUser0*</span><span class="sxs-lookup"><span data-stu-id="21a09-116">*pRasUser0*</span></span> 
</dt> <dd>

<span data-ttu-id="21a09-117">Указатель на структуру [**\_ пользователя RAS \_ 0**](ras-user-0-str.md) , которая получает данные RAS для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="21a09-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that receives the RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21a09-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21a09-118">Return value</span></span>

<span data-ttu-id="21a09-119">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="21a09-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="21a09-120">Если функция завершается ошибкой, возвращаемое значение может быть следующим кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="21a09-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="21a09-121">Значение</span><span class="sxs-lookup"><span data-stu-id="21a09-121">Value</span></span>                                                                                            | <span data-ttu-id="21a09-122">Значение</span><span class="sxs-lookup"><span data-stu-id="21a09-122">Meaning</span></span>                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="21a09-123"><dt>**НЕРР \_ буфтусмалл**</dt></span><span class="sxs-lookup"><span data-stu-id="21a09-123"><dt>**NERR\_BufTooSmall**</dt></span></span> </dl> | <span data-ttu-id="21a09-124">Недостаточно памяти для выполнения этой функции.</span><span class="sxs-lookup"><span data-stu-id="21a09-124">Insufficient memory to perform this function.</span></span><br/> |



 

<span data-ttu-id="21a09-125">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="21a09-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="21a09-126">Требования</span><span class="sxs-lookup"><span data-stu-id="21a09-126">Requirements</span></span>



| <span data-ttu-id="21a09-127">Требование</span><span class="sxs-lookup"><span data-stu-id="21a09-127">Requirement</span></span> | <span data-ttu-id="21a09-128">Значение</span><span class="sxs-lookup"><span data-stu-id="21a09-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21a09-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="21a09-129">End of client support</span></span><br/> | <span data-ttu-id="21a09-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="21a09-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="21a09-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="21a09-131">End of server support</span></span><br/> | <span data-ttu-id="21a09-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21a09-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="21a09-133">Header</span><span class="sxs-lookup"><span data-stu-id="21a09-133">Header</span></span><br/>                | <dl> <span data-ttu-id="21a09-134"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="21a09-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="21a09-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21a09-135">Library</span></span><br/>               | <dl> <span data-ttu-id="21a09-136"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21a09-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="21a09-137">DLL</span><span class="sxs-lookup"><span data-stu-id="21a09-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="21a09-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21a09-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a09-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21a09-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a09-140">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="21a09-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="21a09-141">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="21a09-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="21a09-142">**\_Пользователь RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="21a09-142">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="21a09-143">**расадминжетусераккаунтсервер**</span><span class="sxs-lookup"><span data-stu-id="21a09-143">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="21a09-144">**расадминусерсетинфо**</span><span class="sxs-lookup"><span data-stu-id="21a09-144">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

