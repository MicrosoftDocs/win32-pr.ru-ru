---
description: Функция Пдхвбаддкаунтер создает запись счетчика в указанном объекте запроса и возвращает маркер этого счетчика после успешного завершения.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: Функция Пдхвбаддкаунтер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663221"
---
# <a name="pdhvbaddcounter-function"></a><span data-ttu-id="977a7-103">Функция Пдхвбаддкаунтер</span><span class="sxs-lookup"><span data-stu-id="977a7-103">PdhVbAddCounter function</span></span>

<span data-ttu-id="977a7-104">Функция **пдхвбаддкаунтер** создает запись счетчика в указанном объекте запроса и возвращает маркер этого счетчика после успешного завершения.</span><span class="sxs-lookup"><span data-stu-id="977a7-104">The **PdhVbAddCounter** function creates a counter entry in the specified query object, and returns a handle to that counter upon successful completion.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="977a7-105">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="977a7-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="977a7-106">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="977a7-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="977a7-107">Функция Пдхвбаддкаунтер ( \_ ByVal Куерихандле как Long, \_ ByVal Каунтерпас в качестве строки, \_ ByVal каунтерхандле как long \_ ) как long</span><span class="sxs-lookup"><span data-stu-id="977a7-107">Function PdhVbAddCounter( \_ ByVal QueryHandle As Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="977a7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="977a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="977a7-109">*куерихандле*</span><span class="sxs-lookup"><span data-stu-id="977a7-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="977a7-110">Идентификатор запроса, которому будет назначен этот счетчик.</span><span class="sxs-lookup"><span data-stu-id="977a7-110">ID of the query to which this counter is to be assigned.</span></span> <span data-ttu-id="977a7-111">Это значение возвращается функцией [**пдхвбопенкуери**](pdhvbopenquery.md) .</span><span class="sxs-lookup"><span data-stu-id="977a7-111">This value is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="977a7-112">*CounterPath*</span><span class="sxs-lookup"><span data-stu-id="977a7-112">*CounterPath*</span></span> 
</dt> <dd>

<span data-ttu-id="977a7-113">Текстовая строка, указывающая имя пути счетчика, добавляемого в запрос.</span><span class="sxs-lookup"><span data-stu-id="977a7-113">Text string that specifies the name of the counter path to add to the query.</span></span> <span data-ttu-id="977a7-114">Содержимое этой строки должно быть допустимым путем к счетчику, полученным из браузера счетчиков или другого источника.</span><span class="sxs-lookup"><span data-stu-id="977a7-114">The contents of this string must be a valid counter path, as obtained from the counter browser or other source.</span></span>

</dd> <dt>

<span data-ttu-id="977a7-115">*каунтерхандле*</span><span class="sxs-lookup"><span data-stu-id="977a7-115">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="977a7-116">Уникальная ссылка, определяющая этот счетчик в запросе.</span><span class="sxs-lookup"><span data-stu-id="977a7-116">Unique reference that identifies this counter in the query.</span></span> <span data-ttu-id="977a7-117">Перед вызовом функции эта переменная должна быть инициализирована нулем.</span><span class="sxs-lookup"><span data-stu-id="977a7-117">This variable must be initialized to zero before the function is called.</span></span> <span data-ttu-id="977a7-118">Он содержит допустимое значение для возврата только в случае успешного завершения функции.</span><span class="sxs-lookup"><span data-stu-id="977a7-118">It contains a valid value on return only if the function completes successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="977a7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="977a7-119">Return value</span></span>

<span data-ttu-id="977a7-120">Если функция завершается успешно, она возвращает **длинное** целое число, равное \_ успешному выполнению, и новый маркер в переменной *каунтерхандле* .</span><span class="sxs-lookup"><span data-stu-id="977a7-120">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *CounterHandle* variable.</span></span>

<span data-ttu-id="977a7-121">Если функция завершается ошибкой, возвращаемое значение является [кодом системной ошибки](/windows/desktop/Debug/system-error-codes) или [кодом ошибки PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="977a7-121">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="977a7-122">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="977a7-122">The following are possible values.</span></span>



| <span data-ttu-id="977a7-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="977a7-123">Return code</span></span>                                                                                                     | <span data-ttu-id="977a7-124">Описание</span><span class="sxs-lookup"><span data-stu-id="977a7-124">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="977a7-125"><dt>**\_Недопустимый \_ аргумент PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="977a7-126">Один или несколько аргументов являются недопустимыми или неверными.</span><span class="sxs-lookup"><span data-stu-id="977a7-126">One or more of the arguments is invalid or incorrect.</span></span><br/>              |
| <dl> <span data-ttu-id="977a7-127"><dt>**\_ \_ сбой выделения памяти \_ PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-127"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="977a7-128">Не удалось выделить буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="977a7-128">A memory buffer could not be allocated.</span></span><br/>                            |
| <dl> <span data-ttu-id="977a7-129"><dt>**\_Недопустимый \_ маркер PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-129"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>             | <span data-ttu-id="977a7-130">Недопустимый маркер запроса.</span><span class="sxs-lookup"><span data-stu-id="977a7-130">The query handle is not valid.</span></span><br/>                                     |
| <dl> <span data-ttu-id="977a7-131"><dt>**PDH \_ кстатус \_ без \_ счетчика**</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-131"><dt>**PDH\_CSTATUS\_NO\_COUNTER**</dt></span></span> </dl>        | <span data-ttu-id="977a7-132">Указанный счетчик не найден.</span><span class="sxs-lookup"><span data-stu-id="977a7-132">The specified counter was not found.</span></span><br/>                               |
| <dl> <span data-ttu-id="977a7-133"><dt>**PDH \_ кстатус \_ нет \_ объекта**</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-133"><dt>**PDH\_CSTATUS\_NO\_OBJECT**</dt></span></span> </dl>         | <span data-ttu-id="977a7-134">Не удалось найти указанный объект.</span><span class="sxs-lookup"><span data-stu-id="977a7-134">The specified object could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="977a7-135"><dt>**PDH \_ кстатус \_ нет \_ компьютера**</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-135"><dt>**PDH\_CSTATUS\_NO\_MACHINE**</dt></span></span> </dl>        | <span data-ttu-id="977a7-136">Не удалось создать запись компьютера.</span><span class="sxs-lookup"><span data-stu-id="977a7-136">A computer entry could not be created.</span></span><br/>                             |
| <dl> <span data-ttu-id="977a7-137"><dt>**PDH \_ кстатус \_ Bad \_ COUNTERNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-137"><dt>**PDH\_CSTATUS\_BAD\_COUNTERNAME**</dt></span></span> </dl>   | <span data-ttu-id="977a7-138">Передана пустая строка пути имени счетчика.</span><span class="sxs-lookup"><span data-stu-id="977a7-138">An empty counter name path string was passed in.</span></span><br/>                   |
| <dl> <span data-ttu-id="977a7-139"><dt>**\_функция PDH \_ не \_ найдена**</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-139"><dt>**PDH\_FUNCTION\_NOT\_FOUND**</dt></span></span> </dl>        | <span data-ttu-id="977a7-140">Не удалось определить функцию вычисления для этого счетчика.</span><span class="sxs-lookup"><span data-stu-id="977a7-140">The calculation function for this counter could not be determined.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="977a7-141">Требования</span><span class="sxs-lookup"><span data-stu-id="977a7-141">Requirements</span></span>



| <span data-ttu-id="977a7-142">Требование</span><span class="sxs-lookup"><span data-stu-id="977a7-142">Requirement</span></span> | <span data-ttu-id="977a7-143">Значение</span><span class="sxs-lookup"><span data-stu-id="977a7-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="977a7-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="977a7-144">Minimum supported client</span></span><br/> | <span data-ttu-id="977a7-145">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="977a7-145">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="977a7-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="977a7-146">Minimum supported server</span></span><br/> | <span data-ttu-id="977a7-147">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="977a7-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="977a7-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="977a7-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="977a7-149"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-149"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="977a7-150">DLL</span><span class="sxs-lookup"><span data-stu-id="977a7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="977a7-151"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="977a7-151"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="977a7-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="977a7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="977a7-153">**пдхвбопенкуери**</span><span class="sxs-lookup"><span data-stu-id="977a7-153">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
</dt> </dl>

 

