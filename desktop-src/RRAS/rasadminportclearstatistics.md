---
title: Функция Расадминпортклеарстатистикс (Рассапи. h)
description: Функция Расадминпортклеарстатистикс сбрасывает счетчики, представляющие различные статистические данные, сообщаемые функцией Расадминпортжетинфо в \_ \_ структуре статистики порта RAS. Счетчики сбрасываются в нулевое состояние и начинают накапливаться.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RAS функции Расадминпортклеарстатистикс
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648719"
---
# <a name="rasadminportclearstatistics-function"></a><span data-ttu-id="78db4-105">Функция Расадминпортклеарстатистикс</span><span class="sxs-lookup"><span data-stu-id="78db4-105">RasAdminPortClearStatistics function</span></span>

<span data-ttu-id="78db4-106">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="78db4-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="78db4-107">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78db4-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="78db4-108">Приложения должны использовать функцию [**мпрадминпортклеарстатс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]</span><span class="sxs-lookup"><span data-stu-id="78db4-108">Applications should use the [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) function.\]</span></span>

<span data-ttu-id="78db4-109">Функция **расадминпортклеарстатистикс** сбрасывает счетчики, представляющие различные статистические данные, сообщаемые функцией [**расадминпортжетинфо**](rasadminportgetinfo.md) в структуре [**\_ \_ статистики порта RAS**](ras-port-statistics-str.md) .</span><span class="sxs-lookup"><span data-stu-id="78db4-109">The **RasAdminPortClearStatistics** function resets the counters representing the various statistics reported by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function in the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure.</span></span> <span data-ttu-id="78db4-110">Счетчики сбрасываются в нулевое состояние и начинают накапливаться.</span><span class="sxs-lookup"><span data-stu-id="78db4-110">The counters are reset to zero and start accumulating.</span></span>

## <a name="syntax"></a><span data-ttu-id="78db4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78db4-111">Syntax</span></span>


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="78db4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="78db4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78db4-113">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78db4-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78db4-114">Указатель на строку в Юникоде, заканчивающуюся нулем и указывающую имя сервера RAS.</span><span class="sxs-lookup"><span data-stu-id="78db4-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="78db4-115">Укажите имя с начальными \\ \\ символами в формате: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="78db4-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="78db4-116">*лпсзпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78db4-116">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78db4-117">Указатель на строку в Юникоде, заканчивающуюся нулем и указывающую имя порта на сервере.</span><span class="sxs-lookup"><span data-stu-id="78db4-117">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78db4-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78db4-118">Return value</span></span>

<span data-ttu-id="78db4-119">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="78db4-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="78db4-120">Если функция завершается ошибкой, возвращаемое значение может быть следующим кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="78db4-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="78db4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="78db4-121">Value</span></span>                                                                                                 | <span data-ttu-id="78db4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="78db4-122">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="78db4-123"><dt>**Ошибка \_ dev \_ не \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="78db4-123"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="78db4-124">Указан недопустимый порт.</span><span class="sxs-lookup"><span data-stu-id="78db4-124">The specified port is invalid.</span></span><br/> |



 

<span data-ttu-id="78db4-125">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="78db4-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="78db4-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78db4-126">Remarks</span></span>

<span data-ttu-id="78db4-127">Функция **расадминпортклеарстатистикс** очищает статистику на сервере, а не локально в приложении, которое выполняет вызов.</span><span class="sxs-lookup"><span data-stu-id="78db4-127">The **RasAdminPortClearStatistics** function clears the statistics on the server, not locally within the application that makes the call.</span></span> <span data-ttu-id="78db4-128">Это означает, что статистика также сбрасывается для любого другого приложения, отслеживающего указанный порт.</span><span class="sxs-lookup"><span data-stu-id="78db4-128">This means that the statistics are also reset for any other application that is monitoring the specified port.</span></span>

<span data-ttu-id="78db4-129">Если порт *лпсзпорт* является частью многоканального соединения, **расадминпортклеарстатистикс** Сбрасывает статистику для указанного порта, а функция также сбрасывает совокупную статистику для многоканального соединения.</span><span class="sxs-lookup"><span data-stu-id="78db4-129">If the *lpszPort* port is part of a multilink connection, **RasAdminPortClearStatistics** resets the statistics for the specified port, The function also resets the cumulative statistics for the multilink connection.</span></span> <span data-ttu-id="78db4-130">Однако функция не влияет на отдельные статистические данные для других портов, которые являются частью многоканального соединения.</span><span class="sxs-lookup"><span data-stu-id="78db4-130">However, the function does not effect the individual statistics for other ports that are part of the multilink connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="78db4-131">Требования</span><span class="sxs-lookup"><span data-stu-id="78db4-131">Requirements</span></span>



| <span data-ttu-id="78db4-132">Требование</span><span class="sxs-lookup"><span data-stu-id="78db4-132">Requirement</span></span> | <span data-ttu-id="78db4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="78db4-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78db4-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="78db4-134">End of client support</span></span><br/> | <span data-ttu-id="78db4-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="78db4-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="78db4-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="78db4-136">End of server support</span></span><br/> | <span data-ttu-id="78db4-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78db4-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="78db4-138">Header</span><span class="sxs-lookup"><span data-stu-id="78db4-138">Header</span></span><br/>                | <dl> <span data-ttu-id="78db4-139"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="78db4-139"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="78db4-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78db4-140">Library</span></span><br/>               | <dl> <span data-ttu-id="78db4-141"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78db4-141"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="78db4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="78db4-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="78db4-143"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78db4-143"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78db4-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78db4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78db4-145">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="78db4-145">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="78db4-146">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="78db4-146">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="78db4-147">**\_Статистика порта \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="78db4-147">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="78db4-148">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="78db4-148">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

