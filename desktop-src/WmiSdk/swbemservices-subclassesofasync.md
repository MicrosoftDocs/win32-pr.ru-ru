---
description: Возвращает коллекцию подклассов для указанного класса.
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: SWbemServices. Субклассесофасинк, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8d325c96ea1a292d8ac3afc76bfea619fe5a143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998857"
---
# <a name="swbemservicessubclassesofasync-method"></a><span data-ttu-id="01ca1-103">SWbemServices. Субклассесофасинк, метод</span><span class="sxs-lookup"><span data-stu-id="01ca1-103">SWbemServices.SubclassesOfAsync method</span></span>

<span data-ttu-id="01ca1-104">Метод **субклассесофасинк** объекта [**SwbemServices**](swbemservices.md) Возвращает коллекцию подклассов для указанного класса.</span><span class="sxs-lookup"><span data-stu-id="01ca1-104">The **SubclassesOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of subclasses for a specified class.</span></span> <span data-ttu-id="01ca1-105">Этот метод следует использовать только для объектов класса.</span><span class="sxs-lookup"><span data-stu-id="01ca1-105">Only use this method for class objects.</span></span>

<span data-ttu-id="01ca1-106">Этот метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="01ca1-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="01ca1-107">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="01ca1-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="01ca1-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="01ca1-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="01ca1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01ca1-109">Syntax</span></span>


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="01ca1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="01ca1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ca1-111">*обжвбемсинк*</span><span class="sxs-lookup"><span data-stu-id="01ca1-111">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="01ca1-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="01ca1-112">Required.</span></span> <span data-ttu-id="01ca1-113">Приемник объекта, который асинхронно получает подклассы.</span><span class="sxs-lookup"><span data-stu-id="01ca1-113">Object sink that receives the subclasses asynchronously.</span></span> <span data-ttu-id="01ca1-114">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="01ca1-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="01ca1-115">*стрсуперкласс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="01ca1-115">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-116">Указывает имя родительского класса.</span><span class="sxs-lookup"><span data-stu-id="01ca1-116">Specifies a parent class name.</span></span> <span data-ttu-id="01ca1-117">В перечислителе возвращаются только классы, являющиеся подклассами этого класса.</span><span class="sxs-lookup"><span data-stu-id="01ca1-117">Only the classes that are subclasses of this class are returned in the enumerator.</span></span> <span data-ttu-id="01ca1-118">Если этот параметр пуст и если *ифлагс* имеет значение **вбемкуерифлагшаллов**, возвращаются только классы верхнего уровня (то есть классы, не имеющие родительского класса).</span><span class="sxs-lookup"><span data-stu-id="01ca1-118">If this parameter is blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="01ca1-119">Если этот параметр пуст и если *ифлагс* имеет значение **вбемкуерифлагдип**, возвращаются все классы в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="01ca1-119">If this parameter is blank, and if *iFlags* is **wbemQueryFlagDeep**, all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="01ca1-120">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="01ca1-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-121">Определяет глубину перечисления вызовов.</span><span class="sxs-lookup"><span data-stu-id="01ca1-121">Determines the depth of the call enumeration.</span></span> <span data-ttu-id="01ca1-122">Значение этого параметра по умолчанию — **вбемкуерифлагдип**.</span><span class="sxs-lookup"><span data-stu-id="01ca1-122">The default value for this parameter is **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="01ca1-123">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="01ca1-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="01ca1-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="01ca1-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="01ca1-125">Заставляет перечисление включать только непосредственные подклассы указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="01ca1-125">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="01ca1-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="01ca1-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="01ca1-127">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="01ca1-127">Default for this parameter.</span></span> <span data-ttu-id="01ca1-128">Это значение приводит к принудительному перечислению для всех подклассов, которые являются производными от указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="01ca1-128">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="01ca1-129">Родительский класс не возвращается в перечислении.</span><span class="sxs-lookup"><span data-stu-id="01ca1-129">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="01ca1-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="01ca1-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="01ca1-131">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="01ca1-131">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="01ca1-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="01ca1-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="01ca1-133">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="01ca1-133">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="01ca1-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="01ca1-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="01ca1-135">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="01ca1-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="01ca1-136">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="01ca1-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="01ca1-137">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="01ca1-137">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-138">Как правило, этот параметр не определен.</span><span class="sxs-lookup"><span data-stu-id="01ca1-138">Typically, this parameter is undefined.</span></span> <span data-ttu-id="01ca1-139">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="01ca1-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="01ca1-140">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="01ca1-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="01ca1-141">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="01ca1-141">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-142">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="01ca1-142">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="01ca1-143">Этот параметр используется для выполнения нескольких асинхронных вызовов с использованием одного и того же приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="01ca1-143">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="01ca1-144">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="01ca1-144">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="01ca1-145">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="01ca1-145">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="01ca1-146">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="01ca1-146">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01ca1-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01ca1-147">Return value</span></span>

<span data-ttu-id="01ca1-148">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="01ca1-148">This method does not return a value.</span></span> <span data-ttu-id="01ca1-149">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="01ca1-149">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="01ca1-150">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="01ca1-150">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01ca1-151">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="01ca1-151">Error codes</span></span>

<span data-ttu-id="01ca1-152">После завершения метода **субклассесофасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="01ca1-152">After the completion of the **SubclassesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="01ca1-153">Возвращенная коллекция с нулевым числом элементов не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="01ca1-153">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="01ca1-154">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="01ca1-154">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-155">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="01ca1-155">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="01ca1-156">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="01ca1-156">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-157">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="01ca1-157">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="01ca1-158">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="01ca1-158">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-159">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="01ca1-159">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="01ca1-160">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="01ca1-160">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-161">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="01ca1-161">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="01ca1-162">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="01ca1-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="01ca1-163">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="01ca1-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01ca1-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01ca1-164">Remarks</span></span>

<span data-ttu-id="01ca1-165">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="01ca1-165">This call returns immediately.</span></span> <span data-ttu-id="01ca1-166">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="01ca1-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="01ca1-167">Чтобы обработать каждый объект при поступлении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="01ca1-167">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="01ca1-168">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="01ca1-168">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="01ca1-169">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="01ca1-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="01ca1-170">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="01ca1-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="01ca1-171">Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="01ca1-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01ca1-172">Требования</span><span class="sxs-lookup"><span data-stu-id="01ca1-172">Requirements</span></span>



| <span data-ttu-id="01ca1-173">Требование</span><span class="sxs-lookup"><span data-stu-id="01ca1-173">Requirement</span></span> | <span data-ttu-id="01ca1-174">Значение</span><span class="sxs-lookup"><span data-stu-id="01ca1-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01ca1-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01ca1-175">Minimum supported client</span></span><br/> | <span data-ttu-id="01ca1-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01ca1-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01ca1-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01ca1-177">Minimum supported server</span></span><br/> | <span data-ttu-id="01ca1-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01ca1-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01ca1-179">Header</span><span class="sxs-lookup"><span data-stu-id="01ca1-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="01ca1-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01ca1-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="01ca1-181">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="01ca1-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="01ca1-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01ca1-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01ca1-183">DLL</span><span class="sxs-lookup"><span data-stu-id="01ca1-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01ca1-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01ca1-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="01ca1-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="01ca1-185">CLSID</span></span><br/>                    | <span data-ttu-id="01ca1-186">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="01ca1-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="01ca1-187">IID</span><span class="sxs-lookup"><span data-stu-id="01ca1-187">IID</span></span><br/>                      | <span data-ttu-id="01ca1-188">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="01ca1-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="01ca1-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01ca1-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ca1-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="01ca1-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="01ca1-191">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="01ca1-191">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

