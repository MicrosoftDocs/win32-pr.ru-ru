---
description: Возвращает объект SWbemObjectSet.
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.tgt_platform: multiple
title: SWbemServices. Субклассесоф, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e8c23dee5ee3f0a1cf5babe37d0ccb6aa0a3ac7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711617"
---
# <a name="swbemservicessubclassesof-method"></a><span data-ttu-id="04f85-103">SWbemServices. Субклассесоф, метод</span><span class="sxs-lookup"><span data-stu-id="04f85-103">SWbemServices.SubclassesOf method</span></span>

<span data-ttu-id="04f85-104">Метод **субклассесоф** объекта [**SwbemServices**](swbemservices.md) возвращает объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="04f85-104">The **SubclassesOf** method of the [**SWbemServices**](swbemservices.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="04f85-105">Этот объект представляет собой коллекцию подклассов указанного класса.</span><span class="sxs-lookup"><span data-stu-id="04f85-105">This object is a collection of subclasses of a specified class.</span></span> <span data-ttu-id="04f85-106">Элементы в возвращаемой коллекции можно получить с помощью стандартных методов сбора.</span><span class="sxs-lookup"><span data-stu-id="04f85-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="04f85-107">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="04f85-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="04f85-108">Этот метод работает только для объектов класса.</span><span class="sxs-lookup"><span data-stu-id="04f85-108">This method only works for class objects.</span></span>

<span data-ttu-id="04f85-109">Метод вызывается в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="04f85-109">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="04f85-110">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="04f85-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="04f85-111">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="04f85-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="04f85-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04f85-112">Syntax</span></span>


```VB
objWbemObjectSet = .SubclassesOf( _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="04f85-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="04f85-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f85-114">*стрсуперкласс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="04f85-114">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04f85-115">Указывает имя родительского класса.</span><span class="sxs-lookup"><span data-stu-id="04f85-115">Specifies a parent class name.</span></span> <span data-ttu-id="04f85-116">Только подклассы этого класса возвращают в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="04f85-116">Only subclasses of this class return in the enumerator.</span></span> <span data-ttu-id="04f85-117">Если оставить этот параметр пустым и если *ифлагс* имеет значение **вбемкуерифлагшаллов**, возвращаются только классы верхнего уровня (то есть классы, не имеющие родительского класса).</span><span class="sxs-lookup"><span data-stu-id="04f85-117">If you leave this parameter blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="04f85-118">Если этот параметр пуст, а *ифлагс* — **вбемкуерифлагдип** , возвращаются все классы в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="04f85-118">If this parameter is blank and *iFlags* is **wbemQueryFlagDeep** all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="04f85-119">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="04f85-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04f85-120">Определяет, как детализированный вызов перечисляет.</span><span class="sxs-lookup"><span data-stu-id="04f85-120">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="04f85-121">Значения по умолчанию для этого параметра — **вбемфлагретурниммедиатели** и **вбемкуерифлагдип**.</span><span class="sxs-lookup"><span data-stu-id="04f85-121">The default values for this parameter are **wbemFlagReturnImmediately** and **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="04f85-122">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="04f85-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="04f85-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="04f85-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="04f85-124">Заставляет перечисление включать только непосредственные подклассы указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="04f85-124">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="04f85-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="04f85-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="04f85-126">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="04f85-126">Default for this parameter.</span></span> <span data-ttu-id="04f85-127">Это значение приводит к принудительному перечислению для всех подклассов, которые являются производными от указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="04f85-127">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="04f85-128">Родительский класс не возвращается в перечислении.</span><span class="sxs-lookup"><span data-stu-id="04f85-128">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="04f85-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="04f85-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="04f85-130">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="04f85-130">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="04f85-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="04f85-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="04f85-132">Вызывает блокирование этого вызова до завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="04f85-132">Causes this call to block until the call has completed.</span></span> <span data-ttu-id="04f85-133">Этот флаг вызывает метод в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="04f85-133">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="04f85-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="04f85-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="04f85-135">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="04f85-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="04f85-136">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="04f85-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="04f85-137">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="04f85-137">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04f85-138">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="04f85-138">Typically, this is undefined.</span></span> <span data-ttu-id="04f85-139">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="04f85-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider servicing the request.</span></span> <span data-ttu-id="04f85-140">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="04f85-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f85-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04f85-141">Return value</span></span>

<span data-ttu-id="04f85-142">Если метод выполнен успешно, возвращается объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="04f85-142">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="04f85-143">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="04f85-143">Error codes</span></span>

<span data-ttu-id="04f85-144">После завершения метода **субклассесоф** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="04f85-144">After the completion of the **SubclassesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="04f85-145">Возвращенная коллекция с нулевым числом элементов не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="04f85-145">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="04f85-146">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="04f85-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="04f85-147">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="04f85-147">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="04f85-148">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="04f85-148">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="04f85-149">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="04f85-149">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="04f85-150">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="04f85-150">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="04f85-151">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="04f85-151">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="04f85-152">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="04f85-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="04f85-153">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="04f85-153">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="04f85-154">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="04f85-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="04f85-155">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="04f85-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="04f85-156">Примеры</span><span class="sxs-lookup"><span data-stu-id="04f85-156">Examples</span></span>

<span data-ttu-id="04f85-157">В следующем примере PowerShell показано, как получить подклассы класса в удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="04f85-157">The following PowerShell sample shows how to retrieve the subclasses of a class on a remote system.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="04f85-158">Требования</span><span class="sxs-lookup"><span data-stu-id="04f85-158">Requirements</span></span>



| <span data-ttu-id="04f85-159">Требование</span><span class="sxs-lookup"><span data-stu-id="04f85-159">Requirement</span></span> | <span data-ttu-id="04f85-160">Значение</span><span class="sxs-lookup"><span data-stu-id="04f85-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04f85-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04f85-161">Minimum supported client</span></span><br/> | <span data-ttu-id="04f85-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04f85-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04f85-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04f85-163">Minimum supported server</span></span><br/> | <span data-ttu-id="04f85-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04f85-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04f85-165">Header</span><span class="sxs-lookup"><span data-stu-id="04f85-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="04f85-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04f85-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="04f85-167">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="04f85-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="04f85-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="04f85-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="04f85-169">DLL</span><span class="sxs-lookup"><span data-stu-id="04f85-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04f85-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04f85-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="04f85-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="04f85-171">CLSID</span></span><br/>                    | <span data-ttu-id="04f85-172">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="04f85-172">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="04f85-173">IID</span><span class="sxs-lookup"><span data-stu-id="04f85-173">IID</span></span><br/>                      | <span data-ttu-id="04f85-174">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="04f85-174">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="04f85-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04f85-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f85-176">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="04f85-176">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="04f85-177">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="04f85-177">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




