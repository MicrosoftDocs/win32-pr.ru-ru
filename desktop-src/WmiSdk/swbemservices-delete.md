---
description: Удаляет класс или экземпляр, указанный в пути объекта. Удалять можно только объекты из текущего пространства имен.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Метод SWbemServices. Delete (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497835"
---
# <a name="swbemservicesdelete-method"></a><span data-ttu-id="10d14-104">SWbemServices. Delete, метод</span><span class="sxs-lookup"><span data-stu-id="10d14-104">SWbemServices.Delete method</span></span>

<span data-ttu-id="10d14-105">Метод **Delete** объекта [**SwbemServices**](swbemservices.md) удаляет класс или экземпляр, указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="10d14-105">The **Delete** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance that is specified in the object path.</span></span> <span data-ttu-id="10d14-106">Удалять можно только объекты из текущего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="10d14-106">You can only delete objects in the current namespace.</span></span>

<span data-ttu-id="10d14-107">Если динамический поставщик предоставляет класс или экземпляр, удалить этот объект нельзя, если поставщик не поддерживает удаление класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="10d14-107">If a dynamic provider supplies the class or instance, you cannot delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="10d14-108">Этот метод вызывается в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="10d14-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="10d14-109">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="10d14-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="10d14-110">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="10d14-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="10d14-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10d14-111">Syntax</span></span>


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="10d14-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="10d14-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d14-113">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="10d14-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="10d14-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="10d14-114">Required.</span></span> <span data-ttu-id="10d14-115">Строка, содержащая путь к объекту, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="10d14-115">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="10d14-116">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="10d14-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d14-117">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="10d14-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10d14-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="10d14-118">Reserved.</span></span> <span data-ttu-id="10d14-119">Это значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="10d14-119">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="10d14-120">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="10d14-120">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10d14-121">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="10d14-121">Typically, this is undefined.</span></span> <span data-ttu-id="10d14-122">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает.</span><span class="sxs-lookup"><span data-stu-id="10d14-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="10d14-123">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="10d14-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d14-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10d14-124">Return value</span></span>

<span data-ttu-id="10d14-125">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="10d14-125">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10d14-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="10d14-126">Error codes</span></span>

<span data-ttu-id="10d14-127">После завершения метода **Delete** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="10d14-127">After the completion of the **Delete** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="10d14-128">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="10d14-128">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="10d14-129">Текущий контекст не имеет достаточных прав безопасности для удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="10d14-129">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="10d14-130">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="10d14-130">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="10d14-131">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="10d14-131">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="10d14-132">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="10d14-132">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="10d14-133">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="10d14-133">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="10d14-134">**вбемерринвалидоператион** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="10d14-134">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="10d14-135">Не удается удалить объект.</span><span class="sxs-lookup"><span data-stu-id="10d14-135">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="10d14-136">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="10d14-136">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="10d14-137">Объект не существует.</span><span class="sxs-lookup"><span data-stu-id="10d14-137">Object does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="10d14-138">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="10d14-138">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="10d14-139">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="10d14-139">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10d14-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10d14-140">Remarks</span></span>

<span data-ttu-id="10d14-141">Метод **SwbemServices. Delete** может использоваться, когда свойству ключа объекта не присвоено значение, так как для этого метода в качестве входных данных требуется только путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="10d14-141">The **SWbemServices.Delete** method can be used when the key property for the object is not given a value, because this method only requires an object path as input.</span></span> <span data-ttu-id="10d14-142">Этот метод можно использовать в ситуациях, когда [**SWbemObject. Delete \_**](swbemobject-delete-.md) завершается неудачей для отсутствия значения ключа.</span><span class="sxs-lookup"><span data-stu-id="10d14-142">This method can be used in situations where [**SWbemObject.Delete\_**](swbemobject-delete-.md) fails for lack of a key value.</span></span> <span data-ttu-id="10d14-143">Если объект зафиксирован в WMI с помощью [**SWbemObject. \_ постановки**](swbemobject-put-.md), объект [**свбемобжектпас**](swbemobjectpath.md) был получен через вызов.</span><span class="sxs-lookup"><span data-stu-id="10d14-143">If the object is committed to WMI through [**SWbemObject.Put\_**](swbemobject-put-.md), then an [**SWbemObjectPath**](swbemobjectpath.md) object was obtained through the call.</span></span>

## <a name="examples"></a><span data-ttu-id="10d14-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="10d14-144">Examples</span></span>

<span data-ttu-id="10d14-145">В следующем примере создается новый класс, добавляется свойство, которое не является ключом, записывает новый класс в репозиторий и отображает путь к новому объекту класса.</span><span class="sxs-lookup"><span data-stu-id="10d14-145">The following example creates a new class, adds a property that is not a key, writes the new class to the repository, and displays the path of the new class object.</span></span> <span data-ttu-id="10d14-146">Затем скрипт порождает экземпляр нового класса, записывает экземпляр и отображает путь.</span><span class="sxs-lookup"><span data-stu-id="10d14-146">The script then spawns an instance of the new class, writes the instance, and displays the path.</span></span> <span data-ttu-id="10d14-147">Обратите внимание, что скрипт удаляет класс и его экземпляры из репозитория, удаляя класс.</span><span class="sxs-lookup"><span data-stu-id="10d14-147">Note that the script deletes both the class and its instances from the repository by deleting the class.</span></span> <span data-ttu-id="10d14-148">Дополнительные сведения о классах и экземплярах WMI см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md) и [модель CIM](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="10d14-148">For more information about WMI classes and instances, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Common Information Model](common-information-model.md).</span></span>


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="10d14-149">Требования</span><span class="sxs-lookup"><span data-stu-id="10d14-149">Requirements</span></span>



| <span data-ttu-id="10d14-150">Требование</span><span class="sxs-lookup"><span data-stu-id="10d14-150">Requirement</span></span> | <span data-ttu-id="10d14-151">Значение</span><span class="sxs-lookup"><span data-stu-id="10d14-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10d14-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10d14-152">Minimum supported client</span></span><br/> | <span data-ttu-id="10d14-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10d14-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10d14-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10d14-154">Minimum supported server</span></span><br/> | <span data-ttu-id="10d14-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10d14-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10d14-156">Header</span><span class="sxs-lookup"><span data-stu-id="10d14-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="10d14-157"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10d14-157"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="10d14-158">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="10d14-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="10d14-159"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="10d14-159"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="10d14-160">DLL</span><span class="sxs-lookup"><span data-stu-id="10d14-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10d14-161"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d14-161"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="10d14-162">CLSID</span><span class="sxs-lookup"><span data-stu-id="10d14-162">CLSID</span></span><br/>                    | <span data-ttu-id="10d14-163">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="10d14-163">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="10d14-164">IID</span><span class="sxs-lookup"><span data-stu-id="10d14-164">IID</span></span><br/>                      | <span data-ttu-id="10d14-165">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="10d14-165">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="10d14-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10d14-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d14-167">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="10d14-167">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="10d14-168">**свбемобжектпас**</span><span class="sxs-lookup"><span data-stu-id="10d14-168">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

 




