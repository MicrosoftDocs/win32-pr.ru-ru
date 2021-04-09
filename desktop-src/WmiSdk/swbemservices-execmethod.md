---
description: Выполняет метод, экспортируемый поставщиком метода.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Кмесод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c95bc3b0fa85d7c682f9ffd2436439da9a05763f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080892"
---
# <a name="swbemservicesexecmethod-method"></a><span data-ttu-id="75c29-103">SWbemServices.Exeметод Кмесод</span><span class="sxs-lookup"><span data-stu-id="75c29-103">SWbemServices.ExecMethod method</span></span>

<span data-ttu-id="75c29-104">Метод **ExecMethod** объекта [**SwbemServices**](swbemservices.md) выполняет метод, экспортируемый поставщиком метода.</span><span class="sxs-lookup"><span data-stu-id="75c29-104">The **ExecMethod** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="75c29-105">Этот метод блокируется, пока выполняется метод, перенаправляемый соответствующему поставщику.</span><span class="sxs-lookup"><span data-stu-id="75c29-105">This method blocks while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="75c29-106">Затем информация и состояние возвращаются.</span><span class="sxs-lookup"><span data-stu-id="75c29-106">The information and status are then returned.</span></span> <span data-ttu-id="75c29-107">Поставщик, а не WMI, реализует метод.</span><span class="sxs-lookup"><span data-stu-id="75c29-107">The provider, rather than WMI, implements the method.</span></span>

<span data-ttu-id="75c29-108">Этот метод вызывается в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="75c29-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="75c29-109">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="75c29-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="75c29-110">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="75c29-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="75c29-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75c29-111">Syntax</span></span>


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="75c29-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="75c29-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c29-113">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="75c29-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="75c29-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="75c29-114">Required.</span></span> <span data-ttu-id="75c29-115">Строка, содержащая путь к объекту, для которого выполняется метод.</span><span class="sxs-lookup"><span data-stu-id="75c29-115">String that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="75c29-116">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="75c29-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="75c29-117">*стрмесоднаме*</span><span class="sxs-lookup"><span data-stu-id="75c29-117">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="75c29-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="75c29-118">Required.</span></span> <span data-ttu-id="75c29-119">Имя метода для объекта.</span><span class="sxs-lookup"><span data-stu-id="75c29-119">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="75c29-120">*обжвбеминпарамс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="75c29-120">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75c29-121">Объект [**SWbemObject**](swbemobject.md) , содержащий входные параметры для выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="75c29-121">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="75c29-122">По умолчанию этот параметр не определен.</span><span class="sxs-lookup"><span data-stu-id="75c29-122">By default, this parameter is undefined.</span></span> <span data-ttu-id="75c29-123">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="75c29-123">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="75c29-124">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="75c29-124">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75c29-125">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="75c29-125">Reserved.</span></span> <span data-ttu-id="75c29-126">Это значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="75c29-126">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="75c29-127">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="75c29-127">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75c29-128">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="75c29-128">Typically, this is undefined.</span></span> <span data-ttu-id="75c29-129">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="75c29-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="75c29-130">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="75c29-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c29-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75c29-131">Return value</span></span>

<span data-ttu-id="75c29-132">Если метод выполнен успешно, возвращается объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="75c29-132">If the method is successful, an [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="75c29-133">Возвращаемый объект содержит выходные параметры и возвращаемое значение для выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="75c29-133">The returned object contains the out parameters and return value for the method that is being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="75c29-134">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="75c29-134">Error codes</span></span>

<span data-ttu-id="75c29-135">После завершения метода **ExecMethod** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="75c29-135">After the completion of the **ExecMethod** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="75c29-136">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="75c29-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="75c29-137">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="75c29-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="75c29-138">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="75c29-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="75c29-139">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="75c29-139">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75c29-140">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="75c29-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="75c29-141">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="75c29-141">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75c29-142">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="75c29-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="75c29-143">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="75c29-143">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="75c29-144">**вбемерринвалидмесод** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="75c29-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="75c29-145">Запрошенный метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="75c29-145">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="75c29-146">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="75c29-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="75c29-147">Текущий пользователь не имеет разрешения на выполнение метода.</span><span class="sxs-lookup"><span data-stu-id="75c29-147">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75c29-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75c29-148">Remarks</span></span>

<span data-ttu-id="75c29-149">Используйте **SWbemServices.Exeкмесод** в качестве альтернативы прямой доступ для выполнения [*метода поставщика*](gloss-p.md) в случаях, когда невозможно выполнить метод напрямую.</span><span class="sxs-lookup"><span data-stu-id="75c29-149">Use **SWbemServices.ExecMethod** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="75c29-150">Метод **ExecMethod** позволяет получать выходные параметры, если поставщик предоставляет их, с языком сценариев, который не поддерживает выходные параметры.</span><span class="sxs-lookup"><span data-stu-id="75c29-150">The **ExecMethod** method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="75c29-151">В противном случае для вызова метода рекомендуется использовать прямой доступ.</span><span class="sxs-lookup"><span data-stu-id="75c29-151">Otherwise, the recommended means of invoking a method is to use direct access.</span></span> <span data-ttu-id="75c29-152">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="75c29-152">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="75c29-153">Например, следующий пример кода, вызывающий метод [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider в [**\_ службе Win32**](/windows/desktop/CIMWin32Prov/win32-service) , использует прямой доступ.</span><span class="sxs-lookup"><span data-stu-id="75c29-153">For example, the following code example that calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) uses direct access.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="75c29-154">В этом примере вызывается **SWbemServices.Exeкмесод** для выполнения метода [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="75c29-154">This example calls **SWbemServices.ExecMethod** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="75c29-155">Обратите внимание, что путь к объекту необходим, так как **SWbemServices.Exeкмесод** не работает над объектом, в отличие от [**SWbemObject.Exeкмесод**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="75c29-155">Note that an object path is required because **SWbemServices.ExecMethod** is not operating on the object already, unlike [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



<span data-ttu-id="75c29-156">Для метода **SWbemServices.Exeкмесод** требуется путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="75c29-156">The **SWbemServices.ExecMethod** method requires an object path.</span></span> <span data-ttu-id="75c29-157">Если в скрипте уже содержится объект [**SWbemObject**](swbemobject.md) , используйте метод [**SWbemObject.Exeкмесод**](swbemobject-execmethod-.md) .</span><span class="sxs-lookup"><span data-stu-id="75c29-157">If the script already holds an [**SWbemObject**](swbemobject.md) object, use the [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="75c29-158">Примеры</span><span class="sxs-lookup"><span data-stu-id="75c29-158">Examples</span></span>

<span data-ttu-id="75c29-159">В следующем примере показан метод **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="75c29-159">The following example shows the **ExecMethod** method.</span></span> <span data-ttu-id="75c29-160">Скрипт создает объект [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , который представляет процесс, выполняющий программу «Блокнот».</span><span class="sxs-lookup"><span data-stu-id="75c29-160">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="75c29-161">Он показывает [**настройку объекта параметров**](swbemmethod-inparameters.md) и способ получения результатов из объекта [**параметров**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="75c29-161">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="75c29-162">Сведения о скрипте, отображающем те же операции, выполняемые асинхронно, см. в разделе [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="75c29-162">For a script that shows the same operations performed asynchronously, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span> <span data-ttu-id="75c29-163">Пример использования прямого доступа см. [в разделе Создание метода в классе Win32 \_ процесс](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="75c29-163">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="75c29-164">Пример той же операции с помощью [**SWbemObject**](swbemobject.md)см. в разделе [**SWbemObject.Exeкмесод**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="75c29-164">For an example of the same operation using an [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="75c29-165">Требования</span><span class="sxs-lookup"><span data-stu-id="75c29-165">Requirements</span></span>



| <span data-ttu-id="75c29-166">Требование</span><span class="sxs-lookup"><span data-stu-id="75c29-166">Requirement</span></span> | <span data-ttu-id="75c29-167">Значение</span><span class="sxs-lookup"><span data-stu-id="75c29-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75c29-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75c29-168">Minimum supported client</span></span><br/> | <span data-ttu-id="75c29-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75c29-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75c29-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75c29-170">Minimum supported server</span></span><br/> | <span data-ttu-id="75c29-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75c29-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75c29-172">Header</span><span class="sxs-lookup"><span data-stu-id="75c29-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="75c29-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="75c29-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="75c29-174">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="75c29-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="75c29-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="75c29-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="75c29-176">DLL</span><span class="sxs-lookup"><span data-stu-id="75c29-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75c29-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75c29-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="75c29-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="75c29-178">CLSID</span></span><br/>                    | <span data-ttu-id="75c29-179">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="75c29-179">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="75c29-180">IID</span><span class="sxs-lookup"><span data-stu-id="75c29-180">IID</span></span><br/>                      | <span data-ttu-id="75c29-181">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="75c29-181">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="75c29-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75c29-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c29-183">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="75c29-183">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="75c29-184">**SWbemObject.ExeКмесод\_**</span><span class="sxs-lookup"><span data-stu-id="75c29-184">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="75c29-185">Вызов метода поставщика</span><span class="sxs-lookup"><span data-stu-id="75c29-185">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="75c29-186">Управление сведениями о классе и экземпляре</span><span class="sxs-lookup"><span data-stu-id="75c29-186">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

