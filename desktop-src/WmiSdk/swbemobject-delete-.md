---
description: Метод DELETE \_ объекта SWbemObject удаляет либо текущий класс, либо текущий экземпляр.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: Метод SWbemObject.Delete_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d994c8a9b9e0af9d4bd884c89cd67280513c9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081113"
---
# <a name="swbemobjectdelete_-method"></a><span data-ttu-id="eeb6b-103">SWbemObject. Delete, \_ метод</span><span class="sxs-lookup"><span data-stu-id="eeb6b-103">SWbemObject.Delete\_ method</span></span>

<span data-ttu-id="eeb6b-104">Метод **DELETE \_** объекта [**SWbemObject**](swbemobject.md) удаляет либо текущий класс, либо текущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-104">The **Delete\_** method of the [**SWbemObject**](swbemobject.md) object deletes either the current class or the current instance.</span></span> <span data-ttu-id="eeb6b-105">Если динамический поставщик предоставляет класс или экземпляр, то иногда невозможно удалить этот объект, если поставщик не поддерживает удаление класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-105">If a dynamic provider supplies the class or instance, it is sometimes not possible to delete this object unless the provider supports class or instance deletion.</span></span> <span data-ttu-id="eeb6b-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eeb6b-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb6b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eeb6b-107">Syntax</span></span>


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eeb6b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eeb6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb6b-109">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eeb6b-109">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb6b-110">Зарезервировано и должно быть равно 0 (нулю), если оно указано.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-110">Reserved and must be 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6b-111">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eeb6b-111">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb6b-112">Обычно этот параметр не определен.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-112">This parameter is typically undefined.</span></span> <span data-ttu-id="eeb6b-113">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-113">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="eeb6b-114">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-114">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb6b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eeb6b-115">Return value</span></span>

<span data-ttu-id="eeb6b-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eeb6b-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="eeb6b-117">Error codes</span></span>

<span data-ttu-id="eeb6b-118">После завершения метода **DELETE \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-118">After completion of the **Delete\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="eeb6b-119">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="eeb6b-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="eeb6b-120">Текущий контекст не имеет достаточных прав безопасности для удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-120">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6b-121">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="eeb6b-121">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eeb6b-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-122">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6b-123">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="eeb6b-123">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="eeb6b-124">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-124">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6b-125">**вбемерринвалидоператион** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="eeb6b-125">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="eeb6b-126">Не удается удалить объект.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-126">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6b-127">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="eeb6b-127">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="eeb6b-128">Объект не существует.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-128">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6b-129">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="eeb6b-129">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eeb6b-130">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-130">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eeb6b-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eeb6b-131">Remarks</span></span>

<span data-ttu-id="eeb6b-132">Метод **DELETE \_** завершается ошибкой, если создан новый экземпляр [**SWbemObject**](swbemobject.md) , но для ключевого свойства не указано значение.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-132">The **Delete\_** method fails if a new instance of [**SWbemObject**](swbemobject.md) is created, but no value is supplied for the key property.</span></span> <span data-ttu-id="eeb6b-133">Инструментарий управления Windows (WMI) (WMI) автоматически создает значение глобального уникального идентификатора (GUID), но значение идентификатора GUID не принимается функцией **SWbemObject. Delete \_**.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-133">Windows Management Instrumentation (WMI) generates a globally unique identifier (GUID) value automatically, but a GUID value is not accepted by **SWbemObject.Delete\_**.</span></span> <span data-ttu-id="eeb6b-134">В этом случае [**SwbemServices. Delete**](swbemservices-delete.md), который использует путь к объекту, работает.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-134">In this case, [**SWbemServices.Delete**](swbemservices-delete.md), which uses the object path works.</span></span> <span data-ttu-id="eeb6b-135">Обратите внимание, что объект [**свбемобжектпас**](swbemobjectpath.md) возвращается методом [**SWbemObject \_ .**](swbemobject-put-.md) WHERE после фиксации объекта в WMI.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-135">Note that an [**SWbemObjectPath**](swbemobjectpath.md) object is returned by the [**SWbemObject.Put\_**](swbemobject-put-.md) method after an object is committed to WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="eeb6b-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="eeb6b-136">Examples</span></span>

<span data-ttu-id="eeb6b-137">В следующем примере создается новый класс. Добавляет свойство ключа; записывает новый класс в репозиторий; и отображает путь к новому объекту класса.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-137">The following example creates a new class; adds a key property; writes the new class to the repository; and displays the path of the new class object.</span></span> <span data-ttu-id="eeb6b-138">Затем скрипт порождает экземпляр нового класса. записывает его; и отображает путь.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-138">The script then spawns an instance of the new class; writes it; and displays the path.</span></span> <span data-ttu-id="eeb6b-139">Обратите внимание, что сценарий удаляет класс и его экземпляры из репозитория, просто удаляя класс.</span><span class="sxs-lookup"><span data-stu-id="eeb6b-139">Note that the script deletes both the class and its instances from the repository by simply deleting the class.</span></span>


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="eeb6b-140">Требования</span><span class="sxs-lookup"><span data-stu-id="eeb6b-140">Requirements</span></span>



| <span data-ttu-id="eeb6b-141">Требование</span><span class="sxs-lookup"><span data-stu-id="eeb6b-141">Requirement</span></span> | <span data-ttu-id="eeb6b-142">Значение</span><span class="sxs-lookup"><span data-stu-id="eeb6b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb6b-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eeb6b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb6b-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eeb6b-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eeb6b-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eeb6b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb6b-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eeb6b-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eeb6b-147">Header</span><span class="sxs-lookup"><span data-stu-id="eeb6b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeb6b-148"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeb6b-148"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eeb6b-149">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eeb6b-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="eeb6b-150"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eeb6b-150"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eeb6b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="eeb6b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeb6b-152"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeb6b-152"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eeb6b-153">CLSID</span><span class="sxs-lookup"><span data-stu-id="eeb6b-153">CLSID</span></span><br/>                    | <span data-ttu-id="eeb6b-154">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="eeb6b-154">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="eeb6b-155">IID</span><span class="sxs-lookup"><span data-stu-id="eeb6b-155">IID</span></span><br/>                      | <span data-ttu-id="eeb6b-156">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="eeb6b-156">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




