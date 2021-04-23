---
title: Функция Расадминфрибуффер (Рассапи. h)
description: Функция Расадминфрибуффер освобождает память, выделенную службой RAS от имени вызывающего объекта.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RAS функции Расадминфрибуффер
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680119"
---
# <a name="rasadminfreebuffer-function"></a><span data-ttu-id="badbc-104">Функция Расадминфрибуффер</span><span class="sxs-lookup"><span data-stu-id="badbc-104">RasAdminFreeBuffer function</span></span>

<span data-ttu-id="badbc-105">\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="badbc-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="badbc-106">Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="badbc-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="badbc-107">Приложения должны использовать функцию [**мпрадминбуфферфри**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]</span><span class="sxs-lookup"><span data-stu-id="badbc-107">Applications should use the [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) function.\]</span></span>

<span data-ttu-id="badbc-108">Функция **расадминфрибуффер** освобождает память, ВЫДЕЛЕННУЮ службой RAS от имени вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="badbc-108">The **RasAdminFreeBuffer** function frees memory that was allocated by RAS on behalf of the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="badbc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="badbc-109">Syntax</span></span>


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a><span data-ttu-id="badbc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="badbc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="badbc-111">*Указатель мыши* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="badbc-111">*Pointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="badbc-112">Указатель на буфер для освобождения.</span><span class="sxs-lookup"><span data-stu-id="badbc-112">Pointer to the buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="badbc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="badbc-113">Return value</span></span>

<span data-ttu-id="badbc-114">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="badbc-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="badbc-115">Если функция завершается ошибкой, возвращаемое значение может быть следующим кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="badbc-115">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="badbc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="badbc-116">Value</span></span>                                                                                                    | <span data-ttu-id="badbc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="badbc-117">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="badbc-118"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="badbc-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="badbc-119">Недопустимый параметр *указателя* .</span><span class="sxs-lookup"><span data-stu-id="badbc-119">The *Pointer* parameter is invalid.</span></span><br/> |



 

<span data-ttu-id="badbc-120">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="badbc-120">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="badbc-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="badbc-121">Remarks</span></span>

<span data-ttu-id="badbc-122">Используйте функцию **расадминфрибуффер** , чтобы освободить буферы, выделенные функциями [**расадминпортенум**](rasadminportenum.md) и [**расадминпортжетинфо**](rasadminportgetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="badbc-122">Use the **RasAdminFreeBuffer** function to free the buffers allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="badbc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="badbc-123">Requirements</span></span>



| <span data-ttu-id="badbc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="badbc-124">Requirement</span></span> | <span data-ttu-id="badbc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="badbc-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="badbc-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="badbc-126">End of client support</span></span><br/> | <span data-ttu-id="badbc-127">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="badbc-127">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="badbc-128">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="badbc-128">End of server support</span></span><br/> | <span data-ttu-id="badbc-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="badbc-129">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="badbc-130">Header</span><span class="sxs-lookup"><span data-stu-id="badbc-130">Header</span></span><br/>                | <dl> <span data-ttu-id="badbc-131"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="badbc-131"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="badbc-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="badbc-132">Library</span></span><br/>               | <dl> <span data-ttu-id="badbc-133"><dt>Рассапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="badbc-133"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="badbc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="badbc-134">DLL</span></span><br/>                   | <dl> <span data-ttu-id="badbc-135"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="badbc-135"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="badbc-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="badbc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="badbc-137">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="badbc-137">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="badbc-138">Функции администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="badbc-138">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="badbc-139">**расадминпортенум**</span><span class="sxs-lookup"><span data-stu-id="badbc-139">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> <dt>

[<span data-ttu-id="badbc-140">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="badbc-140">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

