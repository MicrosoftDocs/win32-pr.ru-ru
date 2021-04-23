---
description: Создает перечислитель, возвращающий экземпляры указанного класса в соответствии с заданным пользователем критерием выбора.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: SWbemServices. Инстанцесоф, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913188"
---
# <a name="swbemservicesinstancesof-method"></a><span data-ttu-id="5e47d-103">SWbemServices. Инстанцесоф, метод</span><span class="sxs-lookup"><span data-stu-id="5e47d-103">SWbemServices.InstancesOf method</span></span>

<span data-ttu-id="5e47d-104">Метод **инстанцесоф** объекта [**SwbemServices**](swbemservices.md) создает перечислитель, который возвращает экземпляры указанного класса в соответствии с заданным пользователем критерием выбора.</span><span class="sxs-lookup"><span data-stu-id="5e47d-104">The **InstancesOf** method of the [**SWbemServices**](swbemservices.md) object creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria.</span></span> <span data-ttu-id="5e47d-105">Этот метод реализует простой запрос.</span><span class="sxs-lookup"><span data-stu-id="5e47d-105">This method implements a simple query.</span></span> <span data-ttu-id="5e47d-106">Более сложные запросы могут потребовать использования [**SWbemServices.Exeккуери**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="5e47d-106">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="5e47d-107">Метод вызывается в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="5e47d-107">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="5e47d-108">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5e47d-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="5e47d-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5e47d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e47d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e47d-110">Syntax</span></span>


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5e47d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e47d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e47d-112">*стркласс*</span><span class="sxs-lookup"><span data-stu-id="5e47d-112">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="5e47d-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5e47d-113">Required.</span></span> <span data-ttu-id="5e47d-114">Строка, содержащая имя класса, для которого нужны экземпляры.</span><span class="sxs-lookup"><span data-stu-id="5e47d-114">String that contains the name of the class for which instances are desired.</span></span> <span data-ttu-id="5e47d-115">Этот параметр не может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="5e47d-115">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="5e47d-116">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="5e47d-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-117">Этот параметр определяет, как детализированные вызовы перечисляются и если этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="5e47d-117">This parameter determines how detailed the call enumerates and if this call returns immediately.</span></span> <span data-ttu-id="5e47d-118">Значение этого параметра по умолчанию — **вбемфлагретурниммедиатели**.</span><span class="sxs-lookup"><span data-stu-id="5e47d-118">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="5e47d-119">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="5e47d-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="5e47d-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="5e47d-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="5e47d-121">Вызывает возврат перечислителя "только вперед".</span><span class="sxs-lookup"><span data-stu-id="5e47d-121">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="5e47d-122">Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="5e47d-122">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="5e47d-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5e47d-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5e47d-124">Заставляет Инструментарий WMI хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.</span><span class="sxs-lookup"><span data-stu-id="5e47d-124">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="5e47d-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="5e47d-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="5e47d-126">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="5e47d-126">Default value for this parameter.</span></span> <span data-ttu-id="5e47d-127">Этот флаг приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="5e47d-127">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="5e47d-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5e47d-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5e47d-129">Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="5e47d-129">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="5e47d-130">Этот флаг вызывает метод в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="5e47d-130">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="5e47d-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="5e47d-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="5e47d-132">Заставляет перечисление включать только непосредственные подклассы указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="5e47d-132">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="5e47d-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5e47d-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5e47d-134">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="5e47d-134">Default value for this parameter.</span></span> <span data-ttu-id="5e47d-135">Это значение приводит к включению в перечисление всех классов в иерархии.</span><span class="sxs-lookup"><span data-stu-id="5e47d-135">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="5e47d-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="5e47d-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="5e47d-137">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="5e47d-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="5e47d-138">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="5e47d-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e47d-139">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="5e47d-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-140">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="5e47d-140">Typically, this is undefined.</span></span> <span data-ttu-id="5e47d-141">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="5e47d-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="5e47d-142">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="5e47d-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e47d-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e47d-143">Return value</span></span>

<span data-ttu-id="5e47d-144">В случае успеха метод возвращает [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="5e47d-144">If successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="5e47d-145">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5e47d-145">Error codes</span></span>

<span data-ttu-id="5e47d-146">После завершения метода **инстанцесоф** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="5e47d-146">Upon the completion of the **InstancesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="5e47d-147">Возвращенный перечислитель с нулевым числом элементов не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5e47d-147">A returned enumerator with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="5e47d-148">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="5e47d-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-149">У текущего пользователя нет разрешения на просмотр экземпляров указанного класса.</span><span class="sxs-lookup"><span data-stu-id="5e47d-149">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="5e47d-150">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5e47d-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-151">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5e47d-151">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5e47d-152">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="5e47d-152">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-153">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="5e47d-153">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5e47d-154">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5e47d-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-155">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="5e47d-155">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5e47d-156">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5e47d-156">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-157">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="5e47d-157">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e47d-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e47d-158">Remarks</span></span>

<span data-ttu-id="5e47d-159">Метод **инстанцесоф** работает только для объектов класса.</span><span class="sxs-lookup"><span data-stu-id="5e47d-159">The **InstancesOf** method only works for class objects.</span></span>

<span data-ttu-id="5e47d-160">По умолчанию Инстанцесоф выполняет глубокое извлечение.</span><span class="sxs-lookup"><span data-stu-id="5e47d-160">By default, InstancesOf performs a deep retrieval.</span></span> <span data-ttu-id="5e47d-161">То есть Инстанцесоф извлекает все экземпляры управляемого ресурса, которые вы определяете, и все экземпляры всех подклассов, определенных под целевым классом.</span><span class="sxs-lookup"><span data-stu-id="5e47d-161">That is, InstancesOf retrieves all instances of the managed resource you identify and all instances of all the subclasses defined beneath the target class.</span></span> <span data-ttu-id="5e47d-162">Например, следующий скрипт извлекает все ресурсы, которые моделируются всеми динамическими классами, определенными в \_ абстрактном классе службы CIM.</span><span class="sxs-lookup"><span data-stu-id="5e47d-162">For example, the following script retrieves all of the resources modeled by all of the dynamic classes defined beneath the CIM\_Service abstract class.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



<span data-ttu-id="5e47d-163">При выполнении этого скрипта вы получите информацию.</span><span class="sxs-lookup"><span data-stu-id="5e47d-163">If you run this script, you will get information back.</span></span> <span data-ttu-id="5e47d-164">Однако эти сведения не будут ограничены службами, установленными на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5e47d-164">However, this information will not be limited to the services installed on a computer.</span></span> <span data-ttu-id="5e47d-165">Вместо этого он будет включать сведения обо всех дочерних классах [**\_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service), включая [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) и [**Win32 \_ аппликатионсервице**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e47d-165">Instead, it will include information from all child classes of [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), including [**Win32\_SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) and [**Win32\_ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e47d-166">Требования</span><span class="sxs-lookup"><span data-stu-id="5e47d-166">Requirements</span></span>



| <span data-ttu-id="5e47d-167">Требование</span><span class="sxs-lookup"><span data-stu-id="5e47d-167">Requirement</span></span> | <span data-ttu-id="5e47d-168">Значение</span><span class="sxs-lookup"><span data-stu-id="5e47d-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e47d-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e47d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="5e47d-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e47d-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e47d-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e47d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="5e47d-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e47d-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e47d-173">Header</span><span class="sxs-lookup"><span data-stu-id="5e47d-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e47d-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e47d-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e47d-175">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5e47d-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e47d-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5e47d-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5e47d-177">DLL</span><span class="sxs-lookup"><span data-stu-id="5e47d-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e47d-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e47d-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5e47d-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="5e47d-179">CLSID</span></span><br/>                    | <span data-ttu-id="5e47d-180">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="5e47d-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="5e47d-181">IID</span><span class="sxs-lookup"><span data-stu-id="5e47d-181">IID</span></span><br/>                      | <span data-ttu-id="5e47d-182">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="5e47d-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5e47d-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e47d-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e47d-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="5e47d-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="5e47d-185">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="5e47d-185">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

