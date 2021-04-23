---
title: Функция Расадминпортенум (Рассапи. h)
description: Функция Расадминпортенум перечисляет все порты на указанном сервере RAS. Для каждого порта на сервере функция возвращает \_ структуру порта RAS \_ 0, содержащую сведения о порте.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RAS функции Расадминпортенум
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648718"
---
# <a name="rasadminportenum-function"></a><span data-ttu-id="7847d-105">Функция Расадминпортенум</span><span class="sxs-lookup"><span data-stu-id="7847d-105">RasAdminPortEnum function</span></span>

<span data-ttu-id="7847d-106">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="7847d-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="7847d-107">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7847d-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="7847d-108">Приложения должны использовать функцию [**мпрадминпортенум**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]</span><span class="sxs-lookup"><span data-stu-id="7847d-108">Applications should use the [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) function.\]</span></span>

<span data-ttu-id="7847d-109">Функция **расадминпортенум** перечисляет все порты на указанном сервере RAS.</span><span class="sxs-lookup"><span data-stu-id="7847d-109">The **RasAdminPortEnum** function enumerates all ports on the specified RAS server.</span></span> <span data-ttu-id="7847d-110">Для каждого порта на сервере функция возвращает структуру [**\_ порта RAS \_ 0**](ras-port-0-str.md) , содержащую сведения о порте.</span><span class="sxs-lookup"><span data-stu-id="7847d-110">For each port on the server, the function returns the [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port.</span></span>

## <a name="syntax"></a><span data-ttu-id="7847d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7847d-111">Syntax</span></span>


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a><span data-ttu-id="7847d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7847d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7847d-113">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7847d-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7847d-114">Указатель на строку в Юникоде, заканчивающуюся нулем и указывающую имя сервера RAS.</span><span class="sxs-lookup"><span data-stu-id="7847d-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="7847d-115">Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="7847d-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="7847d-116">*ppRasPort0* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7847d-116">*ppRasPort0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7847d-117">Указатель на переменную, которая получает указатель на буфер, содержащий массив структур [**\_ порта RAS \_ 0**](ras-port-0-str.md) .</span><span class="sxs-lookup"><span data-stu-id="7847d-117">Pointer to a variable that receives a pointer to a buffer that contains an array of [**RAS\_PORT\_0**](ras-port-0-str.md) structures.</span></span> <span data-ttu-id="7847d-118">Когда приложение завершит работу с памятью, освободите его, вызвав функцию [**расадминфрибуффер**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7847d-118">When the application has finished with the memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7847d-119">*пцентриесреад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7847d-119">*pcEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7847d-120">Указатель на 16-разрядную переменную, которая получает общее число [**структур \_ порта RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) , возвращаемых в массиве *ppRasPort0* .</span><span class="sxs-lookup"><span data-stu-id="7847d-120">Pointer to a 16-bit variable that receives the total number of [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) structures returned in the *ppRasPort0* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7847d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7847d-121">Return value</span></span>

<span data-ttu-id="7847d-122">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7847d-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="7847d-123">Если функция завершается ошибкой, возвращаемое значение может быть следующим кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="7847d-123">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="7847d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7847d-124">Value</span></span>                                                                                             | <span data-ttu-id="7847d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7847d-125">Meaning</span></span>                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7847d-126"><dt>**НЕРР \_ итемнотфаунд**</dt></span><span class="sxs-lookup"><span data-stu-id="7847d-126"><dt>**NERR\_ItemNotFound**</dt></span></span> </dl> | <span data-ttu-id="7847d-127">Не удалось перечислить порты.</span><span class="sxs-lookup"><span data-stu-id="7847d-127">No ports could be enumerated.</span></span> <span data-ttu-id="7847d-128">Это может быть вызвано тем, что все настроенные порты на сервере в настоящее время используются для исходящих вызовов.</span><span class="sxs-lookup"><span data-stu-id="7847d-128">This could be because all configured ports on the server are currently being used for dialing out.</span></span><br/> |



 

<span data-ttu-id="7847d-129">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7847d-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="7847d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7847d-130">Requirements</span></span>



| <span data-ttu-id="7847d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7847d-131">Requirement</span></span> | <span data-ttu-id="7847d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7847d-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7847d-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7847d-133">End of client support</span></span><br/> | <span data-ttu-id="7847d-134">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7847d-134">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="7847d-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7847d-135">End of server support</span></span><br/> | <span data-ttu-id="7847d-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7847d-136">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="7847d-137">Header</span><span class="sxs-lookup"><span data-stu-id="7847d-137">Header</span></span><br/>                | <dl> <span data-ttu-id="7847d-138"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7847d-138"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="7847d-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7847d-139">Library</span></span><br/>               | <dl> <span data-ttu-id="7847d-140"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7847d-140"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7847d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7847d-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7847d-142"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7847d-142"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7847d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7847d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7847d-144">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="7847d-144">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="7847d-145">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="7847d-145">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="7847d-146">**\_Порт RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="7847d-146">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="7847d-147">**расадминфрибуффер**</span><span class="sxs-lookup"><span data-stu-id="7847d-147">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

