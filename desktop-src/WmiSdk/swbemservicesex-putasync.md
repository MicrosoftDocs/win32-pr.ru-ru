---
description: Асинхронно сохраняет объект в пространстве имен. При успешном выполнении этот метод отправляет oncompleteное событие в объект Свбемсинк, указанный в качестве входного параметра.
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: Свбемсервицесекс. Путасинк, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081112"
---
# <a name="swbemservicesexputasync-method"></a><span data-ttu-id="b5cfb-104">Свбемсервицесекс. Путасинк, метод</span><span class="sxs-lookup"><span data-stu-id="b5cfb-104">SWbemServicesEx.PutAsync method</span></span>

<span data-ttu-id="b5cfb-105">Метод **путасинк** объекта [**свбемсервицесекс**](swbemservicesex.md) асинхронно сохраняет объект в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-105">The **PutAsync** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves an object asynchronously to a namespace.</span></span> <span data-ttu-id="b5cfb-106">При успешном выполнении этот метод отправляет [**Oncompleteное**](swbemsink-oncompleted.md) событие в объект [**свбемсинк**](swbemsink.md) , указанный в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-106">When successful, this method sends an [**OnCompleted**](swbemsink-oncompleted.md) event to the [**SWbemSink**](swbemsink.md) object that is specified as an input parameter.</span></span>

<span data-ttu-id="b5cfb-107">Этот метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-107">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="b5cfb-108">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b5cfb-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b5cfb-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b5cfb-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cfb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5cfb-110">Syntax</span></span>


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b5cfb-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5cfb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cfb-112">*обжвбемсинк*</span><span class="sxs-lookup"><span data-stu-id="b5cfb-112">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="b5cfb-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-113">Required.</span></span> <span data-ttu-id="b5cfb-114">Приемник объекта, который асинхронно получает объекты.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-114">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="b5cfb-115">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-115">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-116">*ожбвбемобжект*</span><span class="sxs-lookup"><span data-stu-id="b5cfb-116">*ojbWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="b5cfb-117">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-117">Required.</span></span> <span data-ttu-id="b5cfb-118">Новый объект, помещаемый в пространство имен.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-118">The new object to be put in the namespace.</span></span> <span data-ttu-id="b5cfb-119">Это может быть только что созданный объект или измененный объект.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-119">This may be a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-120">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b5cfb-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-121">Этот параметр определяет, создает ли вызов или обновляет объект, и происходит ли немедленное возвращение вызова.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-121">This parameter determines whether the call creates or updates the object and whether the call returns immediately.</span></span> <span data-ttu-id="b5cfb-122">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="b5cfb-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**вбемчанжефлагупдатекомпатибле** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-124">Позволяет обновлять класс при отсутствии производных классов и экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-124">Allows a class to be updated when there are no derived classes and no instances for the class.</span></span> <span data-ttu-id="b5cfb-125">Это также позволяет обновлять во всех случаях, когда изменение выполняется только для неважных квалификаторов, например квалификатор **описания** .</span><span class="sxs-lookup"><span data-stu-id="b5cfb-125">It also allows updates in all cases when the change is only to unimportant qualifiers, for example, the **Description** qualifier.</span></span> <span data-ttu-id="b5cfb-126">Это поведение по умолчанию для этого вызова и используется для совместимости с предыдущими версиями инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-126">This is the default behavior for this call, and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="b5cfb-127">Если класс имеет экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-127">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="b5cfb-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**вбемчанжефлагупдатесафемоде** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-129">Позволяет обновлять классы даже при наличии дочерних классов, а изменение не вызывает конфликтов с дочерними классами.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-129">Allows updates of classes even when there are child classes and the change does not cause conflicts with the child classes.</span></span> <span data-ttu-id="b5cfb-130">Используйте этот флаг при добавлении нового свойства в базовый класс, который не упоминался ранее в каких-либо дочерних классах.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-130">Use this flag when adding a new property to a base class that is not mentioned previously in any of the child classes.</span></span> <span data-ttu-id="b5cfb-131">Если класс имеет экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-131">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="b5cfb-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**вбемчанжефлагупдатефорцемоде** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-133">Этот флаг вызывает принудительное обновление классов при наличии конфликтующих дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-133">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="b5cfb-134">Например, этот флаг принудительно выполняет обновление, если квалификатор класса определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор в конфликт с существующим.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-134">For example, this flag forces an update when a class qualifier is defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="b5cfb-135">В принудительном режиме этот конфликт разрешается путем удаления конфликтующего квалификатора в дочернем классе.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-135">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="b5cfb-136">Если класс имеет экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-136">If the class has instances, the update fails.</span></span>

<span data-ttu-id="b5cfb-137">Использование режима Force для обновления статического класса приводит к удалению всех экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-137">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="b5cfb-138">Принудительное обновление класса поставщика не удаляет экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-138">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="b5cfb-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**вбемчанжефлагкреатеорупдате** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-140">Вызывает создание класса или экземпляра, если он не существует, или перезапись, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-140">Causes the class or instance to be created if it does not exist, or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="b5cfb-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**вбемчанжефлагкреатеонли** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-142">Используется только для создания.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-142">Used for creation only.</span></span> <span data-ttu-id="b5cfb-143">Вызов завершается ошибкой, если класс или экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-143">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="b5cfb-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**вбемчанжефлагупдатеонли** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-145">Приводит к обновлению этого вызова.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-145">Causes this call to update.</span></span> <span data-ttu-id="b5cfb-146">Для успешного вызова должен существовать класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-146">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="b5cfb-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**вбемфлагретурниммедиатели** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-148">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-148">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="b5cfb-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**вбемфлагретурнвхенкомплете** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-150">Вызывает блокирование этого вызова до завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-150">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="b5cfb-151">Этот флаг вызывает метод в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-151">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b5cfb-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**вбемфлагусеамендедкуалифиерс** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b5cfb-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b5cfb-153">Заставляет Инструментарий WMI записывать данные о поправности классов и определение базового класса.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-153">Causes WMI to write class amendment data and the base class definition.</span></span> <span data-ttu-id="b5cfb-154">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b5cfb-154">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b5cfb-155">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b5cfb-155">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-156">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-156">Typically, this is undefined.</span></span> <span data-ttu-id="b5cfb-157">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-157">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="b5cfb-158">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-158">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-159">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b5cfb-159">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-160">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-160">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b5cfb-161">Этот параметр используется для выполнения нескольких асинхронных вызовов с использованием одного и того же приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-161">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b5cfb-162">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-162">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b5cfb-163">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b5cfb-163">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b5cfb-164">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b5cfb-164">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cfb-165">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5cfb-165">Return value</span></span>

<span data-ttu-id="b5cfb-166">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-166">This method does not return a value.</span></span> <span data-ttu-id="b5cfb-167">Если вызов выполнен успешно, событие [**онобжектпут**](swbemsink-onobjectput.md) переданного приемника объекта получает объект [**свбемобжектпас**](swbemobjectpath.md) , который содержит путь к объекту экземпляра или класса, который успешно зафиксирован в WMI.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-167">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, which contains the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5cfb-168">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b5cfb-168">Error codes</span></span>

<span data-ttu-id="b5cfb-169">После завершения метода **путасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-169">After the completion of the **PutAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b5cfb-170">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-171">У текущего пользователя нет разрешения на обновление экземпляра указанного класса.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-171">Current user does not have the permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-172">**вбемерралреадексистс** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-172">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-173">Был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-173">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-174">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-174">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-175">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-175">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-176">**вбемерриллегалнулл** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-176">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-177">Для свойства, которое не может быть равно null, указано значение null.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-177">A value of Null was specified for a property that cannot be Null.</span></span> <span data-ttu-id="b5cfb-178">Примером такого свойства является один, помеченный квалификатором **Key**, **индексированного** или **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="b5cfb-178">An example of such a property is one marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-179">**вбемерринвалидобжект** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-179">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-180">Задан недопустимый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-180">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-181">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-181">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-182">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-182">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-183">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-183">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-184">Был указан флаг **вбемчанжефлагупдатеонли** , но экземпляр или класс не существует.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-184">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-185">**вбемерринкомплетекласс** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-185">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-186">Обязательные свойства для классов не заданы.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-186">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfb-187">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b5cfb-187">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b5cfb-188">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-188">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5cfb-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5cfb-189">Remarks</span></span>

<span data-ttu-id="b5cfb-190">Этот вызов возвращает немедленно, а результаты и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-190">This call returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b5cfb-191">Чтобы обрабатывал каждый объект при поступлении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="b5cfb-191">To handle each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="b5cfb-192">Любая обработка, выполненная после прибытия всех объектов, выполняется в подподпрограмме для *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b5cfb-192">Any processing done after all the objects arrive is done in a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="b5cfb-193">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-193">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b5cfb-194">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="b5cfb-194">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b5cfb-195">Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="b5cfb-195">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cfb-196">Требования</span><span class="sxs-lookup"><span data-stu-id="b5cfb-196">Requirements</span></span>



| <span data-ttu-id="b5cfb-197">Требование</span><span class="sxs-lookup"><span data-stu-id="b5cfb-197">Requirement</span></span> | <span data-ttu-id="b5cfb-198">Значение</span><span class="sxs-lookup"><span data-stu-id="b5cfb-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cfb-199">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5cfb-199">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cfb-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5cfb-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5cfb-201">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5cfb-201">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cfb-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5cfb-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5cfb-203">Header</span><span class="sxs-lookup"><span data-stu-id="b5cfb-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5cfb-204"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5cfb-204"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5cfb-205">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b5cfb-205">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5cfb-206"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5cfb-206"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5cfb-207">DLL</span><span class="sxs-lookup"><span data-stu-id="b5cfb-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5cfb-208"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5cfb-208"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5cfb-209">CLSID</span><span class="sxs-lookup"><span data-stu-id="b5cfb-209">CLSID</span></span><br/>                    | <span data-ttu-id="b5cfb-210">\_ИСВБЕМСЕРВИЦЕСЕКС CLSID</span><span class="sxs-lookup"><span data-stu-id="b5cfb-210">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="b5cfb-211">IID</span><span class="sxs-lookup"><span data-stu-id="b5cfb-211">IID</span></span><br/>                      | <span data-ttu-id="b5cfb-212">IID \_ исвбемсервицесекс</span><span class="sxs-lookup"><span data-stu-id="b5cfb-212">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

