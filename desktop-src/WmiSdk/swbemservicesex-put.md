---
description: Возвращает объект Свбемобжектпас, содержащий путь к объекту, в который были записаны данные.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Метод Свбемсервицесекс. Where (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711618"
---
# <a name="swbemservicesexput-method"></a><span data-ttu-id="1ec1a-103">Свбемсервицесекс. размещение, метод</span><span class="sxs-lookup"><span data-stu-id="1ec1a-103">SWbemServicesEx.Put method</span></span>

<span data-ttu-id="1ec1a-104">Метод **размещения** объекта [**свбемсервицесекс**](swbemservicesex.md) сохраняет объект в пространство имен, привязанное к объекту, и возвращает объект [**свбемобжектпас**](swbemobjectpath.md) , содержащий путь к объекту, в который были записаны данные.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-104">The **Put** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves the object to the namespace bound to the object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span>

<span data-ttu-id="1ec1a-105">Этот метод вызывается в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-105">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="1ec1a-106">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1ec1a-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="1ec1a-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1ec1a-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec1a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ec1a-108">Syntax</span></span>


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1ec1a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec1a-110">*обжвбемобжект*</span><span class="sxs-lookup"><span data-stu-id="1ec1a-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec1a-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-111">Required.</span></span> <span data-ttu-id="1ec1a-112">Новый объект, помещаемый в пространство имен.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-112">The new object to be put in the namespace.</span></span> <span data-ttu-id="1ec1a-113">Это может быть только что созданный объект или измененный объект.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-113">This can be either a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-114">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="1ec1a-114">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-115">Этот параметр определяет, создает ли вызов или обновляет объект, и, если вызов возвращается немедленно.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-115">This parameter determines if the call creates or updates the object and if the call returns immediately.</span></span> <span data-ttu-id="1ec1a-116">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="1ec1a-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**вбемчанжефлагупдатекомпатибле** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-118">Позволяет обновлять класс, если нет производных классов и для этого класса нет экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-118">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="1ec1a-119">Это также позволяет обновлять во всех случаях, если изменение относится только к неважным квалификаторам (например, квалификатору **Description** ).</span><span class="sxs-lookup"><span data-stu-id="1ec1a-119">It also allows updates in all cases if the change is only to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="1ec1a-120">Это поведение по умолчанию для этого вызова и используется для совместимости с предыдущими версиями инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-120">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="1ec1a-121">Если класс имеет экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-121">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="1ec1a-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**вбемчанжефлагупдатесафемоде** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-123">Позволяет обновлять классы даже при наличии дочерних классов, если изменение не вызывает конфликтов с дочерними классами.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-123">Allows updates of classes even if there are child classes, when the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="1ec1a-124">Этот флаг можно использовать при добавлении нового свойства в базовый класс, который ранее не упоминался ни в одном из дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-124">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="1ec1a-125">Если класс имеет экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-125">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="1ec1a-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**вбемчанжефлагупдатефорцемоде** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-127">Этот флаг вызывает принудительное обновление классов при наличии конфликтующих дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-127">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="1ec1a-128">Например, этот флаг приводит к принудительному обновлению, если квалификатор класса был определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор в конфликт с существующим.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-128">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="1ec1a-129">В принудительном режиме этот конфликт разрешается путем удаления конфликтующего квалификатора в дочернем классе.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-129">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="1ec1a-130">Если класс имеет экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-130">If the class has instances, the update fails.</span></span>

<span data-ttu-id="1ec1a-131">Использование режима Force для обновления статического класса приводит к удалению всех экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-131">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="1ec1a-132">Принудительное обновление класса поставщика не удаляет экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-132">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="1ec1a-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**вбемчанжефлагкреатеорупдате** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-134">Вызывает создание класса или экземпляра, если он не существует, или перезапись, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-134">Causes the class or instance to be created if it does not exist, or overwritten if it already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="1ec1a-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**вбемчанжефлагкреатеонли** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-136">Используется только для создания.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-136">Used for creation only.</span></span> <span data-ttu-id="1ec1a-137">Вызов завершается ошибкой, если класс или экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-137">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="1ec1a-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**вбемчанжефлагупдатеонли** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-139">Вызывает выполнение этого вызова только для обновления.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-139">Causes this call to only do an update.</span></span> <span data-ttu-id="1ec1a-140">Для успешного вызова должен существовать класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-140">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="1ec1a-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**вбемфлагретурниммедиатели** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-142">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-142">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="1ec1a-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**вбемфлагретурнвхенкомплете** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-144">Вызывает блокирование этого вызова до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-144">Causes this call to block until the operation has completed.</span></span> <span data-ttu-id="1ec1a-145">Этот флаг вызывает метод в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-145">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="1ec1a-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**вбемфлагусеамендедкуалифиерс** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="1ec1a-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="1ec1a-147">Заставляет Инструментарий WMI записывать данные о поправности классов, а также определение базового класса.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-147">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="1ec1a-148">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="1ec1a-148">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1ec1a-149">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="1ec1a-149">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-150">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-150">Typically, this is undefined.</span></span> <span data-ttu-id="1ec1a-151">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-151">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="1ec1a-152">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-152">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec1a-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec1a-153">Return value</span></span>

<span data-ttu-id="1ec1a-154">Если вызов выполнен успешно, возвращается объект [**свбемобжектпас**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec1a-154">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="1ec1a-155">Этот объект содержит путь к объекту экземпляра или класса, который был успешно передан в WMI.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-155">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1ec1a-156">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1ec1a-156">Error codes</span></span>

<span data-ttu-id="1ec1a-157">После завершения метода **размещения** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-157">After the completion of the **Put** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="1ec1a-158">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-159">У текущего пользователя нет разрешения на операцию.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-159">Current user does not have the permission for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-160">**вбемерралреадексистс** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-160">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-161">Был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-161">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-162">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-163">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-164">**вбемерриллегалнулл** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-164">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-165">Для свойства, которое не может быть **равно NULL**, указано значение **null** .</span><span class="sxs-lookup"><span data-stu-id="1ec1a-165">A value of **NULL** was specified for a property that cannot be **NULL**.</span></span> <span data-ttu-id="1ec1a-166">Примером такого свойства является один, помеченный квалификатором [**Key**](standard-qualifiers.md), **индексированного** или **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="1ec1a-166">An example of such a property is one marked by a [**Key**](standard-qualifiers.md), **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-167">**вбемерринвалидобжект** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-167">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-168">Указан недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-168">The specified object is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-169">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-170">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-170">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-171">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-171">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-172">Был указан флаг **вбемчанжефлагупдатеонли** , но экземпляр или класс не существует.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-172">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-173">**вбемерринкомплетекласс** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-173">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-174">Обязательные свойства для классов не заданы.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-174">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="1ec1a-175">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="1ec1a-175">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="1ec1a-176">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="1ec1a-176">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ec1a-177">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec1a-177">Requirements</span></span>



| <span data-ttu-id="1ec1a-178">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec1a-178">Requirement</span></span> | <span data-ttu-id="1ec1a-179">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec1a-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec1a-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ec1a-180">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec1a-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ec1a-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1ec1a-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ec1a-182">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec1a-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ec1a-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ec1a-184">Header</span><span class="sxs-lookup"><span data-stu-id="1ec1a-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec1a-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec1a-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ec1a-186">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1ec1a-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="1ec1a-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1ec1a-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1ec1a-188">DLL</span><span class="sxs-lookup"><span data-stu-id="1ec1a-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ec1a-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ec1a-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1ec1a-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="1ec1a-190">CLSID</span></span><br/>                    | <span data-ttu-id="1ec1a-191">\_ИСВБЕМСЕРВИЦЕСЕКС CLSID</span><span class="sxs-lookup"><span data-stu-id="1ec1a-191">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="1ec1a-192">IID</span><span class="sxs-lookup"><span data-stu-id="1ec1a-192">IID</span></span><br/>                      | <span data-ttu-id="1ec1a-193">IID \_ исвбемсервицесекс</span><span class="sxs-lookup"><span data-stu-id="1ec1a-193">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

 




