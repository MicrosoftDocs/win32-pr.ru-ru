---
description: Функция Пдхвбупдателог обновляет текущий запрос и записывает новые данные в файл журнала. Эта функция вызывает Пдхупдателог.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: Функция Пдхвбупдателог
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663209"
---
# <a name="pdhvbupdatelog-function"></a><span data-ttu-id="08a7b-104">Функция Пдхвбупдателог</span><span class="sxs-lookup"><span data-stu-id="08a7b-104">PdhVbUpdateLog function</span></span>

<span data-ttu-id="08a7b-105">Функция **пдхвбупдателог** обновляет текущий запрос и записывает новые данные в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="08a7b-105">The **PdhVbUpdateLog** function function updates the current query and writes new data to the log file.</span></span> <span data-ttu-id="08a7b-106">Эта функция вызывает [**пдхупдателог**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span><span class="sxs-lookup"><span data-stu-id="08a7b-106">This function calls [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08a7b-107">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="08a7b-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="08a7b-108">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="08a7b-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="08a7b-109">Функция Пдхвбупдателог ( \_ ByVal HLog как PDH \_ hLog, \_ BYVAL сзусерстринг AS LPCTSTR \_ )</span><span class="sxs-lookup"><span data-stu-id="08a7b-109">Function PdhVbUpdateLog( \_ ByVal hLog As PDH\_HLOG, \_ ByVal szUserString As LPCTSTR \_ )</span></span>

## <a name="parameters"></a><span data-ttu-id="08a7b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="08a7b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a7b-111">*hLog* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08a7b-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a7b-112">Обрабатываемый файл журнала.</span><span class="sxs-lookup"><span data-stu-id="08a7b-112">Handle to the log file to be updated.</span></span> <span data-ttu-id="08a7b-113">Этот маркер возвращается функцией [**пдхвбопенлог**](pdhvbopenlog.md) .</span><span class="sxs-lookup"><span data-stu-id="08a7b-113">This handle is returned by the [**PdhVbOpenLog**](pdhvbopenlog.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="08a7b-114">*сзусерстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08a7b-114">*szUserString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a7b-115">Указатель на строку, указывающую данные, которые должны быть добавлены в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="08a7b-115">Pointer to a string that specifies the data to be added to the log file.</span></span> <span data-ttu-id="08a7b-116">Обычно это используется для комментариев в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="08a7b-116">This is generally used for comments within the log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a7b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08a7b-117">Return value</span></span>

<span data-ttu-id="08a7b-118">Если функция завершается с ошибкой, она возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="08a7b-118">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="08a7b-119">Если функция завершается ошибкой, возвращаемое значение является [кодом системной ошибки](/windows/desktop/Debug/system-error-codes) или [кодом ошибки PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="08a7b-119">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="08a7b-120">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="08a7b-120">The following are possible values.</span></span>



| <span data-ttu-id="08a7b-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="08a7b-121">Return code</span></span>                                                                                                | <span data-ttu-id="08a7b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="08a7b-122">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08a7b-123"><dt>**\_недостаточный \_ Размер буфера PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="08a7b-123"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="08a7b-124">Запрошенные данные больше, чем указанный буфер.</span><span class="sxs-lookup"><span data-stu-id="08a7b-124">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="08a7b-125">Не удалось вернуть запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="08a7b-125">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="08a7b-126"><dt>**\_Недопустимый \_ аргумент PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="08a7b-126"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="08a7b-127">Один или несколько буферов строк имеют неправильный размер.</span><span class="sxs-lookup"><span data-stu-id="08a7b-127">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="08a7b-128"><dt>**\_Недопустимый \_ маркер PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="08a7b-128"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="08a7b-129">Этот маркер не является допустимым объектом PDH.</span><span class="sxs-lookup"><span data-stu-id="08a7b-129">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="08a7b-130"><dt>**\_ \_ \_ Ошибка при открытии файла журнала PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08a7b-130"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="08a7b-131">Не удалось открыть указанный файл журнала.</span><span class="sxs-lookup"><span data-stu-id="08a7b-131">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="08a7b-132"><dt>**\_файл PDH \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="08a7b-132"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="08a7b-133">Не удалось найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="08a7b-133">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="08a7b-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08a7b-134">Remarks</span></span>

<span data-ttu-id="08a7b-135">В настоящий момент должен быть открытый запрос, и перед вызовом этой функции необходимо добавить в него нужные счетчики.</span><span class="sxs-lookup"><span data-stu-id="08a7b-135">There must be a currently opened query, and the desired counters must be added to it before this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a7b-136">Требования</span><span class="sxs-lookup"><span data-stu-id="08a7b-136">Requirements</span></span>



| <span data-ttu-id="08a7b-137">Требование</span><span class="sxs-lookup"><span data-stu-id="08a7b-137">Requirement</span></span> | <span data-ttu-id="08a7b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="08a7b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08a7b-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08a7b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="08a7b-140">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="08a7b-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08a7b-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08a7b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="08a7b-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08a7b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="08a7b-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="08a7b-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="08a7b-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08a7b-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="08a7b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="08a7b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a7b-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a7b-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a7b-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08a7b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a7b-148">**пдхупдателог**</span><span class="sxs-lookup"><span data-stu-id="08a7b-148">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[<span data-ttu-id="08a7b-149">**пдхвбжетлогфилесизе**</span><span class="sxs-lookup"><span data-stu-id="08a7b-149">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="08a7b-150">**пдхвбопенлог**</span><span class="sxs-lookup"><span data-stu-id="08a7b-150">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> </dl>

 

