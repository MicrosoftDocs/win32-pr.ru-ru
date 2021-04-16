---
description: Выполняет запрос для получения событий. Вызов немедленно возвращает значение.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Кнотификатионкуери (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712102"
---
# <a name="swbemservicesexecnotificationquery-method"></a><span data-ttu-id="27b47-104">SWbemServices.Exeметод Кнотификатионкуери</span><span class="sxs-lookup"><span data-stu-id="27b47-104">SWbemServices.ExecNotificationQuery method</span></span>

<span data-ttu-id="27b47-105">Метод **ексекнотификатионкуери** объекта [**SwbemServices**](swbemservices.md) выполняет запрос для получения событий.</span><span class="sxs-lookup"><span data-stu-id="27b47-105">The **ExecNotificationQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="27b47-106">Вызов немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="27b47-106">The call returns immediately.</span></span> <span data-ttu-id="27b47-107">Пользователь может опросить возвращенный перечислитель для событий по мере их поступления.</span><span class="sxs-lookup"><span data-stu-id="27b47-107">The user can poll the returned enumerator for events as they arrive.</span></span>

<span data-ttu-id="27b47-108">Метод вызывается в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="27b47-108">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="27b47-109">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="27b47-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="27b47-110">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="27b47-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="27b47-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27b47-111">Syntax</span></span>


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="27b47-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="27b47-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b47-113">*стркуери*</span><span class="sxs-lookup"><span data-stu-id="27b47-113">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="27b47-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="27b47-114">Required.</span></span> <span data-ttu-id="27b47-115">Строка, содержащая текст запроса, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="27b47-115">String that contains the text of the event-related query.</span></span> <span data-ttu-id="27b47-116">Этот параметр не может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="27b47-116">This parameter cannot be blank.</span></span> <span data-ttu-id="27b47-117">Дополнительные сведения о создании строк запросов WMI см. в разделе [запросы с помощью WQL](querying-with-wql.md) и Справочник по [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="27b47-117">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="27b47-118">*стркуерилангуаже* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="27b47-118">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="27b47-119">Строка, содержащая используемый язык запросов.</span><span class="sxs-lookup"><span data-stu-id="27b47-119">String that contains the query language to be used.</span></span> <span data-ttu-id="27b47-120">Если указано, это значение должно быть "WQL".</span><span class="sxs-lookup"><span data-stu-id="27b47-120">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="27b47-121">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="27b47-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="27b47-122">Это целое число, определяющее поведение запроса.</span><span class="sxs-lookup"><span data-stu-id="27b47-122">This is an integer that determines the behavior of the query.</span></span> <span data-ttu-id="27b47-123">Значение по умолчанию — **вбемфлагретурниммедиатели**  +  **вбемфлагфорвардонли**.</span><span class="sxs-lookup"><span data-stu-id="27b47-123">The default value is **wbemFlagReturnImmediately** + **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="27b47-124">Если указан этот параметр, для этого параметра необходимо задать значение **вбемфлагретурниммедиатели** и **вбемфлагфорвардонли** , иначе вызов завершится неудачей.</span><span class="sxs-lookup"><span data-stu-id="27b47-124">If you specify this parameter, this parameter must be set to both **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** or the call fails.</span></span> <span data-ttu-id="27b47-125">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="27b47-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="27b47-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="27b47-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="27b47-127">Вызывает возврат перечислителя "только вперед".</span><span class="sxs-lookup"><span data-stu-id="27b47-127">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="27b47-128">Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="27b47-128">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="27b47-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="27b47-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="27b47-130">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="27b47-130">Causes the call to return immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="27b47-131">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="27b47-131">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="27b47-132">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="27b47-132">Typically, this is undefined.</span></span> <span data-ttu-id="27b47-133">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="27b47-133">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="27b47-134">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="27b47-134">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27b47-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27b47-135">Return value</span></span>

<span data-ttu-id="27b47-136">Если ошибка не возникает, этот метод возвращает объект [**свбемевентсаурце**](swbemeventsource.md) .</span><span class="sxs-lookup"><span data-stu-id="27b47-136">If no error occurs, this method returns an [**SWbemEventSource**](swbemeventsource.md) object.</span></span> <span data-ttu-id="27b47-137">Вы можете вызвать метод [**свбемевентсаурце. некстевент**](swbemeventsource-nextevent.md) , чтобы получить события по мере их поступления.</span><span class="sxs-lookup"><span data-stu-id="27b47-137">You can call the [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27b47-138">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="27b47-138">Error codes</span></span>

<span data-ttu-id="27b47-139">После завершения метода **ексекнотификатионкуери** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="27b47-139">After the completion of the **ExecNotificationQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="27b47-140">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="27b47-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="27b47-141">Текущий пользователь не имеет права на Просмотр результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="27b47-141">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="27b47-142">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="27b47-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="27b47-143">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="27b47-143">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="27b47-144">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="27b47-144">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="27b47-145">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="27b47-145">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="27b47-146">**вбемерринвалидкуери** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="27b47-146">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="27b47-147">Недопустимый синтаксис запроса.</span><span class="sxs-lookup"><span data-stu-id="27b47-147">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="27b47-148">**вбемерринвалидкуеритипе** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="27b47-148">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="27b47-149">Запрошенный язык запросов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="27b47-149">The requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="27b47-150">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="27b47-150">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="27b47-151">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="27b47-151">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27b47-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27b47-152">Remarks</span></span>

<span data-ttu-id="27b47-153">В отличие от метода [**SWbemServices.Exeккуерясинк**](swbemservices-execqueryasync.md) , **ексекнотификатионкуери** возвращает объекты типа события, которые создаются в будущих событиях, а не в существующих объектах.</span><span class="sxs-lookup"><span data-stu-id="27b47-153">Unlike the [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method, **ExecNotificationQuery** returns event type objects that are generated by future events rather than existing objects.</span></span> <span data-ttu-id="27b47-154">Объекты событий, **ексекнотификатионкуери** запросы, могут быть встроенными (например, [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md)) или внешние (например, события поставщика реестра, такие как [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) или SNMP).</span><span class="sxs-lookup"><span data-stu-id="27b47-154">The event objects that **ExecNotificationQuery** requests can either be intrinsic (such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) or extrinsic (such as registry provider events like [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="27b47-155">Дополнительные сведения см. в разделе [Определение типа события для получения](determining-the-type-of-event-to-receive.md) и [получения уведомлений о событиях](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="27b47-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md) and [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

<span data-ttu-id="27b47-156">Существует ряд ограничений на количество ключевых слов **and** и **or** , которые могут использоваться в запросах WQL.</span><span class="sxs-lookup"><span data-stu-id="27b47-156">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="27b47-157">Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, что WMI вернет код ошибки **\_ \_ \_ нарушения квоты WBEM E** как значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27b47-157">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="27b47-158">Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.</span><span class="sxs-lookup"><span data-stu-id="27b47-158">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="27b47-159">Примеры</span><span class="sxs-lookup"><span data-stu-id="27b47-159">Examples</span></span>

<span data-ttu-id="27b47-160">В следующем примере кода VBScript отслеживаются изменения в томах на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="27b47-160">The following VBScript code example monitors changes to volumes on a local computer.</span></span> <span data-ttu-id="27b47-161">Обратите внимание, что [**Win32 \_ волумечанжеевент**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) — это внешнее событие, определяемое поставщиком, а не встроенное событие, определяемое WMI.</span><span class="sxs-lookup"><span data-stu-id="27b47-161">Note that [**Win32\_VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) is an extrinsic event that is defined by a provider not an intrinsic WMI-defined event.</span></span> <span data-ttu-id="27b47-162">Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="27b47-162">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



<span data-ttu-id="27b47-163">В следующем примере кода VBScript отслеживается Удаление процесса.</span><span class="sxs-lookup"><span data-stu-id="27b47-163">The following VBScript code example monitors process deletion.</span></span> <span data-ttu-id="27b47-164">При удалении процесса в диспетчере задач или закрытии приложения сценарий отображает сообщение.</span><span class="sxs-lookup"><span data-stu-id="27b47-164">If you delete a process in Task Manager or close an application, then the script displays a message.</span></span> <span data-ttu-id="27b47-165">Обратите внимание, что этот скрипт запрашивает внутреннее событие, определенное WMI- [**\_ \_ инстанцеделетионевент**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="27b47-165">Note that this script queries an intrinsic event that is defined by WMI - [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span>


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a><span data-ttu-id="27b47-166">Требования</span><span class="sxs-lookup"><span data-stu-id="27b47-166">Requirements</span></span>



| <span data-ttu-id="27b47-167">Требование</span><span class="sxs-lookup"><span data-stu-id="27b47-167">Requirement</span></span> | <span data-ttu-id="27b47-168">Значение</span><span class="sxs-lookup"><span data-stu-id="27b47-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27b47-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27b47-169">Minimum supported client</span></span><br/> | <span data-ttu-id="27b47-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27b47-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27b47-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27b47-171">Minimum supported server</span></span><br/> | <span data-ttu-id="27b47-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27b47-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27b47-173">Header</span><span class="sxs-lookup"><span data-stu-id="27b47-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="27b47-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="27b47-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="27b47-175">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="27b47-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="27b47-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="27b47-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="27b47-177">DLL</span><span class="sxs-lookup"><span data-stu-id="27b47-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27b47-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27b47-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="27b47-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="27b47-179">CLSID</span></span><br/>                    | <span data-ttu-id="27b47-180">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="27b47-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="27b47-181">IID</span><span class="sxs-lookup"><span data-stu-id="27b47-181">IID</span></span><br/>                      | <span data-ttu-id="27b47-182">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="27b47-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="27b47-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27b47-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b47-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="27b47-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="27b47-185">**Свбемевентсаурце. Некстевент**</span><span class="sxs-lookup"><span data-stu-id="27b47-185">**SWbemEventSource.NextEvent**</span></span>](swbemeventsource-nextevent.md)
</dt> <dt>

[<span data-ttu-id="27b47-186">**SWbemServices.ExeКкуери**</span><span class="sxs-lookup"><span data-stu-id="27b47-186">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="27b47-187">Получение события WMI</span><span class="sxs-lookup"><span data-stu-id="27b47-187">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> <dt>

[<span data-ttu-id="27b47-188">Запросы с помощью WQL</span><span class="sxs-lookup"><span data-stu-id="27b47-188">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="27b47-189">WQL (SQL для WMI)</span><span class="sxs-lookup"><span data-stu-id="27b47-189">WQL (SQL for WMI)</span></span>](wql-sql-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="27b47-190">Определение типа получаемого события</span><span class="sxs-lookup"><span data-stu-id="27b47-190">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

