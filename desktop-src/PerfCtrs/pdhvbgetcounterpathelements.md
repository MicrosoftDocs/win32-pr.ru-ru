---
description: Функция Пдхвбжеткаунтерпаселементс анализирует полную строку пути счетчика производительности в отдельные элементы.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: Функция Пдхвбжеткаунтерпаселементс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663219"
---
# <a name="pdhvbgetcounterpathelements-function"></a><span data-ttu-id="214de-103">Функция Пдхвбжеткаунтерпаселементс</span><span class="sxs-lookup"><span data-stu-id="214de-103">PdhVbGetCounterPathElements function</span></span>

<span data-ttu-id="214de-104">Функция **пдхвбжеткаунтерпаселементс** анализирует полную строку пути счетчика производительности в отдельные элементы.</span><span class="sxs-lookup"><span data-stu-id="214de-104">The **PdhVbGetCounterPathElements** function parses a fully qualified performance counter path string into its individual elements.</span></span> <span data-ttu-id="214de-105">Каждая из строковых переменных должна иметь одинаковый размер (*bufferSize*), а также измерения и инициализировать их перед использованием в этой функции.</span><span class="sxs-lookup"><span data-stu-id="214de-105">Each of the string variables must be the same size (*BufferSize*) and dimensioned and initialized before it is used in this function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="214de-106">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="214de-106">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="214de-107">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="214de-107">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="214de-108">Функция Пдхвбжеткаунтерпаселементс ( \_ ByVal PathString как строка, \_ ByVal MachineName как строка, \_ ByVal ObjectName как строка, \_ ByVal имя_экземпляра как String, \_ ByVal Парентинстанце как String, ByVal \_ CounterName как String, ByVal \_ bufferSize как long \_ ) как long</span><span class="sxs-lookup"><span data-stu-id="214de-108">Function PdhVbGetCounterPathElements( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="214de-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="214de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214de-110">*PathString*</span><span class="sxs-lookup"><span data-stu-id="214de-110">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="214de-111">Строка пути счетчика, которая должна быть разбита на отдельные элементы.</span><span class="sxs-lookup"><span data-stu-id="214de-111">Counter path string that is to be broken up into its individual elements.</span></span>

</dd> <dt>

<span data-ttu-id="214de-112">*MachineName*</span><span class="sxs-lookup"><span data-stu-id="214de-112">*MachineName*</span></span> 
</dt> <dd>

<span data-ttu-id="214de-113">Строка для получения имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="214de-113">String to receive the computer name.</span></span>

</dd> <dt>

<span data-ttu-id="214de-114">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="214de-114">*ObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="214de-115">Строка для получения имени объекта.</span><span class="sxs-lookup"><span data-stu-id="214de-115">String to receive the object name.</span></span>

</dd> <dt>

<span data-ttu-id="214de-116">*InstanceName*</span><span class="sxs-lookup"><span data-stu-id="214de-116">*InstanceName*</span></span> 
</dt> <dd>

<span data-ttu-id="214de-117">Строка для получения имени экземпляра, если используется.</span><span class="sxs-lookup"><span data-stu-id="214de-117">String to receive the instance name, if used.</span></span>

</dd> <dt>

<span data-ttu-id="214de-118">*парентинстанце*</span><span class="sxs-lookup"><span data-stu-id="214de-118">*ParentInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="214de-119">Строка, которая получает родительский экземпляр, если используется.</span><span class="sxs-lookup"><span data-stu-id="214de-119">String to receive the parent instance, if used.</span></span>

</dd> <dt>

<span data-ttu-id="214de-120">*CounterName*</span><span class="sxs-lookup"><span data-stu-id="214de-120">*CounterName*</span></span> 
</dt> <dd>

<span data-ttu-id="214de-121">Строка для получения имени счетчика.</span><span class="sxs-lookup"><span data-stu-id="214de-121">String to receive the counter name.</span></span>

</dd> <dt>

<span data-ttu-id="214de-122">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="214de-122">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="214de-123">Максимальный размер каждой строковой переменной, используемой в качестве параметра для этого вызова функции.</span><span class="sxs-lookup"><span data-stu-id="214de-123">Maximum size of each string variable used as a parameter to this function call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214de-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="214de-124">Return value</span></span>

<span data-ttu-id="214de-125">Если функция завершается успешно, она возвращает **длинное** целое число, равное \_ успешному выполнению ошибки.</span><span class="sxs-lookup"><span data-stu-id="214de-125">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS.</span></span>

<span data-ttu-id="214de-126">Если функция завершается ошибкой, возвращаемое значение является [кодом системной ошибки](/windows/desktop/Debug/system-error-codes) или [кодом ошибки PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="214de-126">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="214de-127">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="214de-127">The following are possible values.</span></span>



| <span data-ttu-id="214de-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="214de-128">Return code</span></span>                                                                                                     | <span data-ttu-id="214de-129">Описание</span><span class="sxs-lookup"><span data-stu-id="214de-129">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="214de-130"><dt>**\_Недопустимый \_ аргумент PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="214de-130"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="214de-131">Один или несколько буферов строк имеют неправильный размер.</span><span class="sxs-lookup"><span data-stu-id="214de-131">One or more of the string buffers is not the correct size.</span></span><br/>                          |
| <dl> <span data-ttu-id="214de-132"><dt>**\_Дополнительные \_ данные PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="214de-132"><dt>**PDH\_MORE\_DATA**</dt></span></span> </dl>                  | <span data-ttu-id="214de-133">Один или несколько элементов пути счетчиков слишком велики для длины буфера возврата.</span><span class="sxs-lookup"><span data-stu-id="214de-133">One or more of the counter path elements is too large for the return buffer length.</span></span><br/> |
| <dl> <span data-ttu-id="214de-134"><dt>**\_ \_ сбой выделения памяти \_ PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="214de-134"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="214de-135">Не удалось выделить временный буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="214de-135">A temporary memory buffer could not be allocated.</span></span><br/>                                   |



 

## <a name="requirements"></a><span data-ttu-id="214de-136">Требования</span><span class="sxs-lookup"><span data-stu-id="214de-136">Requirements</span></span>



| <span data-ttu-id="214de-137">Требование</span><span class="sxs-lookup"><span data-stu-id="214de-137">Requirement</span></span> | <span data-ttu-id="214de-138">Значение</span><span class="sxs-lookup"><span data-stu-id="214de-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="214de-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="214de-139">Minimum supported client</span></span><br/> | <span data-ttu-id="214de-140">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="214de-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="214de-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="214de-141">Minimum supported server</span></span><br/> | <span data-ttu-id="214de-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="214de-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="214de-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="214de-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="214de-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="214de-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="214de-145">DLL</span><span class="sxs-lookup"><span data-stu-id="214de-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="214de-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="214de-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="214de-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="214de-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214de-148">**пдхвбкреатекаунтерпаслист**</span><span class="sxs-lookup"><span data-stu-id="214de-148">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="214de-149">**пдхвбжеткаунтерпасфромлист**</span><span class="sxs-lookup"><span data-stu-id="214de-149">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="214de-150">**пдхвбжетонекаунтерпас**</span><span class="sxs-lookup"><span data-stu-id="214de-150">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

