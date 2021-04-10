---
description: Метод Путасинк \_ объекта SWbemObject асинхронно создает или обновляет объект экземпляра или класса для Инструментарий управления Windows (WMI) (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: Метод SWbemObject.PutAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272568"
---
# <a name="swbemobjectputasync_-method"></a><span data-ttu-id="b933e-103">SWbemObject. Путасинк, \_ метод</span><span class="sxs-lookup"><span data-stu-id="b933e-103">SWbemObject.PutAsync\_ method</span></span>

<span data-ttu-id="b933e-104">Метод **путасинк \_** объекта [**SWbemObject**](swbemobject.md) асинхронно создает или обновляет объект экземпляра или класса для Инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b933e-104">The **PutAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="b933e-105">Этот метод можно использовать после изменения любых свойств или методов в **SWbemObject**, и ваши изменения записываются в WMI.</span><span class="sxs-lookup"><span data-stu-id="b933e-105">You can use this method after you modify any properties or methods in **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="b933e-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b933e-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b933e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b933e-107">Syntax</span></span>


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b933e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b933e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b933e-109">*обжвбемсинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b933e-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b933e-110">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b933e-110">Required.</span></span> <span data-ttu-id="b933e-111">Приемник объекта, который асинхронно получает результат операции **размещения** .</span><span class="sxs-lookup"><span data-stu-id="b933e-111">Object sink that asynchronously receives the result of the **put** operation.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-112">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b933e-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b933e-113">Определяет, создает ли вызов или обновляет класс или экземпляр, и, если вызов возвращается немедленно.</span><span class="sxs-lookup"><span data-stu-id="b933e-113">Determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="b933e-114">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b933e-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="b933e-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>Вбемчанжефлагупдатекомпатибле \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b933e-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-116">Позволяет обновлять класс, если нет производных классов и для этого класса нет экземпляров.</span><span class="sxs-lookup"><span data-stu-id="b933e-116">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="b933e-117">Это также позволяет обновлять во всех случаях, если изменение относится только к неважным квалификаторам (например, квалификатору **Description** ).</span><span class="sxs-lookup"><span data-stu-id="b933e-117">It also allows updates in all cases if the change is just to unimportant qualifiers (for example the **Description** qualifier).</span></span> <span data-ttu-id="b933e-118">Это поведение по умолчанию для этого вызова и используется для совместимости с предыдущими версиями инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="b933e-118">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="b933e-119">Если в классе есть экземпляры, происходит сбой обновления.</span><span class="sxs-lookup"><span data-stu-id="b933e-119">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="b933e-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>Вбемчанжефлагупдатесафемоде \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="b933e-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-121">Позволяет обновлять классы даже при наличии дочерних классов, если изменение не вызывает конфликтов с дочерними классами.</span><span class="sxs-lookup"><span data-stu-id="b933e-121">Allows updates of classes, even if there are child classes, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="b933e-122">Этот флаг можно использовать при добавлении нового свойства в базовый класс, который ранее не упоминался ни в одном из дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="b933e-122">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="b933e-123">Если в классе есть экземпляры, происходит сбой обновления.</span><span class="sxs-lookup"><span data-stu-id="b933e-123">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="b933e-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>Вбемчанжефлагупдатефорцемоде \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="b933e-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-125">Принудительно обновляет классы при наличии конфликтующих дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="b933e-125">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="b933e-126">Например, этот флаг приводит к принудительному обновлению, если квалификатор класса был определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор в конфликт с существующим.</span><span class="sxs-lookup"><span data-stu-id="b933e-126">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class attempts to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="b933e-127">В принудительном режиме этот конфликт разрешается путем удаления конфликтующего квалификатора в дочернем классе.</span><span class="sxs-lookup"><span data-stu-id="b933e-127">In force mode this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="b933e-128">Если в классе есть экземпляры, происходит сбой обновления.</span><span class="sxs-lookup"><span data-stu-id="b933e-128">If the class has instances the update fails.</span></span>

<span data-ttu-id="b933e-129">Использование принудительного режима для обновления статического класса приводит к удалению всех экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="b933e-129">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="b933e-130">Принудительное обновление класса поставщика не удаляет экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="b933e-130">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="b933e-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>Вбемчанжефлагкреатеорупдате \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b933e-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-132">Вызывает создание класса или экземпляра, если он не существует или перезаписан, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="b933e-132">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="b933e-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>Вбемчанжефлагкреатеонли \* \* \* \* (0x2)</span><span class="sxs-lookup"><span data-stu-id="b933e-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-134">Используется только для создания.</span><span class="sxs-lookup"><span data-stu-id="b933e-134">Used for creation only.</span></span> <span data-ttu-id="b933e-135">Вызов завершается ошибкой, если класс или экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="b933e-135">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="b933e-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>Вбемчанжефлагупдатеонли \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b933e-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-137">Приводит к обновлению этого вызова.</span><span class="sxs-lookup"><span data-stu-id="b933e-137">Causes this call to update.</span></span> <span data-ttu-id="b933e-138">Для успешного вызова должен существовать класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b933e-138">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="b933e-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="b933e-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-140">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="b933e-140">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="b933e-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b933e-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-142">Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="b933e-142">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b933e-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b933e-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-144">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="b933e-144">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b933e-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b933e-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-146">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="b933e-146">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b933e-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b933e-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b933e-148">Заставляет Инструментарий WMI записывать данные о поправности классов вместе с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="b933e-148">Causes WMI to write class amendment data along with the base class definition.</span></span> <span data-ttu-id="b933e-149">Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b933e-149">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b933e-150">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b933e-150">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b933e-151">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="b933e-151">Typically, this is undefined.</span></span> <span data-ttu-id="b933e-152">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="b933e-152">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b933e-153">Поставщик, который поддерживает или требует эту информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="b933e-153">A provider that supports or requires this information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-154">*обжвбемасинкконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b933e-154">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b933e-155">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="b933e-155">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b933e-156">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="b933e-156">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b933e-157">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="b933e-157">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b933e-158">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b933e-158">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b933e-159">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b933e-159">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b933e-160">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b933e-160">Return value</span></span>

<span data-ttu-id="b933e-161">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b933e-161">This method does not return a value.</span></span> <span data-ttu-id="b933e-162">Если вызов выполнен успешно, событие [**онобжектпут**](swbemsink-onobjectput.md) переданного приемника объекта получает объект [**свбемобжектпас**](swbemobjectpath.md) , содержащий путь к объекту экземпляра или класса, который успешно зафиксирован в WMI.</span><span class="sxs-lookup"><span data-stu-id="b933e-162">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, containing the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b933e-163">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b933e-163">Error codes</span></span>

<span data-ttu-id="b933e-164">После завершения метода **путасинк \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="b933e-164">After the completion of the **PutAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b933e-165">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b933e-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-166">У текущего пользователя нет разрешения на обновление экземпляра указанного класса.</span><span class="sxs-lookup"><span data-stu-id="b933e-166">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-167">**вбемерралреадексистс** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="b933e-167">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-168">Был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="b933e-168">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-169">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b933e-169">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-170">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b933e-170">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-171">**вбемерриллегалнулл** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="b933e-171">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-172">Для свойства, которое не может быть **Nothing**, указано значение **Nothing** .</span><span class="sxs-lookup"><span data-stu-id="b933e-172">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="b933e-173">Примером такого свойства является атрибут, помеченный квалификатором **Key**, **индексированного** или **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="b933e-173">An example of such a property is one that is marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-174">**вбемерринвалидобжект** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="b933e-174">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-175">Задан недопустимый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b933e-175">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-176">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b933e-176">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-177">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="b933e-177">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-178">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="b933e-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-179">Был указан флаг **вбемчанжефлагупдатеонли** , но экземпляр или класс не существует.</span><span class="sxs-lookup"><span data-stu-id="b933e-179">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-180">**вбемерринкомплетекласс** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="b933e-180">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-181">Обязательные свойства для классов не заданы.</span><span class="sxs-lookup"><span data-stu-id="b933e-181">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="b933e-182">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b933e-182">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b933e-183">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b933e-183">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b933e-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b933e-184">Remarks</span></span>

<span data-ttu-id="b933e-185">Этот вызов возвращает немедленно, и результат операции **размещения** возвращается вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="b933e-185">This call returns immediately, and the result of the **put** operation is returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b933e-186">Реализуйте *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="b933e-186">Implement the *objWbemSink*.</span></span> <span data-ttu-id="b933e-187">Метод [**онобжектпут**](swbemsink-onobjectput.md) для получения пути к объекту экземпляра или класса, который записывается в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="b933e-187">[**OnObjectPut**](swbemsink-onobjectput.md) method to obtain the object path of the instance or class that is written to the WMI repository.</span></span> <span data-ttu-id="b933e-188">Дополнительные сведения о методах приемника см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b933e-188">For more information about sink methods, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b933e-189">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="b933e-189">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b933e-190">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="b933e-190">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b933e-191">Чтобы устранить риски, используйте семисинчронаус или синхронный обмен данными.</span><span class="sxs-lookup"><span data-stu-id="b933e-191">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="b933e-192">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b933e-192">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b933e-193">Требования</span><span class="sxs-lookup"><span data-stu-id="b933e-193">Requirements</span></span>



| <span data-ttu-id="b933e-194">Требование</span><span class="sxs-lookup"><span data-stu-id="b933e-194">Requirement</span></span> | <span data-ttu-id="b933e-195">Значение</span><span class="sxs-lookup"><span data-stu-id="b933e-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b933e-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b933e-196">Minimum supported client</span></span><br/> | <span data-ttu-id="b933e-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b933e-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b933e-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b933e-198">Minimum supported server</span></span><br/> | <span data-ttu-id="b933e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b933e-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b933e-200">Header</span><span class="sxs-lookup"><span data-stu-id="b933e-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="b933e-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b933e-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b933e-202">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b933e-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="b933e-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b933e-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b933e-204">DLL</span><span class="sxs-lookup"><span data-stu-id="b933e-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b933e-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b933e-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b933e-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="b933e-206">CLSID</span></span><br/>                    | <span data-ttu-id="b933e-207">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="b933e-207">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b933e-208">IID</span><span class="sxs-lookup"><span data-stu-id="b933e-208">IID</span></span><br/>                      | <span data-ttu-id="b933e-209">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="b933e-209">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="b933e-210">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b933e-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b933e-211">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="b933e-211">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="b933e-212">**Свбемобжектпас. класс**</span><span class="sxs-lookup"><span data-stu-id="b933e-212">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="b933e-213">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="b933e-213">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="b933e-214">**свбемкуалифиер**</span><span class="sxs-lookup"><span data-stu-id="b933e-214">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

