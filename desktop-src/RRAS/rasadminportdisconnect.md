---
title: Функция Расадминпортдисконнект (Рассапи. h)
description: Функция Расадминпортдисконнект отключает порт, который используется в данный момент.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RAS функции Расадминпортдисконнект
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676017"
---
# <a name="rasadminportdisconnect-function"></a><span data-ttu-id="c6f3b-104">Функция Расадминпортдисконнект</span><span class="sxs-lookup"><span data-stu-id="c6f3b-104">RasAdminPortDisconnect function</span></span>

<span data-ttu-id="c6f3b-105">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="c6f3b-106">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="c6f3b-107">Приложения должны использовать функцию [**мпрадминпортдисконнект**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]</span><span class="sxs-lookup"><span data-stu-id="c6f3b-107">Applications should use the [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) function.\]</span></span>

<span data-ttu-id="c6f3b-108">Функция **расадминпортдисконнект** отключает порт, который используется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-108">The **RasAdminPortDisconnect** function disconnects a port that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f3b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6f3b-109">Syntax</span></span>


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="c6f3b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6f3b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6f3b-111">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6f3b-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f3b-112">Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя сервера удаленного доступа Windows NT или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-112">Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="c6f3b-113">Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="c6f3b-114">*лпсзпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6f3b-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f3b-115">Указатель на строку в Юникоде, заканчивающуюся нулем и указывающую имя порта на сервере.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6f3b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6f3b-116">Return value</span></span>

<span data-ttu-id="c6f3b-117">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c6f3b-118">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-118">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="c6f3b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c6f3b-119">Value</span></span>                                                                                               | <span data-ttu-id="c6f3b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c6f3b-120">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c6f3b-121"><dt>**Ошибка \_ недопустимого \_ порта**</dt></span><span class="sxs-lookup"><span data-stu-id="c6f3b-121"><dt>**ERROR\_INVALID\_PORT**</dt></span></span> </dl> | <span data-ttu-id="c6f3b-122">Указан недопустимый порт.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-122">The specified port is invalid.</span></span><br/>    |
| <dl> <span data-ttu-id="c6f3b-123"><dt>**НЕРР \_ усернотфаунд**</dt></span><span class="sxs-lookup"><span data-stu-id="c6f3b-123"><dt>**NERR\_UserNotFound**</dt></span></span> </dl>   | <span data-ttu-id="c6f3b-124">Порт сейчас не используется.</span><span class="sxs-lookup"><span data-stu-id="c6f3b-124">The port is not currently in use.</span></span><br/> |



 

<span data-ttu-id="c6f3b-125">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c6f3b-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6f3b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c6f3b-126">Requirements</span></span>



| <span data-ttu-id="c6f3b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c6f3b-127">Requirement</span></span> | <span data-ttu-id="c6f3b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c6f3b-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f3b-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c6f3b-129">End of client support</span></span><br/> | <span data-ttu-id="c6f3b-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c6f3b-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="c6f3b-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c6f3b-131">End of server support</span></span><br/> | <span data-ttu-id="c6f3b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6f3b-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="c6f3b-133">Header</span><span class="sxs-lookup"><span data-stu-id="c6f3b-133">Header</span></span><br/>                | <dl> <span data-ttu-id="c6f3b-134"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6f3b-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6f3b-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c6f3b-135">Library</span></span><br/>               | <dl> <span data-ttu-id="c6f3b-136"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6f3b-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6f3b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c6f3b-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c6f3b-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6f3b-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6f3b-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6f3b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f3b-140">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="c6f3b-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c6f3b-141">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="c6f3b-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> </dl>

 

