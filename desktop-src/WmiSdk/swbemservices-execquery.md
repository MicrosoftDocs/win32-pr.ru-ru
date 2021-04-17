---
description: Выполняет запрос для получения объектов.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Ккуери (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2f3a894681bafc71de34ae7722b985494ef80b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712101"
---
# <a name="swbemservicesexecquery-method"></a><span data-ttu-id="da658-103">SWbemServices.Exeметод Ккуери</span><span class="sxs-lookup"><span data-stu-id="da658-103">SWbemServices.ExecQuery method</span></span>

<span data-ttu-id="da658-104">Метод **ExecQuery** объекта [**SwbemServices**](swbemservices.md) выполняет запрос для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="da658-104">The **ExecQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="da658-105">Эти объекты доступны через возвращенную коллекцию [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="da658-105">These objects are available through the returned [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span>

<span data-ttu-id="da658-106">Этот метод вызывается в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="da658-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="da658-107">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="da658-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="da658-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="da658-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da658-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da658-109">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="da658-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="da658-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da658-111">*стркуери*</span><span class="sxs-lookup"><span data-stu-id="da658-111">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="da658-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="da658-112">Required.</span></span> <span data-ttu-id="da658-113">Строка, содержащая текст запроса.</span><span class="sxs-lookup"><span data-stu-id="da658-113">String that contains the text of the query.</span></span> <span data-ttu-id="da658-114">Этот параметр не может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="da658-114">This parameter cannot be blank.</span></span> <span data-ttu-id="da658-115">Дополнительные сведения о создании строк запросов WMI см. в разделе [запросы с помощью WQL](querying-with-wql.md) и Справочник по [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="da658-115">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="da658-116">*стркуерилангуаже* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="da658-116">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da658-117">Строка, содержащая используемый язык запросов.</span><span class="sxs-lookup"><span data-stu-id="da658-117">String that contains the query language to be used.</span></span> <span data-ttu-id="da658-118">Если указано, это значение должно быть "WQL".</span><span class="sxs-lookup"><span data-stu-id="da658-118">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="da658-119">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="da658-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da658-120">Целое число, определяющее поведение запроса и определяющее, будет ли этот вызов немедленно возвращен.</span><span class="sxs-lookup"><span data-stu-id="da658-120">Integer that determines the behavior of the query and determines whether this call returns immediately.</span></span> <span data-ttu-id="da658-121">Значение этого параметра по умолчанию — **вбемфлагретурниммедиатели**.</span><span class="sxs-lookup"><span data-stu-id="da658-121">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="da658-122">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="da658-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="da658-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="da658-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="da658-124">Вызывает возврат перечислителя "только вперед".</span><span class="sxs-lookup"><span data-stu-id="da658-124">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="da658-125">Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="da658-125">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="da658-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="da658-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="da658-127">Заставляет Инструментарий WMI хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.</span><span class="sxs-lookup"><span data-stu-id="da658-127">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="da658-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="da658-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="da658-129">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="da658-129">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="da658-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="da658-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="da658-131">Вызывает блокирование этого вызова до завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="da658-131">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="da658-132">Этот флаг вызывает метод в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="da658-132">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="da658-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>Вбемкуерифлагпрототипе \* \* \* \* (0x2)</span><span class="sxs-lookup"><span data-stu-id="da658-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="da658-134">Используется для создания прототипов.</span><span class="sxs-lookup"><span data-stu-id="da658-134">Used for prototyping.</span></span> <span data-ttu-id="da658-135">Этот флаг останавливает запрос и возвращает объект, который выглядит как типичный объект результата.</span><span class="sxs-lookup"><span data-stu-id="da658-135">This flag stops the query from happening and returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="da658-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="da658-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="da658-137">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="da658-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="da658-138">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="da658-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="da658-139">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="da658-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da658-140">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="da658-140">Typically, this is undefined.</span></span> <span data-ttu-id="da658-141">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="da658-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="da658-142">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="da658-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da658-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da658-143">Return value</span></span>

<span data-ttu-id="da658-144">Если ошибка не возникает, этот метод возвращает объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="da658-144">If no error occurs, this method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="da658-145">Это коллекция объектов, содержащая результирующий набор запроса.</span><span class="sxs-lookup"><span data-stu-id="da658-145">This is an object collection that contains the result set of the query.</span></span> <span data-ttu-id="da658-146">Вызывающий объект может проверить коллекцию, используя реализацию коллекций для используемого языка программирования.</span><span class="sxs-lookup"><span data-stu-id="da658-146">The caller can examine the collection using the implementation of collections for the programming language you are using.</span></span> <span data-ttu-id="da658-147">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="da658-147">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="da658-148">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="da658-148">Error codes</span></span>

<span data-ttu-id="da658-149">После завершения метода **ExecQuery** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="da658-149">After the completion of the **ExecQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="da658-150">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="da658-150">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="da658-151">У текущего пользователя нет разрешения на Просмотр результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="da658-151">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="da658-152">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="da658-152">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="da658-153">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="da658-153">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="da658-154">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="da658-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="da658-155">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="da658-155">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="da658-156">**вбемерринвалидкуери** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="da658-156">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="da658-157">Недопустимый синтаксис запроса.</span><span class="sxs-lookup"><span data-stu-id="da658-157">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="da658-158">**вбемерринвалидкуеритипе** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="da658-158">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="da658-159">Запрошенный язык запросов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="da658-159">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="da658-160">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="da658-160">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="da658-161">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="da658-161">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da658-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da658-162">Remarks</span></span>

<span data-ttu-id="da658-163">**ExecQuery** — один из наиболее часто используемых вызовов для получения сведений WMI.</span><span class="sxs-lookup"><span data-stu-id="da658-163">**ExecQuery** is one of the most commonly-used calls to retrieve WMI information.</span></span> <span data-ttu-id="da658-164">Стандартный вызов **ExecQuery** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="da658-164">A standard call to **ExecQuery** looks like the following:</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



<span data-ttu-id="da658-165">Обратите внимание, что вы создаете объект [**SwbemServices**](swbemservices.md) с моникером, который представляет соответствующее пространство имен и безопасность, а затем делает вызов **ExecQuery** через службу.</span><span class="sxs-lookup"><span data-stu-id="da658-165">Note that you create the [**SWbemServices**](swbemservices.md) object with a moniker that represents the appropriate namespace and security, then make the **ExecQuery** call through the service.</span></span> <span data-ttu-id="da658-166">Более подробное обсуждение см. в разделе [Создание скрипта WMI](creating-a-wmi-script.md) и [перечисление WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="da658-166">For a more complete discussion, see [Creating a WMI Script](creating-a-wmi-script.md) and [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="da658-167">Как и метод [**инстанцесоф**](swbemservices-instancesof.md) , метод **ExecQuery** всегда возвращает коллекцию [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="da658-167">Like the [**InstancesOf**](swbemservices-instancesof.md) method, the **ExecQuery** method always returns an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="da658-168">Таким образом, сценарий WMI должен перечислить коллекцию ExecQuery, чтобы получить доступ к каждому экземпляру управляемого ресурса в коллекции, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="da658-168">Thus your WMI script must enumerate the collection ExecQuery returns in order to access each managed resource instance in the collection, as shown here:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="da658-169">Другие методы [**SwbemServices**](swbemservices.md) , возвращающие [**SWbemObjectSet**](swbemobjectset.md) , включают [**ассоЦиаторсоф**](swbemservices-associatorsof.md), [**референцесто**](swbemservices-referencesto.md)и [**субклассесоф**](swbemservices-subclassesof.md).</span><span class="sxs-lookup"><span data-stu-id="da658-169">Other [**SWbemServices**](swbemservices.md) methods that return an [**SWbemObjectSet**](swbemobjectset.md) include [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md), and [**SubclassesOf**](swbemservices-subclassesof.md).</span></span>

<span data-ttu-id="da658-170">Запрос на возврат пустого результирующего набора не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="da658-170">It is not an error for the query to return an empty result set.</span></span> <span data-ttu-id="da658-171">Метод **ExecQuery** возвращает ключевые свойства независимо от того, запрашивается ли ключевое свойство в аргументе *стркуери* .</span><span class="sxs-lookup"><span data-stu-id="da658-171">The **ExecQuery** method returns key properties whether or not the key property is requested in the *strQuery* argument.</span></span> <span data-ttu-id="da658-172">Если при выполнении этого метода возникает ошибка и не используется флаг **вбемфлагретурниммедиатели** , то объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) не задается до тех пор, пока не будет произведена попытка получить доступ к возвращенному набору объектов.</span><span class="sxs-lookup"><span data-stu-id="da658-172">If an error occurs when executing this method and you do not use the **wbemFlagReturnImmediately** flag, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object is not set until you attempt to access the returned object set.</span></span> <span data-ttu-id="da658-173">Однако при использовании флага **вбемфлагретурнвхенкомплете** объект Err задается при вызове метода **ExecQuery** .</span><span class="sxs-lookup"><span data-stu-id="da658-173">However, if you use the **wbemFlagReturnWhenComplete** flag, the Err object is set when the **ExecQuery** method is called.</span></span>

<span data-ttu-id="da658-174">Существует ряд ограничений на количество ключевых слов **and** и **or** , которые могут использоваться в запросах WQL.</span><span class="sxs-lookup"><span data-stu-id="da658-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="da658-175">Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, что WMI вернет код ошибки **\_ \_ \_ нарушения квоты WBEM E** как значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da658-175">Large numbers of WQL keywords that are used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="da658-176">Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.</span><span class="sxs-lookup"><span data-stu-id="da658-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="da658-177">Примеры</span><span class="sxs-lookup"><span data-stu-id="da658-177">Examples</span></span>

<span data-ttu-id="da658-178">Следующий пример кода VBScript находит все диски на локальном компьютере и отображает идентификатор устройства и тип диска.</span><span class="sxs-lookup"><span data-stu-id="da658-178">The following VBScript code example locates all the disk drives on the local computer and displays the device ID and the type of the disk drive.</span></span>


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a><span data-ttu-id="da658-179">Требования</span><span class="sxs-lookup"><span data-stu-id="da658-179">Requirements</span></span>



| <span data-ttu-id="da658-180">Требование</span><span class="sxs-lookup"><span data-stu-id="da658-180">Requirement</span></span> | <span data-ttu-id="da658-181">Значение</span><span class="sxs-lookup"><span data-stu-id="da658-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da658-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da658-182">Minimum supported client</span></span><br/> | <span data-ttu-id="da658-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da658-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da658-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da658-184">Minimum supported server</span></span><br/> | <span data-ttu-id="da658-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da658-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da658-186">Header</span><span class="sxs-lookup"><span data-stu-id="da658-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="da658-187"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="da658-187"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="da658-188">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="da658-188">Type library</span></span><br/>             | <dl> <span data-ttu-id="da658-189"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="da658-189"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="da658-190">DLL</span><span class="sxs-lookup"><span data-stu-id="da658-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da658-191"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da658-191"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="da658-192">CLSID</span><span class="sxs-lookup"><span data-stu-id="da658-192">CLSID</span></span><br/>                    | <span data-ttu-id="da658-193">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="da658-193">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="da658-194">IID</span><span class="sxs-lookup"><span data-stu-id="da658-194">IID</span></span><br/>                      | <span data-ttu-id="da658-195">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="da658-195">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="da658-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da658-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da658-197">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="da658-197">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="da658-198">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="da658-198">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> <dt>

[<span data-ttu-id="da658-199">Запросы с помощью WQL</span><span class="sxs-lookup"><span data-stu-id="da658-199">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="da658-200">Создание скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="da658-200">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="da658-201">Перечисление WMI</span><span class="sxs-lookup"><span data-stu-id="da658-201">Enumerating WMI</span></span>](enumerating-wmi.md)
</dt> </dl>

 

