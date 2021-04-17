---
title: Функция Расадминсервержетинфо (Рассапи. h)
description: Функция Расадминсервержетинфо возвращает конфигурацию сервера RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RAS функции Расадминсервержетинфо
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676015"
---
# <a name="rasadminservergetinfo-function"></a><span data-ttu-id="9f8a0-104">Функция Расадминсервержетинфо</span><span class="sxs-lookup"><span data-stu-id="9f8a0-104">RasAdminServerGetInfo function</span></span>

<span data-ttu-id="9f8a0-105">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="9f8a0-106">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="9f8a0-107">Приложения должны использовать функцию [**мпрадминсервержетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="9f8a0-107">Applications should use the [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) function.\]</span></span>

<span data-ttu-id="9f8a0-108">Функция **расадминсервержетинфо** возвращает конфигурацию сервера RAS.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-108">The **RasAdminServerGetInfo** function gets the server configuration of a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f8a0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f8a0-109">Syntax</span></span>


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a><span data-ttu-id="9f8a0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f8a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f8a0-111">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f8a0-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f8a0-112">Указатель на строку в Юникоде, заканчивающуюся **нулем,** которая указывает имя сервера удаленного доступа Windows NT или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-112">Pointer to a **null**-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="9f8a0-113">Если этот параметр имеет **значение NULL**, функция возвращает сведения о локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-113">If this parameter is **NULL**, the function returns information about the local computer.</span></span> <span data-ttu-id="9f8a0-114">Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-114">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="9f8a0-115">*pRasServer0* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9f8a0-115">*pRasServer0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f8a0-116">Указатель на структуру [**RAS \_ Server \_ 0**](ras-server-0-str.md) , которая получает количество портов, настроенных на сервере, количество используемых в данный момент портов и номер версии сервера.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-116">Pointer to the [**RAS\_SERVER\_0**](ras-server-0-str.md) structure that receives the number of ports configured on the server, the number of ports currently in use, and the server version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f8a0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f8a0-117">Return value</span></span>

<span data-ttu-id="9f8a0-118">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9f8a0-119">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-119">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="9f8a0-120">Возможные коды ошибок включают данные, возвращаемые [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) для функции [**каллнамедпипе**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="9f8a0-120">Possible error codes include those returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) function.</span></span> <span data-ttu-id="9f8a0-121">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-121">There is no extended error information for this function; do not call **GetLastError**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f8a0-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f8a0-122">Remarks</span></span>

<span data-ttu-id="9f8a0-123">Чтобы перечислить все серверы RAS в домене, вызовите функцию [**нетсерверенум**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) и укажите \_ тип ООКП \_ для параметра *serverType* .</span><span class="sxs-lookup"><span data-stu-id="9f8a0-123">To enumerate all RAS servers in a domain, call the [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) function and specify SV\_TYPE\_DIALIN for the *servertype* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f8a0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9f8a0-124">Requirements</span></span>



| <span data-ttu-id="9f8a0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9f8a0-125">Requirement</span></span> | <span data-ttu-id="9f8a0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9f8a0-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8a0-127">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9f8a0-127">End of client support</span></span><br/> | <span data-ttu-id="9f8a0-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9f8a0-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="9f8a0-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9f8a0-129">End of server support</span></span><br/> | <span data-ttu-id="9f8a0-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f8a0-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="9f8a0-131">Header</span><span class="sxs-lookup"><span data-stu-id="9f8a0-131">Header</span></span><br/>                | <dl> <span data-ttu-id="9f8a0-132"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f8a0-132"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f8a0-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f8a0-133">Library</span></span><br/>               | <dl> <span data-ttu-id="9f8a0-134"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f8a0-134"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f8a0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9f8a0-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9f8a0-136"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f8a0-136"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f8a0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f8a0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f8a0-138">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="9f8a0-138">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="9f8a0-139">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="9f8a0-139">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="9f8a0-140">**нетсерверенум**</span><span class="sxs-lookup"><span data-stu-id="9f8a0-140">**NetServerEnum**</span></span>](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[<span data-ttu-id="9f8a0-141">**\_Сервер RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="9f8a0-141">**RAS\_SERVER\_0**</span></span>](ras-server-0-str.md)
</dt> </dl>

 

