---
description: Метод размещения \_ SWbemObject создает или обновляет экземпляр или объект класса для Инструментарий управления Windows (WMI) (WMI). Этот метод можно использовать после изменения любых свойств или методов в SWbemObject, и ваши изменения записываются в WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: Метод SWbemObject.Put_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711643"
---
# <a name="swbemobjectput_-method"></a><span data-ttu-id="eb193-104">SWbemObject. размещение, \_ метод</span><span class="sxs-lookup"><span data-stu-id="eb193-104">SWbemObject.Put\_ method</span></span>

<span data-ttu-id="eb193-105">Метод **размещения \_** [**SWbemObject**](swbemobject.md) создает или обновляет экземпляр или объект класса для Инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="eb193-105">The **Put\_** method of [**SWbemObject**](swbemobject.md) creates or updates an instance or a class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="eb193-106">Этот метод можно использовать после изменения любых свойств или методов в **SWbemObject**, и ваши изменения записываются в WMI.</span><span class="sxs-lookup"><span data-stu-id="eb193-106">You can use this method after you modify any properties or methods in an **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="eb193-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eb193-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb193-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb193-108">Syntax</span></span>


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eb193-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb193-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb193-110">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eb193-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb193-111">Этот параметр определяет, создает ли вызов или обновляет класс или экземпляр, и, если вызов возвращается немедленно.</span><span class="sxs-lookup"><span data-stu-id="eb193-111">This parameter determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="eb193-112">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="eb193-112">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="eb193-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>Вбемчанжефлагупдатекомпатибле \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="eb193-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-114">Позволяет обновлять класс, если нет производных классов и для этого класса нет экземпляров.</span><span class="sxs-lookup"><span data-stu-id="eb193-114">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="eb193-115">Это также позволяет обновлять во всех случаях, если изменение относится только к неважным квалификаторам (например, квалификатору **Description** ).</span><span class="sxs-lookup"><span data-stu-id="eb193-115">It also allows updates in all cases if the change is just to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="eb193-116">Это поведение по умолчанию для этого вызова и используется для совместимости с предыдущими версиями инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="eb193-116">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="eb193-117">Если в классе есть экземпляры, происходит сбой обновления.</span><span class="sxs-lookup"><span data-stu-id="eb193-117">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="eb193-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>Вбемчанжефлагупдатесафемоде \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="eb193-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-119">Позволяет обновлять классы даже при наличии дочерних классов, если изменение не вызывает конфликтов с дочерними классами.</span><span class="sxs-lookup"><span data-stu-id="eb193-119">Allows updates of classes even if there are child classes if the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="eb193-120">Этот флаг можно использовать при добавлении нового свойства в базовый класс, который ранее не упоминался ни в одном из дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="eb193-120">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="eb193-121">Если в классе есть экземпляры, происходит сбой обновления.</span><span class="sxs-lookup"><span data-stu-id="eb193-121">If the class has instances the update fails.</span></span> <span data-ttu-id="eb193-122">Если в классе есть экземпляры, происходит сбой обновления.</span><span class="sxs-lookup"><span data-stu-id="eb193-122">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="eb193-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>Вбемчанжефлагупдатефорцемоде \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="eb193-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-124">Этот флаг вызывает принудительное обновление классов при наличии конфликтующих дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="eb193-124">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="eb193-125">Например, этот флаг принудительно вызовет обновление, если квалификатор класса был определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор и в конфликт с существующим.</span><span class="sxs-lookup"><span data-stu-id="eb193-125">For example, this flag will force an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier and in conflict with the existing one.</span></span> <span data-ttu-id="eb193-126">В принудительном режиме этот конфликт можно устранить, удалив конфликтующий квалификатор в дочернем классе.</span><span class="sxs-lookup"><span data-stu-id="eb193-126">In force mode this conflict would be resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="eb193-127">Если у класса есть экземпляры, обновление завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb193-127">If the class has instances the update will fail.</span></span>

<span data-ttu-id="eb193-128">Использование принудительного режима для обновления статического класса приводит к удалению всех экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="eb193-128">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="eb193-129">Принудительное обновление класса поставщика не удаляет экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="eb193-129">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="eb193-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>Вбемчанжефлагкреатеорупдате \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="eb193-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-131">Вызывает создание класса или экземпляра, если он не существует или перезаписан, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="eb193-131">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="eb193-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>Вбемчанжефлагкреатеонли \* \* \* \* (0x2)</span><span class="sxs-lookup"><span data-stu-id="eb193-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-133">Используется только для создания.</span><span class="sxs-lookup"><span data-stu-id="eb193-133">Used for creation only.</span></span> <span data-ttu-id="eb193-134">Вызов завершается ошибкой, если класс или экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="eb193-134">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="eb193-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>Вбемчанжефлагупдатеонли \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="eb193-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-136">Приводит к обновлению этого вызова.</span><span class="sxs-lookup"><span data-stu-id="eb193-136">Causes this call to update.</span></span> <span data-ttu-id="eb193-137">Для успешного вызова должен существовать класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="eb193-137">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="eb193-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="eb193-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-139">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="eb193-139">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="eb193-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="eb193-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-141">Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="eb193-141">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="eb193-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="eb193-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="eb193-143">Заставляет Инструментарий WMI записывать данные о поправности классов, а также определение базового класса.</span><span class="sxs-lookup"><span data-stu-id="eb193-143">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="eb193-144">Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="eb193-144">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb193-145">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eb193-145">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb193-146">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="eb193-146">Typically, this is undefined.</span></span> <span data-ttu-id="eb193-147">В противном случае это объект [**свбемобжектпас**](swbemobjectpath.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="eb193-147">Otherwise, this is an [**SWbemObjectPath**](swbemobjectpath.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="eb193-148">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="eb193-148">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb193-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb193-149">Return value</span></span>

<span data-ttu-id="eb193-150">Если вызов выполнен успешно, возвращается объект [**свбемобжектпас**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="eb193-150">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="eb193-151">Этот объект содержит путь к объекту экземпляра или класса, который был успешно передан в WMI.</span><span class="sxs-lookup"><span data-stu-id="eb193-151">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb193-152">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="eb193-152">Error codes</span></span>

<span data-ttu-id="eb193-153">После завершения метода **размещения \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="eb193-153">After the completion of the **Put\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="eb193-154">**вбемерракцессдениед** -2147749891</span><span class="sxs-lookup"><span data-stu-id="eb193-154">**wbemErrAccessDenied** - 2147749891</span></span>
</dt> <dd>

<span data-ttu-id="eb193-155">У текущего пользователя нет разрешения на обновление экземпляра указанного класса.</span><span class="sxs-lookup"><span data-stu-id="eb193-155">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="eb193-156">**вбемерралреадексистс** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="eb193-156">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="eb193-157">Был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="eb193-157">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="eb193-158">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="eb193-158">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eb193-159">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="eb193-159">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="eb193-160">**вбемерриллегалнулл** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="eb193-160">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="eb193-161">Для свойства, которое не может быть **Nothing**, указано значение **Nothing** .</span><span class="sxs-lookup"><span data-stu-id="eb193-161">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="eb193-162">Примером такого свойства является один, помеченный квалификатором **Key,** **индексированного** или **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="eb193-162">An example of such a property is one marked by a **Key,** **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="eb193-163">**вбемерринвалидобжект** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="eb193-163">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="eb193-164">Задан недопустимый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="eb193-164">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb193-165">**вбемерринвалидпараметер** — 0x80041008</span><span class="sxs-lookup"><span data-stu-id="eb193-165">**wbemErrInvalidParameter** - 0x80041008</span></span>
</dt> <dd>

<span data-ttu-id="eb193-166">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="eb193-166">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb193-167">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="eb193-167">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="eb193-168">Был указан флаг **вбемчанжефлагупдатеонли** , но экземпляр или класс не существует.</span><span class="sxs-lookup"><span data-stu-id="eb193-168">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="eb193-169">**вбемерринкомплетекласс** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="eb193-169">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="eb193-170">Обязательные свойства для классов не заданы.</span><span class="sxs-lookup"><span data-stu-id="eb193-170">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="eb193-171">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="eb193-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eb193-172">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="eb193-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb193-173">Требования</span><span class="sxs-lookup"><span data-stu-id="eb193-173">Requirements</span></span>



| <span data-ttu-id="eb193-174">Требование</span><span class="sxs-lookup"><span data-stu-id="eb193-174">Requirement</span></span> | <span data-ttu-id="eb193-175">Значение</span><span class="sxs-lookup"><span data-stu-id="eb193-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb193-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb193-176">Minimum supported client</span></span><br/> | <span data-ttu-id="eb193-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb193-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb193-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb193-178">Minimum supported server</span></span><br/> | <span data-ttu-id="eb193-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb193-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb193-180">Header</span><span class="sxs-lookup"><span data-stu-id="eb193-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb193-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb193-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb193-182">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eb193-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb193-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb193-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb193-184">DLL</span><span class="sxs-lookup"><span data-stu-id="eb193-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb193-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb193-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb193-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="eb193-186">CLSID</span></span><br/>                    | <span data-ttu-id="eb193-187">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="eb193-187">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="eb193-188">IID</span><span class="sxs-lookup"><span data-stu-id="eb193-188">IID</span></span><br/>                      | <span data-ttu-id="eb193-189">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="eb193-189">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="eb193-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb193-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb193-191">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="eb193-191">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="eb193-192">**Свбемобжектпас. класс**</span><span class="sxs-lookup"><span data-stu-id="eb193-192">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="eb193-193">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="eb193-193">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="eb193-194">**свбемкуалифиер**</span><span class="sxs-lookup"><span data-stu-id="eb193-194">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

