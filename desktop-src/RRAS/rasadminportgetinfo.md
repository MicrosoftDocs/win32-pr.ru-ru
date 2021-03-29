---
title: Функция Расадминпортжетинфо (Рассапи. h)
description: Функция Расадминпортжетинфо извлекает сведения об указанном порте на указанном сервере.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RAS функции Расадминпортжетинфо
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676016"
---
# <a name="rasadminportgetinfo-function"></a><span data-ttu-id="c85b3-104">Функция Расадминпортжетинфо</span><span class="sxs-lookup"><span data-stu-id="c85b3-104">RasAdminPortGetInfo function</span></span>

<span data-ttu-id="c85b3-105">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="c85b3-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="c85b3-106">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c85b3-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="c85b3-107">Приложения должны использовать функцию [**мпрадминпортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="c85b3-107">Applications should use the [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) function.\]</span></span>

<span data-ttu-id="c85b3-108">Функция **расадминпортжетинфо** извлекает сведения об указанном порте на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="c85b3-108">The **RasAdminPortGetInfo** function retrieves information about a specified port on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c85b3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c85b3-109">Syntax</span></span>


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a><span data-ttu-id="c85b3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c85b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c85b3-111">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c85b3-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c85b3-112">Указатель на строку в Юникоде, заканчивающуюся нулем и указывающую имя сервера RAS.</span><span class="sxs-lookup"><span data-stu-id="c85b3-112">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="c85b3-113">Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="c85b3-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="c85b3-114">*лпсзпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c85b3-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c85b3-115">Указатель на строку в Юникоде, заканчивающуюся нулем и указывающую имя порта на сервере.</span><span class="sxs-lookup"><span data-stu-id="c85b3-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> <dt>

<span data-ttu-id="c85b3-116">*pRasPort1* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c85b3-116">*pRasPort1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c85b3-117">Указатель на структуру [**\_ порта RAS \_ 1**](ras-port-1-str.md) , которая заполняется функцией, с информацией о состоянии порта.</span><span class="sxs-lookup"><span data-stu-id="c85b3-117">Pointer to the [**RAS\_PORT\_1**](ras-port-1-str.md) structure that the function fills in with information about the state of the port.</span></span>

</dd> <dt>

<span data-ttu-id="c85b3-118">*прасстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c85b3-118">*pRasStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c85b3-119">Указатель на структуру [**\_ \_ статистики порта RAS**](ras-port-statistics-str.md) , которую функция заполняет с помощью статистики по порту.</span><span class="sxs-lookup"><span data-stu-id="c85b3-119">Pointer to the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure that the function fills in with statistics about the port.</span></span>

</dd> <dt>

<span data-ttu-id="c85b3-120">*ппраспарамс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c85b3-120">*ppRasParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c85b3-121">Указатель на переменную указателя, которая получает адрес массива [**\_ параметров службы RAS**](ras-parameters-str.md) .</span><span class="sxs-lookup"><span data-stu-id="c85b3-121">Pointer to a pointer variable that receives the address of an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures.</span></span> <span data-ttu-id="c85b3-122">Каждая структура содержит имя ключа для конкретного носителя, например МАКСКОННЕКТБПС, и связанное с ним значение.</span><span class="sxs-lookup"><span data-stu-id="c85b3-122">Each structure contains the name of a media-specific key, such as MAXCONNECTBPS, and its associated value.</span></span> <span data-ttu-id="c85b3-123">Когда приложение завершит работу с этой памятью, освободите его, вызвав функцию [**расадминфрибуффер**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c85b3-123">When the application is finished with this memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c85b3-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c85b3-124">Return value</span></span>

<span data-ttu-id="c85b3-125">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c85b3-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c85b3-126">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="c85b3-126">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="c85b3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c85b3-127">Value</span></span>                                                                                                     | <span data-ttu-id="c85b3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c85b3-128">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c85b3-129"><dt>**Ошибка \_ dev \_ не \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="c85b3-129"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl>     | <span data-ttu-id="c85b3-130">Указан недопустимый порт.</span><span class="sxs-lookup"><span data-stu-id="c85b3-130">The specified port is invalid.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c85b3-131"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="c85b3-131"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="c85b3-132">Недостаточно памяти для выделения буфера для массива *ппраспарамс* .</span><span class="sxs-lookup"><span data-stu-id="c85b3-132">Insufficient memory to allocate a buffer for the *ppRasParams* array.</span></span><br/> |



 

<span data-ttu-id="c85b3-133">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c85b3-133">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="c85b3-134">Требования</span><span class="sxs-lookup"><span data-stu-id="c85b3-134">Requirements</span></span>



| <span data-ttu-id="c85b3-135">Требование</span><span class="sxs-lookup"><span data-stu-id="c85b3-135">Requirement</span></span> | <span data-ttu-id="c85b3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="c85b3-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c85b3-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c85b3-137">End of client support</span></span><br/> | <span data-ttu-id="c85b3-138">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c85b3-138">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="c85b3-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c85b3-139">End of server support</span></span><br/> | <span data-ttu-id="c85b3-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c85b3-140">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="c85b3-141">Header</span><span class="sxs-lookup"><span data-stu-id="c85b3-141">Header</span></span><br/>                | <dl> <span data-ttu-id="c85b3-142"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c85b3-142"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c85b3-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c85b3-143">Library</span></span><br/>               | <dl> <span data-ttu-id="c85b3-144"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c85b3-144"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c85b3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c85b3-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c85b3-146"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c85b3-146"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c85b3-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c85b3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85b3-148">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="c85b3-148">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c85b3-149">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="c85b3-149">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="c85b3-150">**\_Параметры RAS**</span><span class="sxs-lookup"><span data-stu-id="c85b3-150">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="c85b3-151">**\_Порт RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c85b3-151">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="c85b3-152">**\_Статистика порта \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="c85b3-152">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="c85b3-153">**расадминфрибуффер**</span><span class="sxs-lookup"><span data-stu-id="c85b3-153">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

