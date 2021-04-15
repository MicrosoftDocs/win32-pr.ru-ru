---
title: Функция Расадминусерсетинфо (Рассапи. h)
description: Функция Расадминусерсетинфо устанавливает разрешения RAS и номер телефона обратного вызова для указанного пользователя.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RAS функции Расадминусерсетинфо
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648729"
---
# <a name="rasadminusersetinfo-function"></a><span data-ttu-id="799c3-104">Функция Расадминусерсетинфо</span><span class="sxs-lookup"><span data-stu-id="799c3-104">RasAdminUserSetInfo function</span></span>

<span data-ttu-id="799c3-105">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="799c3-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="799c3-106">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="799c3-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="799c3-107">Приложения должны использовать функцию [**мпрадминусерсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="799c3-107">Applications should use the [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) function.\]</span></span>

<span data-ttu-id="799c3-108">Функция **расадминусерсетинфо** устанавливает разрешения RAS и номер телефона обратного вызова для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="799c3-108">The **RasAdminUserSetInfo** function sets the RAS permissions and call-back phone number for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="799c3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="799c3-109">Syntax</span></span>


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="799c3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="799c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="799c3-111">*лпсзусераккаунтсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="799c3-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="799c3-112">Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя основного или резервного контроллера домена с базой данных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="799c3-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="799c3-113">Используйте функцию [**расадминжетусераккаунтсервер**](rasadmingetuseraccountserver.md) для получения имени этого сервера.</span><span class="sxs-lookup"><span data-stu-id="799c3-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="799c3-114">*лпсзусер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="799c3-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="799c3-115">Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя пользователя, для которого задаются сведения RAS.</span><span class="sxs-lookup"><span data-stu-id="799c3-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom RAS information is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="799c3-116">*pRasUser0* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="799c3-116">*pRasUser0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="799c3-117">Указатель на структуру [**\_ пользователя RAS \_ 0**](ras-user-0-str.md) , указывающий новые данные RAS для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="799c3-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that specifies the new RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="799c3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="799c3-118">Return value</span></span>

<span data-ttu-id="799c3-119">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="799c3-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="799c3-120">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="799c3-120">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="799c3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="799c3-121">Value</span></span>                                                                                                           | <span data-ttu-id="799c3-122">Описание</span><span class="sxs-lookup"><span data-stu-id="799c3-122">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="799c3-123"><dt>**Ошибка при \_ недопустимых \_ данных**</dt></span><span class="sxs-lookup"><span data-stu-id="799c3-123"><dt>**ERROR\_INVALID\_DATA**</dt></span></span> </dl>             | <span data-ttu-id="799c3-124">Буфер *pRasUser0* содержит недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="799c3-124">The *pRasUser0* buffer contains invalid data.</span></span><br/>                                        |
| <dl> <span data-ttu-id="799c3-125"><dt>**Ошибка \_ недопустимого \_ номера обратного вызова \_**</dt></span><span class="sxs-lookup"><span data-stu-id="799c3-125"><dt>**ERROR\_INVALID\_CALLBACK\_NUMBER**</dt></span></span> </dl> | <span data-ttu-id="799c3-126">Номер обратного вызова, указанный в буфере *pRasUser0* , содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="799c3-126">The callback number specified in the *pRasUser0* buffer contains invalid characters.</span></span><br/> |
| <dl> <span data-ttu-id="799c3-127"><dt>**Нерр \_ Буфтусмалл**</dt></span><span class="sxs-lookup"><span data-stu-id="799c3-127"><dt>**NERR\_BufTooSmall** </dt></span></span> </dl>               | <span data-ttu-id="799c3-128">Недостаточно памяти для выполнения этой функции.</span><span class="sxs-lookup"><span data-stu-id="799c3-128">Insufficient memory to perform this function.</span></span><br/>                                        |



 

<span data-ttu-id="799c3-129">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="799c3-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="799c3-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="799c3-130">Remarks</span></span>

<span data-ttu-id="799c3-131">При установке разрешений RAS для пользователя элемент **бфпривилеже** структуры [**\_ пользователя RAS \_ 0**](ras-user-0-str.md) должен указать по меньшей мере один из флагов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="799c3-131">When setting the RAS permissions for a user, the **bfPrivilege** member of the [**RAS\_USER\_0**](ras-user-0-str.md) structure must specify at least one of the call-back flags.</span></span> <span data-ttu-id="799c3-132">Например, чтобы задать права пользователя на разрешение удаленного доступа, но нет прав на обратную связь, задайте для **бфпривилеже** значение расприв \_ диалинпривилеже \| расприв \_ callback.</span><span class="sxs-lookup"><span data-stu-id="799c3-132">For example, to set a user's privileges to allow dial-in privilege but no call-back privilege, set **bfPrivilege** to RASPRIV\_DialinPrivilege \| RASPRIV\_NoCallback.</span></span>

## <a name="requirements"></a><span data-ttu-id="799c3-133">Требования</span><span class="sxs-lookup"><span data-stu-id="799c3-133">Requirements</span></span>



| <span data-ttu-id="799c3-134">Требование</span><span class="sxs-lookup"><span data-stu-id="799c3-134">Requirement</span></span> | <span data-ttu-id="799c3-135">Значение</span><span class="sxs-lookup"><span data-stu-id="799c3-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="799c3-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="799c3-136">End of client support</span></span><br/> | <span data-ttu-id="799c3-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="799c3-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="799c3-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="799c3-138">End of server support</span></span><br/> | <span data-ttu-id="799c3-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="799c3-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="799c3-140">Header</span><span class="sxs-lookup"><span data-stu-id="799c3-140">Header</span></span><br/>                | <dl> <span data-ttu-id="799c3-141"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="799c3-141"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="799c3-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="799c3-142">Library</span></span><br/>               | <dl> <span data-ttu-id="799c3-143"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="799c3-143"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="799c3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="799c3-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="799c3-145"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="799c3-145"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="799c3-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="799c3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="799c3-147">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="799c3-147">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="799c3-148">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="799c3-148">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="799c3-149">**\_Пользователь RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="799c3-149">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="799c3-150">**расадминжетусераккаунтсервер**</span><span class="sxs-lookup"><span data-stu-id="799c3-150">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="799c3-151">**расадминусержетинфо**</span><span class="sxs-lookup"><span data-stu-id="799c3-151">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> </dl>

 

