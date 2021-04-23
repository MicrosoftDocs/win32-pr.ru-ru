---
description: Метод ExecMethod \_ объекта SWbemObject выполняет метод, экспортированный поставщиком метода.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: Метод SWbemObject.ExecMethod_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155830"
---
# <a name="swbemobjectexecmethod_-method"></a><span data-ttu-id="9d09a-103">SWbemObject.Exe\_ метод кмесод</span><span class="sxs-lookup"><span data-stu-id="9d09a-103">SWbemObject.ExecMethod\_ method</span></span>

<span data-ttu-id="9d09a-104">Метод **ExecMethod \_** объекта [**SWbemObject**](swbemobject.md) выполняет метод, экспортированный поставщиком метода.</span><span class="sxs-lookup"><span data-stu-id="9d09a-104">The **ExecMethod\_** method of the [**SWbemObject**](swbemobject.md) object executes a method exported by a method provider.</span></span>

<span data-ttu-id="9d09a-105">Этот метод приостанавливается, пока выполняется метод, перенаправляемый соответствующему поставщику.</span><span class="sxs-lookup"><span data-stu-id="9d09a-105">This method pauses while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="9d09a-106">Затем информация и состояние возвращаются.</span><span class="sxs-lookup"><span data-stu-id="9d09a-106">The information and status are then returned.</span></span> <span data-ttu-id="9d09a-107">Поставщик, а не WMI, реализует метод.</span><span class="sxs-lookup"><span data-stu-id="9d09a-107">The provider rather than WMI implements the method.</span></span>

<span data-ttu-id="9d09a-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9d09a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d09a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d09a-109">Syntax</span></span>


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9d09a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d09a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d09a-111">*стрмесоднаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d09a-111">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9d09a-112">Required.</span></span> <span data-ttu-id="9d09a-113">Имя метода для объекта.</span><span class="sxs-lookup"><span data-stu-id="9d09a-113">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="9d09a-114">*обжвбеминпарамс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9d09a-114">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-115">Это объект [**SWbemObject**](swbemobject.md) , содержащий входные параметры для выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="9d09a-115">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="9d09a-116">По умолчанию этот параметр не определен.</span><span class="sxs-lookup"><span data-stu-id="9d09a-116">By default, this parameter is undefined.</span></span> <span data-ttu-id="9d09a-117">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9d09a-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d09a-118">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9d09a-118">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-119">Зарезервированное значение и должно быть равно 0 (нуль), если оно задано.</span><span class="sxs-lookup"><span data-stu-id="9d09a-119">Reserved and must be set to 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="9d09a-120">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9d09a-120">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-121">Как правило, он не определен.</span><span class="sxs-lookup"><span data-stu-id="9d09a-121">Typically, it is undefined.</span></span> <span data-ttu-id="9d09a-122">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="9d09a-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="9d09a-123">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="9d09a-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d09a-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d09a-124">Return value</span></span>

<span data-ttu-id="9d09a-125">Если этот метод успешно выполнен, объект [**SWbemObject**](swbemobject.md) возвращает.</span><span class="sxs-lookup"><span data-stu-id="9d09a-125">If this method is successful, an [**SWbemObject**](swbemobject.md) object returns.</span></span> <span data-ttu-id="9d09a-126">Возвращаемый объект содержит выходные параметры и возвращаемое значение для выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="9d09a-126">The returned object contains the out parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d09a-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9d09a-127">Error codes</span></span>

<span data-ttu-id="9d09a-128">После завершения метода **ExecMethod \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="9d09a-128">After the completion of the **ExecMethod\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9d09a-129">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9d09a-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-130">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="9d09a-130">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9d09a-131">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="9d09a-131">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-132">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="9d09a-132">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9d09a-133">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9d09a-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-134">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="9d09a-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9d09a-135">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9d09a-135">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-136">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="9d09a-136">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9d09a-137">**вбемерринвалидмесод** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="9d09a-137">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-138">Запрошенный метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="9d09a-138">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="9d09a-139">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="9d09a-139">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="9d09a-140">Текущий пользователь не имеет разрешения на выполнение метода.</span><span class="sxs-lookup"><span data-stu-id="9d09a-140">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d09a-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d09a-141">Remarks</span></span>

<span data-ttu-id="9d09a-142">Этот метод аналогичен [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md), но он работает непосредственно с объектом, метод которого должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="9d09a-142">This method is similar to [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), but it operates directly on the object whose method is to be executed.</span></span> <span data-ttu-id="9d09a-143">Например, следующий пример кода вызывает метод [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider в [**\_ службе Win32**](/windows/desktop/CIMWin32Prov/win32-service) и использует [прямой доступ](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="9d09a-143">For example, the following code example calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) and uses [direct access](manipulating-class-and-instance-information.md).</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="9d09a-144">Эта версия вызывает **SWbemObject.Exeкмесод \_** для выполнения метода [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="9d09a-144">This version calls **SWbemObject.ExecMethod\_** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



<span data-ttu-id="9d09a-145">Используйте **SWbemObject.Exeкмесод \_** в качестве альтернативы прямой доступ для выполнения [*метода поставщика*](gloss-p.md) в случаях, когда невозможно выполнить метод напрямую.</span><span class="sxs-lookup"><span data-stu-id="9d09a-145">Use **SWbemObject.ExecMethod\_** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="9d09a-146">Например, можно использовать **SWbemObject.Exeкмесод \_** с языком сценариев, который не поддерживает выходные параметры, если метод имеет параметры out.</span><span class="sxs-lookup"><span data-stu-id="9d09a-146">For example, you would use **SWbemObject.ExecMethod\_** with a scripting language that does not support output parameters if your method has out parameters.</span></span> <span data-ttu-id="9d09a-147">В противном случае для вызова метода рекомендуется использовать прямой доступ.</span><span class="sxs-lookup"><span data-stu-id="9d09a-147">Otherwise, the recommended means of invoking a method is to use direct access.</span></span>

-   <span data-ttu-id="9d09a-148">Метод **SWbemObject.Exeкмесод \_** предполагает, что объект, представленный [**SWbemObject**](swbemobject.md) , содержит метод для выполнения.</span><span class="sxs-lookup"><span data-stu-id="9d09a-148">The **SWbemObject.ExecMethod\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="9d09a-149">Напротив, для [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md) требуется путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="9d09a-149">By contrast, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requires an object path.</span></span> <span data-ttu-id="9d09a-150">Используйте **SWbemObject.Exeкмесод \_** , если вы уже получили объект, метод которого необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="9d09a-150">Use **SWbemObject.ExecMethod\_** if you already have obtained the object whose method you want to execute.</span></span>

## <a name="examples"></a><span data-ttu-id="9d09a-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="9d09a-151">Examples</span></span>

<span data-ttu-id="9d09a-152">В следующем примере показан метод [**ExecMethod**](swbemservices-execmethod.md) . Скрипт создает объект [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , представляющий процесс, выполняемый в блокноте.</span><span class="sxs-lookup"><span data-stu-id="9d09a-152">The following example shows the [**ExecMethod**](swbemservices-execmethod.md) method.The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object representing a process running Notepad.</span></span> <span data-ttu-id="9d09a-153">Дополнительные сведения о скриптах, иллюстрирующих те же операции, выполняемые асинхронно, см. в разделе [**SWbemObject.Exeкмесодасинк \_**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="9d09a-153">For more information about a script illustrating the same operations performed asynchronously, see [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md).</span></span> <span data-ttu-id="9d09a-154">Пример использования прямого доступа см. в разделе [**Создание метода в классе Win32 \_ процесс**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span><span class="sxs-lookup"><span data-stu-id="9d09a-154">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span></span> <span data-ttu-id="9d09a-155">Пример той же операции с помощью объекта [**SwbemServices**](swbemservices.md) см. в разделе **SWbemServices.Exeкмесод**.</span><span class="sxs-lookup"><span data-stu-id="9d09a-155">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see **SWbemServices.ExecMethod**.</span></span>


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="9d09a-156">Требования</span><span class="sxs-lookup"><span data-stu-id="9d09a-156">Requirements</span></span>



| <span data-ttu-id="9d09a-157">Требование</span><span class="sxs-lookup"><span data-stu-id="9d09a-157">Requirement</span></span> | <span data-ttu-id="9d09a-158">Значение</span><span class="sxs-lookup"><span data-stu-id="9d09a-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d09a-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d09a-159">Minimum supported client</span></span><br/> | <span data-ttu-id="9d09a-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d09a-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d09a-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d09a-161">Minimum supported server</span></span><br/> | <span data-ttu-id="9d09a-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d09a-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d09a-163">Header</span><span class="sxs-lookup"><span data-stu-id="9d09a-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d09a-164"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d09a-164"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d09a-165">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9d09a-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d09a-166"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9d09a-166"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9d09a-167">DLL</span><span class="sxs-lookup"><span data-stu-id="9d09a-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d09a-168"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d09a-168"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d09a-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="9d09a-169">CLSID</span></span><br/>                    | <span data-ttu-id="9d09a-170">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="9d09a-170">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="9d09a-171">IID</span><span class="sxs-lookup"><span data-stu-id="9d09a-171">IID</span></span><br/>                      | <span data-ttu-id="9d09a-172">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="9d09a-172">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="9d09a-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d09a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d09a-174">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="9d09a-174">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="9d09a-175">**SWbemObject.ExeКмесодасинк\_**</span><span class="sxs-lookup"><span data-stu-id="9d09a-175">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="9d09a-176">**SWbemServices.ExeКмесод**</span><span class="sxs-lookup"><span data-stu-id="9d09a-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> </dl>

 

