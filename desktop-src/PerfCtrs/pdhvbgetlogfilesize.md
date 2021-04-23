---
description: Функция Пдхвбжетлогфилесизе возвращает размер указанного файла журнала. Эта функция вызывает Пдхжетлогфилесизе.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: Функция Пдхвбжетлогфилесизе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663215"
---
# <a name="pdhvbgetlogfilesize-function"></a><span data-ttu-id="8a8a8-104">Функция Пдхвбжетлогфилесизе</span><span class="sxs-lookup"><span data-stu-id="8a8a8-104">PdhVbGetLogFileSize function</span></span>

<span data-ttu-id="8a8a8-105">Функция **пдхвбжетлогфилесизе** возвращает размер указанного файла журнала.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-105">The **PdhVbGetLogFileSize** function returns the size of the specified log file.</span></span> <span data-ttu-id="8a8a8-106">Эта функция вызывает [**пдхжетлогфилесизе**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span><span class="sxs-lookup"><span data-stu-id="8a8a8-106">This function calls [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a8a8-107">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="8a8a8-108">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8a8a8-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="8a8a8-109">Функция Пдхвбжетлогфилесизе ( \_ ByVal HLog AS PDH \_ hLog, \_ ByRef ллсизе как long \_ ) как DWORD</span><span class="sxs-lookup"><span data-stu-id="8a8a8-109">Function PdhVbGetLogFileSize( \_ ByVal hLog As PDH\_HLOG, \_ ByRef llSize As LONG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="8a8a8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a8a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8a8-111">*hLog* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a8a8-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8a8-112">Обработчик файла журнала.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-112">Handle to the log file.</span></span> <span data-ttu-id="8a8a8-113">Этот маркер возвращается функцией [**пдхопенлог**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) .</span><span class="sxs-lookup"><span data-stu-id="8a8a8-113">This handle is returned by the [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) function.</span></span>

</dd> <dt>

<span data-ttu-id="8a8a8-114">*ллсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8a8a8-114">*llSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8a8-115">Указатель на переменную, которая получает размер файла журнала в байтах.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-115">Pointer to a variable that receives the size of the log file, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8a8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a8a8-116">Return value</span></span>

<span data-ttu-id="8a8a8-117">Если функция завершается с ошибкой, она возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-117">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="8a8a8-118">Если функция завершается ошибкой, возвращаемое значение является [кодом системной ошибки](/windows/desktop/Debug/system-error-codes) или [кодом ошибки PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8a8a8-118">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="8a8a8-119">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-119">The following are possible values.</span></span>



| <span data-ttu-id="8a8a8-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8a8a8-120">Return code</span></span>                                                                                                | <span data-ttu-id="8a8a8-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8a8a8-121">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a8a8-122"><dt>**\_недостаточный \_ Размер буфера PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="8a8a8-122"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="8a8a8-123">Запрошенные данные больше, чем указанный буфер.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-123">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="8a8a8-124">Не удалось вернуть запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-124">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="8a8a8-125"><dt>**\_Недопустимый \_ аргумент PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="8a8a8-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="8a8a8-126">Один или несколько буферов строк имеют неправильный размер.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-126">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="8a8a8-127"><dt>**\_Недопустимый \_ маркер PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="8a8a8-127"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="8a8a8-128">Этот маркер не является допустимым объектом PDH.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-128">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="8a8a8-129"><dt>**\_ \_ \_ Ошибка при открытии файла журнала PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8a8a8-129"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="8a8a8-130">Не удалось открыть указанный файл журнала.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-130">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="8a8a8-131"><dt>**\_файл PDH \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="8a8a8-131"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="8a8a8-132">Не удалось найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="8a8a8-132">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="8a8a8-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8a8a8-133">Requirements</span></span>



| <span data-ttu-id="8a8a8-134">Требование</span><span class="sxs-lookup"><span data-stu-id="8a8a8-134">Requirement</span></span> | <span data-ttu-id="8a8a8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8a8a8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8a8-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a8a8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8a8-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8a8a8-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a8a8-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a8a8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8a8-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a8a8-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8a8a8-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a8a8-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a8a8-141"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a8a8-141"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="8a8a8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8a8a8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8a8-143"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8a8-143"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a8a8-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a8a8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8a8-145">**пдхжетлогфилесизе**</span><span class="sxs-lookup"><span data-stu-id="8a8a8-145">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[<span data-ttu-id="8a8a8-146">**пдхвбопенлог**</span><span class="sxs-lookup"><span data-stu-id="8a8a8-146">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> <dt>

[<span data-ttu-id="8a8a8-147">**пдхвбупдателог**</span><span class="sxs-lookup"><span data-stu-id="8a8a8-147">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

