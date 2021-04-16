---
description: '\_Класс ошибок CIM содержит сведения о сбое операции CIM.'
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: Класс CIM_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59ae2527478235c14a8f856319178afe00c02a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342645"
---
# <a name="cim_error-class"></a><span data-ttu-id="55251-103">\_Класс ошибок CIM</span><span class="sxs-lookup"><span data-stu-id="55251-103">CIM\_Error class</span></span>

<span data-ttu-id="55251-104">Класс **\_ ошибок CIM** содержит сведения о сбое операции CIM.</span><span class="sxs-lookup"><span data-stu-id="55251-104">The **CIM\_Error** class contains information about the failure of a CIM operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="55251-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55251-105">Syntax</span></span>

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a><span data-ttu-id="55251-106">Члены</span><span class="sxs-lookup"><span data-stu-id="55251-106">Members</span></span>

<span data-ttu-id="55251-107">Класс **\_ ошибок CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="55251-107">The **CIM\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="55251-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="55251-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55251-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="55251-109">Properties</span></span>

<span data-ttu-id="55251-110">Класс **\_ ошибок CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="55251-110">The **CIM\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55251-111">**Цимстатускоде**</span><span class="sxs-lookup"><span data-stu-id="55251-111">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-112">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55251-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55251-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-114">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. \|Ошибка DMTF. КОД \| 2,3 "," DSP0200. DMTF \| Цимеррор \| 1,3 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Цимстатускодедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="55251-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.CODE\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCodeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-115">Код состояния CIM, характеризующий этот экземпляр.</span><span class="sxs-lookup"><span data-stu-id="55251-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="55251-116">Это свойство определяет коды состояния, которые могут возвращаться сервером CIM или прослушивателем.</span><span class="sxs-lookup"><span data-stu-id="55251-116">This property defines the status codes that can be return by a CIM server or listener.</span></span>

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span data-ttu-id="55251-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**Модель CIM \_ \_Ошибка Err** (1)</span><span class="sxs-lookup"><span data-stu-id="55251-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM\_ERR\_FAILED** (1)</span></span>


</dt> <dd>

<span data-ttu-id="55251-118">Произошла общая ошибка, которая не охватывает более конкретный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="55251-118">A general error occurred that is not covered by a more specific error code.</span></span>

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span data-ttu-id="55251-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**Модель CIM \_ Ошибка \_ \_ отказа в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="55251-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM\_ERR\_ACCESS\_DENIED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="55251-120">Доступ к ресурсу CIM недоступен для клиента.</span><span class="sxs-lookup"><span data-stu-id="55251-120">Access to a CIM resource was not available to the client.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span data-ttu-id="55251-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**Модель CIM \_ ERR- \_ недопустимое \_ пространство имен** (3)</span><span class="sxs-lookup"><span data-stu-id="55251-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM\_ERR\_INVALID\_NAMESPACE** (3)</span></span>


</dt> <dd>

<span data-ttu-id="55251-122">Целевое пространство имен не существует.</span><span class="sxs-lookup"><span data-stu-id="55251-122">The target namespace does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span data-ttu-id="55251-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**Модель CIM \_ ERR- \_ Недопустимый \_ параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="55251-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM\_ERR\_INVALID\_PARAMETER** (4)</span></span>


</dt> <dd>

<span data-ttu-id="55251-124">Одно или несколько значений параметров, переданных в метод, недопустимы.</span><span class="sxs-lookup"><span data-stu-id="55251-124">One or more parameter values passed to the method were invalid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span data-ttu-id="55251-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**Модель CIM \_ ERR- \_ Недопустимый \_ класс** (5)</span><span class="sxs-lookup"><span data-stu-id="55251-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM\_ERR\_INVALID\_CLASS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="55251-126">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="55251-126">The specified Class does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span data-ttu-id="55251-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**Модель CIM \_ Ошибка \_ не \_ найдена** (6)</span><span class="sxs-lookup"><span data-stu-id="55251-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM\_ERR\_NOT\_FOUND** (6)</span></span>


</dt> <dd>

<span data-ttu-id="55251-128">Не удалось найти запрошенный объект.</span><span class="sxs-lookup"><span data-stu-id="55251-128">The requested object could not be found.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span data-ttu-id="55251-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**Модель CIM \_ ERR \_ не \_ поддерживается** (7)</span><span class="sxs-lookup"><span data-stu-id="55251-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM\_ERR\_NOT\_SUPPORTED** (7)</span></span>


</dt> <dd>

<span data-ttu-id="55251-130">Запрошенная операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="55251-130">The requested operation is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span data-ttu-id="55251-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**Модель CIM \_ \_Класс Err \_ имеет \_ дочерние элементы** (8)</span><span class="sxs-lookup"><span data-stu-id="55251-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM\_ERR\_CLASS\_HAS\_CHILDREN** (8)</span></span>


</dt> <dd>

<span data-ttu-id="55251-132">Операция не может быть выполнена для этого класса, так как у него есть экземпляры.</span><span class="sxs-lookup"><span data-stu-id="55251-132">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span data-ttu-id="55251-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**Модель CIM \_ \_Класс Err \_ имеет \_ экземпляры** (9)</span><span class="sxs-lookup"><span data-stu-id="55251-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM\_ERR\_CLASS\_HAS\_INSTANCES** (9)</span></span>


</dt> <dd>

<span data-ttu-id="55251-134">Операция не может быть выполнена для этого класса, так как у него есть экземпляры.</span><span class="sxs-lookup"><span data-stu-id="55251-134">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span data-ttu-id="55251-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**Модель CIM \_ ERR- \_ Недопустимый \_ Суперкласс** (10)</span><span class="sxs-lookup"><span data-stu-id="55251-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM\_ERR\_INVALID\_SUPERCLASS** (10)</span></span>


</dt> <dd>

<span data-ttu-id="55251-136">Операция не может быть выполнена, так как указанный суперкласс не существует.</span><span class="sxs-lookup"><span data-stu-id="55251-136">Operation cannot be carried out since the specified superclass does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span data-ttu-id="55251-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**Модель CIM \_ ERR \_ уже \_ существует** (11)</span><span class="sxs-lookup"><span data-stu-id="55251-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM\_ERR\_ALREADY\_EXISTS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="55251-138">Операция не может быть выполнена, так как объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="55251-138">Operation cannot be carried out because an object already exists.</span></span>

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span data-ttu-id="55251-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**Модель CIM \_ Ошибка \_ нет \_ такого \_ Свойства** (12)</span><span class="sxs-lookup"><span data-stu-id="55251-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM\_ERR\_NO\_SUCH\_PROPERTY** (12)</span></span>


</dt> <dd>

<span data-ttu-id="55251-140">Указанное свойство не существует.</span><span class="sxs-lookup"><span data-stu-id="55251-140">The specified Property does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span data-ttu-id="55251-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**Модель CIM \_ \_Несоответствие \_ типов Err** (13)</span><span class="sxs-lookup"><span data-stu-id="55251-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM\_ERR\_TYPE\_MISMATCH** (13)</span></span>


</dt> <dd>

<span data-ttu-id="55251-142">Переданное значение несовместимо с типом.</span><span class="sxs-lookup"><span data-stu-id="55251-142">The value supplied is incompatible with the type.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span data-ttu-id="55251-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**Модель CIM \_ \_Язык запросов \_ Err \_ не \_ поддерживается** (14)</span><span class="sxs-lookup"><span data-stu-id="55251-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED** (14)</span></span>


</dt> <dd>

<span data-ttu-id="55251-144">Язык запросов не распознан или не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="55251-144">The query language is not recognized or supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span data-ttu-id="55251-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**Модель CIM \_ \_Недопустимый \_ запрос Err** (15)</span><span class="sxs-lookup"><span data-stu-id="55251-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM\_ERR\_INVALID\_QUERY** (15)</span></span>


</dt> <dd>

<span data-ttu-id="55251-146">Недопустимый запрос для указанного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="55251-146">The query is not valid for the specified query language.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span data-ttu-id="55251-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**Модель CIM \_ \_Метод Err \_ \_ недоступен** (16)</span><span class="sxs-lookup"><span data-stu-id="55251-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE** (16)</span></span>


</dt> <dd>

<span data-ttu-id="55251-148">Не удалось выполнить внешний метод.</span><span class="sxs-lookup"><span data-stu-id="55251-148">The extrinsic Method could not be executed.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span data-ttu-id="55251-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**Модель CIM \_ \_Метод Err \_ не \_ найден** (17)</span><span class="sxs-lookup"><span data-stu-id="55251-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM\_ERR\_METHOD\_NOT\_FOUND** (17)</span></span>


</dt> <dd>

<span data-ttu-id="55251-150">Указанный внешний метод не существует.</span><span class="sxs-lookup"><span data-stu-id="55251-150">The specified extrinsic Method does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span data-ttu-id="55251-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**Модель CIM \_ \_Непредвиденный \_ ответ Err** (18)</span><span class="sxs-lookup"><span data-stu-id="55251-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM\_ERR\_UNEXPECTED\_RESPONSE** (18)</span></span>


</dt> <dd>

<span data-ttu-id="55251-152">Возвращенный ответ на асинхронную операцию не ожидался.</span><span class="sxs-lookup"><span data-stu-id="55251-152">The returned response to the asynchronous operation was not expected.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span data-ttu-id="55251-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**Модель CIM \_ \_Недопустимый \_ \_ адрес назначения ответа Err** (19)</span><span class="sxs-lookup"><span data-stu-id="55251-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION** (19)</span></span>


</dt> <dd>

<span data-ttu-id="55251-154">Указано недопустимое назначение для асинхронного ответа.</span><span class="sxs-lookup"><span data-stu-id="55251-154">The specified destination for the asynchronous response is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span data-ttu-id="55251-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**Модель CIM \_ \_Пространство имен Err \_ не \_ пусто** (20)</span><span class="sxs-lookup"><span data-stu-id="55251-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY** (20)</span></span>


</dt> <dd>

<span data-ttu-id="55251-156">Указанное пространство имен не пусто.</span><span class="sxs-lookup"><span data-stu-id="55251-156">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span data-ttu-id="55251-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**Модель CIM \_ ERR- \_ Недопустимый \_ \_ контекст перечисления** (21)</span><span class="sxs-lookup"><span data-stu-id="55251-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM\_ERR\_INVALID\_ENUMERATION\_CONTEXT** (21)</span></span>


</dt> <dd>

<span data-ttu-id="55251-158">Указан недопустимый контекст перечисления.</span><span class="sxs-lookup"><span data-stu-id="55251-158">The enumeration context supplied is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span data-ttu-id="55251-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**Модель CIM \_ Ошибка \_ недопустимого \_ \_ времени ожидания для операции** (22)</span><span class="sxs-lookup"><span data-stu-id="55251-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM\_ERR\_INVALID\_OPERATION\_TIMEOUT** (22)</span></span>


</dt> <dd>

<span data-ttu-id="55251-160">Указанное пространство имен не пусто.</span><span class="sxs-lookup"><span data-stu-id="55251-160">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span data-ttu-id="55251-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**Модель CIM \_ Ошибка \_ при \_ \_ \_ отброшенном вытягивание** (23)</span><span class="sxs-lookup"><span data-stu-id="55251-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM\_ERR\_PULL\_HAS\_BEEN\_ABANDONED** (23)</span></span>


</dt> <dd>

<span data-ttu-id="55251-162">Указанное пространство имен не пусто.</span><span class="sxs-lookup"><span data-stu-id="55251-162">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span data-ttu-id="55251-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**Модель CIM \_ \_ \_ Не удается \_ \_ отброшенное извлечение Err** (24)</span><span class="sxs-lookup"><span data-stu-id="55251-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM\_ERR\_PULL\_CANNOT\_BE\_ABANDONED** (24)</span></span>


</dt> <dd>

<span data-ttu-id="55251-164">Сбой при попытке отменить операцию извлечения.</span><span class="sxs-lookup"><span data-stu-id="55251-164">The attempt to abandon a pull operation has failed.</span></span>

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span data-ttu-id="55251-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**Модель CIM \_ \_Фильтруемое \_ перечисление Err \_ не \_ поддерживается** (25)</span><span class="sxs-lookup"><span data-stu-id="55251-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM\_ERR\_FILTERED\_ENUMERATION\_NOT\_SUPPORTED** (25)</span></span>


</dt> <dd>

<span data-ttu-id="55251-166">Отфильтрованные Енумератрионс не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="55251-166">Filtered Enumeratrions are not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span data-ttu-id="55251-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**Модель CIM \_ \_Продолжение \_ \_ ошибки \_ не \_ поддерживается** (26)</span><span class="sxs-lookup"><span data-stu-id="55251-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM\_ERR\_CONTINUATION\_ON\_ERROR\_NOT\_SUPPORTED** (26)</span></span>


</dt> <dd>

<span data-ttu-id="55251-168">Продолжение при ошибке не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="55251-168">Continue on error is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span data-ttu-id="55251-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**Модель CIM \_ \_ \_ \_ Превышено ограничение сервера Err** (27)</span><span class="sxs-lookup"><span data-stu-id="55251-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM\_ERR\_SERVER\_LIMITS\_EXCEEDED** (27)</span></span>


</dt> <dd>

<span data-ttu-id="55251-170">Превышены ограничения сервера WBEM (например, память, соединения,...).</span><span class="sxs-lookup"><span data-stu-id="55251-170">The WBEM Server limits have been exceeded (e.g. memory, connections, ...).</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span data-ttu-id="55251-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**Модель CIM \_ \_Сервер Err \_ \_ завершает работу \_** (28)</span><span class="sxs-lookup"><span data-stu-id="55251-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM\_ERR\_SERVER\_IS\_SHUTTING\_DOWN** (28)</span></span>


</dt> <dd>

<span data-ttu-id="55251-172">Сервер WBEM завершает работу.</span><span class="sxs-lookup"><span data-stu-id="55251-172">The WBEM Server is shutting down.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span data-ttu-id="55251-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**Модель CIM \_ \_Функция запросов \_ Err \_ не \_ поддерживается** (29)</span><span class="sxs-lookup"><span data-stu-id="55251-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM\_ERR\_QUERY\_FEATURE\_NOT\_SUPPORTED** (29)</span></span>


</dt> <dd>

<span data-ttu-id="55251-174">Указанная функция запроса не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="55251-174">The specified Query Feature is not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="55251-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="55251-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55251-176">**Цимстатускодедескриптион**</span><span class="sxs-lookup"><span data-stu-id="55251-176">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55251-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55251-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-179">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. \|Ошибка DMTF. Описание \| 2,3 "," DSP0200. DMTF \| Цимеррор \| 1,3 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Цимстатускоде**")</span><span class="sxs-lookup"><span data-stu-id="55251-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.DESCRIPTION\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCode**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-180">Произвольная строка, содержащая удобное для восприятия описание значения свойства **Цимстатускоде** .</span><span class="sxs-lookup"><span data-stu-id="55251-180">A free-form string that contains a human-readable description of the **CIMStatusCode** property value.</span></span>

> [!Note]  
> <span data-ttu-id="55251-181">Это описание может расширяться, но должно соответствовать определению **Цимстатускоде**.</span><span class="sxs-lookup"><span data-stu-id="55251-181">This description may extend, but must be consistent with the definition of **CIMStatusCode**.</span></span>

 

</dd> <dt>

<span data-ttu-id="55251-182">**еррорсаурце**</span><span class="sxs-lookup"><span data-stu-id="55251-182">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55251-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55251-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-185">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Еррорсаурцеформат**")</span><span class="sxs-lookup"><span data-stu-id="55251-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-186">Сведения, определяющие сущность, вызвавшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="55251-186">Information that identifies the entity that generated the error.</span></span> <span data-ttu-id="55251-187">Если сущность моделируется схемой CIM, это свойство содержит путь к экземпляру, закодированный как строковый параметр.</span><span class="sxs-lookup"><span data-stu-id="55251-187">If the entity is modeled by the CIM Schema, this property contains the path to the instance encoded as a string parameter.</span></span> <span data-ttu-id="55251-188">В противном случае свойство содержит строку, которая именует сущность, вызвавшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="55251-188">Otherwise, the property contains a string that names the entity that generated the error.</span></span> <span data-ttu-id="55251-189">Формат этого свойства задается свойством **еррорсаурцеформат** .</span><span class="sxs-lookup"><span data-stu-id="55251-189">The format of this property is specified by the **ErrorSourceFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="55251-190">**еррорсаурцеформат**</span><span class="sxs-lookup"><span data-stu-id="55251-190">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-191">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55251-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55251-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-193">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Еррорсаурце**","**\_ Ошибка CIM**.**Осереррорсаурцеформат**")</span><span class="sxs-lookup"><span data-stu-id="55251-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSource**", "**CIM\_Error**.**OtherErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-194">Формат свойства **еррорсаурце** .</span><span class="sxs-lookup"><span data-stu-id="55251-194">The format of the **ErrorSource** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55251-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="55251-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="55251-196">Неизвестный или неосмысленный формат, интерпретируемый клиентским приложением CIM.</span><span class="sxs-lookup"><span data-stu-id="55251-196">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55251-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="55251-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="55251-198">Формат определяется значением свойства **осереррорсаурцеформат** .</span><span class="sxs-lookup"><span data-stu-id="55251-198">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="55251-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**Цимобжектпас** (2)</span><span class="sxs-lookup"><span data-stu-id="55251-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="55251-200">Путь к объекту CIM, как определено в спецификации инфраструктуры CIM.</span><span class="sxs-lookup"><span data-stu-id="55251-200">A CIM Object Path as defined in the CIM Infrastructure specification.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="55251-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="55251-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55251-202">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="55251-202">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-203">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55251-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55251-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-205">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Осереррортипе**")</span><span class="sxs-lookup"><span data-stu-id="55251-205">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**OtherErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-206">Основной тип ошибки.</span><span class="sxs-lookup"><span data-stu-id="55251-206">The primary error type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55251-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="55251-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55251-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="55251-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span data-ttu-id="55251-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Ошибка связи** (2)</span><span class="sxs-lookup"><span data-stu-id="55251-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Communications Error** (2)</span></span>


</dt> <dd>

<span data-ttu-id="55251-210">Ошибки этого типа связаны с процедурами и (или) процессами, необходимыми для передачи информации из одной точки в другую.</span><span class="sxs-lookup"><span data-stu-id="55251-210">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span data-ttu-id="55251-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Ошибка качества обслуживания** (3)</span><span class="sxs-lookup"><span data-stu-id="55251-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Quality of Service Error** (3)</span></span>


</dt> <dd>

<span data-ttu-id="55251-212">Ошибки этого типа связаны с ошибками, приводящими к снижению функциональности или производительности.</span><span class="sxs-lookup"><span data-stu-id="55251-212">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span>

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="55251-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Ошибка программного обеспечения** (4)</span><span class="sxs-lookup"><span data-stu-id="55251-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="55251-214">Ошибка этого типа связана с программным обеспечением или ошибкой обработки.</span><span class="sxs-lookup"><span data-stu-id="55251-214">Error of this type are principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span data-ttu-id="55251-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Аппаратная ошибка** (5)</span><span class="sxs-lookup"><span data-stu-id="55251-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="55251-216">Ошибки этого типа связаны с оборудованием или сбоем оборудования.</span><span class="sxs-lookup"><span data-stu-id="55251-216">Errors of this type are principally associated with an equipment or hardware failure.</span></span>

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span data-ttu-id="55251-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Ошибка окружающей среды** (6)</span><span class="sxs-lookup"><span data-stu-id="55251-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Environmental Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="55251-218">другие вопросы о окружающей среде.</span><span class="sxs-lookup"><span data-stu-id="55251-218">other environmental considerations.</span></span>

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span data-ttu-id="55251-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Ошибка безопасности** (7)</span><span class="sxs-lookup"><span data-stu-id="55251-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Security Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="55251-220">Ошибки этого типа связаны с нарушениями безопасности, обнаружением вирусов и аналогичными проблемами.</span><span class="sxs-lookup"><span data-stu-id="55251-220">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span>

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span data-ttu-id="55251-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Ошибка превышения лимита подписки** (8)</span><span class="sxs-lookup"><span data-stu-id="55251-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Oversubscription Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="55251-222">Ошибки этого типа связаны с ошибкой при выделении достаточного количества ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="55251-222">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span>

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span data-ttu-id="55251-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Ошибка недоступного ресурса** (9)</span><span class="sxs-lookup"><span data-stu-id="55251-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Unavailable Resource Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="55251-224">Ошибки этого типа связаны с ошибкой доступа к требуемому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="55251-224">Errors of this type are principally associated with the failure to access a required resource.</span></span>

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span data-ttu-id="55251-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Неподдерживаемая ошибка операции** (10)</span><span class="sxs-lookup"><span data-stu-id="55251-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Unsupported Operation Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="55251-226">Ошибки этого типа связаны с неподдерживаемыми запросами.</span><span class="sxs-lookup"><span data-stu-id="55251-226">Errors of this type are principally associated with requests that are not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="55251-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="55251-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55251-228">**Message**</span><span class="sxs-lookup"><span data-stu-id="55251-228">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55251-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55251-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-231">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**MessageID**","**\_ Ошибка CIM**.**Мессажеаргументс**")</span><span class="sxs-lookup"><span data-stu-id="55251-231">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-232">Форматированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="55251-232">The formatted message.</span></span>

> [!Note]  
> <span data-ttu-id="55251-233">Это сообщение создается путем объединения динамических элементов свойства **мессажеаргументс** со статическими элементами свойства **MessageId** , а затем добавления их в реестр сообщений или каталог, связанный с **овнинжентити**.</span><span class="sxs-lookup"><span data-stu-id="55251-233">This message is created by combining dynamic elements of the **MessageArguments** property with the static elements of the **MessageID** property, and then adding them to a message registry or catalog associated with the **OwningEntity**.</span></span>

 

</dd> <dt>

<span data-ttu-id="55251-234">**мессажеаргументс**</span><span class="sxs-lookup"><span data-stu-id="55251-234">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-235">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="55251-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55251-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-237">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**MessageID**","**\_ Ошибка CIM**.**Сообщение**")</span><span class="sxs-lookup"><span data-stu-id="55251-237">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**Message**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-238">Массив, содержащий динамическое содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="55251-238">An array that contains the dynamic content of the message.</span></span>

</dd> <dt>

<span data-ttu-id="55251-239">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="55251-239">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55251-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55251-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-242">Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Сообщение**","**\_ Ошибка CIM**.**Мессажеаргументс**")</span><span class="sxs-lookup"><span data-stu-id="55251-242">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**Message**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-243">Непрозрачная строка, однозначно идентифицирующая в области Овнинжентити формат сообщения.</span><span class="sxs-lookup"><span data-stu-id="55251-243">An opaque string that uniquely identifies, within the scope of the OwningEntity, the format of the Message.</span></span>

</dd> <dt>

<span data-ttu-id="55251-244">**осереррорсаурцеформат**</span><span class="sxs-lookup"><span data-stu-id="55251-244">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-245">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55251-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55251-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-247">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Еррорсаурцеформат**")</span><span class="sxs-lookup"><span data-stu-id="55251-247">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-248">Строка, определяющая значение **еррорсаурцеформат** , если **еррорсаурцеформат** имеет значение "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="55251-248">A string that defines the **ErrorSourceFormat** value when **ErrorSourceFormat** is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="55251-249">**осереррортипе**</span><span class="sxs-lookup"><span data-stu-id="55251-249">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55251-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55251-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-252">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**ErrorType**")</span><span class="sxs-lookup"><span data-stu-id="55251-252">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-253">Произвольная строка, описывающая значение **ErrorType** , если оно равно "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="55251-253">A free-form string that describes the **ErrorType** value when it is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="55251-254">**овнинжентити**</span><span class="sxs-lookup"><span data-stu-id="55251-254">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55251-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55251-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55251-257">Уникальный идентификатор сущности, которой принадлежит формат сообщения, описываемого этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="55251-257">The unique ID of the entity that owns the format of the message described by this instance.</span></span>

> [!Note]  
> <span data-ttu-id="55251-258">Это свойство должно включать имя, охраняемое товарным знаком или уникальное название, которое принадлежит бизнес-сущности или стандартам, заданным в формате сообщения.</span><span class="sxs-lookup"><span data-stu-id="55251-258">This property must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

 

</dd> <dt>

<span data-ttu-id="55251-259">**перцеиведсеверити**</span><span class="sxs-lookup"><span data-stu-id="55251-259">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-260">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55251-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55251-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-262">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Наблюдаемая серьезность ")</span><span class="sxs-lookup"><span data-stu-id="55251-262">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="55251-263">Описание серьезности ошибки с точки зрения элемента, отправившего сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="55251-263">A description of the error severity from the point of view of the element that sent the error message.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55251-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="55251-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="55251-265">Наблюдаемая степень серьезности индикации неизвестна или неопределена.</span><span class="sxs-lookup"><span data-stu-id="55251-265">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55251-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="55251-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="55251-267">Указывает, что значение серьезности можно найти в свойстве **осерсеверити** .</span><span class="sxs-lookup"><span data-stu-id="55251-267">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="55251-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Информация** (2)</span><span class="sxs-lookup"><span data-stu-id="55251-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="55251-269">При предоставлении информативного ответа следует использовать сведения.</span><span class="sxs-lookup"><span data-stu-id="55251-269">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="55251-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Снижение уровня работоспособности/предупреждение** (3)</span><span class="sxs-lookup"><span data-stu-id="55251-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="55251-271">Следует использовать, если нужно, чтобы пользователь мог решить, требуется ли действие.</span><span class="sxs-lookup"><span data-stu-id="55251-271">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="55251-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Дополнительный** (4)</span><span class="sxs-lookup"><span data-stu-id="55251-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="55251-273">Требуется действие, но в настоящее время ситуация не является серьезной.</span><span class="sxs-lookup"><span data-stu-id="55251-273">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="55251-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Основной** (5)</span><span class="sxs-lookup"><span data-stu-id="55251-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="55251-275">Теперь требуется действие.</span><span class="sxs-lookup"><span data-stu-id="55251-275">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="55251-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (6)</span><span class="sxs-lookup"><span data-stu-id="55251-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="55251-277">Требуется действие, и область является широкой (возможно, это приведет к появлению случайного сбоя для критического ресурса).</span><span class="sxs-lookup"><span data-stu-id="55251-277">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="55251-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Неустранимый или невосстанавливаемый** (7)</span><span class="sxs-lookup"><span data-stu-id="55251-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="55251-279">произошла ошибка, но слишком поздно для выполнения действия по воспроизведению мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="55251-279">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="55251-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="55251-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55251-281">**пробаблекаусе**</span><span class="sxs-lookup"><span data-stu-id="55251-281">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-282">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55251-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55251-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-284">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Вероятная причина: "," рекомендация. ITU \| M3100. пробаблекаусе "," ITU-IANA-Alarm-TC "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Пробаблекауседескриптион**")</span><span class="sxs-lookup"><span data-stu-id="55251-284">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCauseDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-285">Описание, возможно, приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="55251-285">A description of te probable cause of the error.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55251-286">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="55251-286">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55251-287">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="55251-287">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="55251-288">**Ошибка адаптера или карты** (2)</span><span class="sxs-lookup"><span data-stu-id="55251-288">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="55251-289">**Сбой подсистемы приложения** (3)</span><span class="sxs-lookup"><span data-stu-id="55251-289">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="55251-290">**Полоса пропускания снижена** (4)</span><span class="sxs-lookup"><span data-stu-id="55251-290">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="55251-291">**Ошибка установки соединения** (5)</span><span class="sxs-lookup"><span data-stu-id="55251-291">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="55251-292">**Ошибка протокола связи** (6)</span><span class="sxs-lookup"><span data-stu-id="55251-292">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="55251-293">**Сбой подсистемы связи** (7)</span><span class="sxs-lookup"><span data-stu-id="55251-293">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="55251-294">**Ошибка настройки или настройки** (8)</span><span class="sxs-lookup"><span data-stu-id="55251-294">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="55251-295">**Перегрузка** (9)</span><span class="sxs-lookup"><span data-stu-id="55251-295">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="55251-296">**Поврежденные данные** (10)</span><span class="sxs-lookup"><span data-stu-id="55251-296">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="55251-297">**Превышен предел циклов ЦП** (11)</span><span class="sxs-lookup"><span data-stu-id="55251-297">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="55251-298">**Набор данных/ошибка модема** (12)</span><span class="sxs-lookup"><span data-stu-id="55251-298">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="55251-299">**Сигнал пониженной функциональности** (13)</span><span class="sxs-lookup"><span data-stu-id="55251-299">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="55251-300">**DTE-ошибка интерфейса DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="55251-300">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="55251-301">**Открыта дверца корпуса** (15)</span><span class="sxs-lookup"><span data-stu-id="55251-301">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="55251-302">**Неисправность оборудования** (16)</span><span class="sxs-lookup"><span data-stu-id="55251-302">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="55251-303">**Чрезмерная вибрация** (17)</span><span class="sxs-lookup"><span data-stu-id="55251-303">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="55251-304">**Ошибка формата файла** (18)</span><span class="sxs-lookup"><span data-stu-id="55251-304">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="55251-305">**Обнаружена Пожарная** программа (19)</span><span class="sxs-lookup"><span data-stu-id="55251-305">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="55251-306">**Обнаружен Flood** (20)</span><span class="sxs-lookup"><span data-stu-id="55251-306">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="55251-307">**Ошибка кадрирования** (21)</span><span class="sxs-lookup"><span data-stu-id="55251-307">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="55251-308">**Проблема с кондиционированием** (22)</span><span class="sxs-lookup"><span data-stu-id="55251-308">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="55251-309">**Недопустимая влажность** (23)</span><span class="sxs-lookup"><span data-stu-id="55251-309">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="55251-310">**Ошибка устройства ввода-вывода** (24)</span><span class="sxs-lookup"><span data-stu-id="55251-310">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="55251-311">**Ошибка устройства ввода** (25)</span><span class="sxs-lookup"><span data-stu-id="55251-311">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="55251-312">**Ошибка локальной сети** (26)</span><span class="sxs-lookup"><span data-stu-id="55251-312">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="55251-313">**Обнаружена Нетоксичнуюная утечка** (27)</span><span class="sxs-lookup"><span data-stu-id="55251-313">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="55251-314">**Ошибка передачи локального узла** (28)</span><span class="sxs-lookup"><span data-stu-id="55251-314">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="55251-315">**Потери кадра** (29)</span><span class="sxs-lookup"><span data-stu-id="55251-315">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="55251-316">**Потери сигнала** (30)</span><span class="sxs-lookup"><span data-stu-id="55251-316">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="55251-317">**Исчерпана заставка материалов** (31)</span><span class="sxs-lookup"><span data-stu-id="55251-317">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="55251-318">**Проблема мультиплексора** (32)</span><span class="sxs-lookup"><span data-stu-id="55251-318">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="55251-319">**Недостаточно памяти** (33)</span><span class="sxs-lookup"><span data-stu-id="55251-319">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="55251-320">**Ошибка устройства вывода** (34)</span><span class="sxs-lookup"><span data-stu-id="55251-320">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="55251-321">Снижение **производительности** (35)</span><span class="sxs-lookup"><span data-stu-id="55251-321">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="55251-322">**Проблема с питанием** (36)</span><span class="sxs-lookup"><span data-stu-id="55251-322">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="55251-323">**Неприемлемое давление** (37)</span><span class="sxs-lookup"><span data-stu-id="55251-323">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="55251-324">**Проблема с процессором (внутренняя ошибка компьютера)** (38)</span><span class="sxs-lookup"><span data-stu-id="55251-324">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="55251-325">**Сбой насоса** (39)</span><span class="sxs-lookup"><span data-stu-id="55251-325">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="55251-326">**Превышен размер очереди** (40)</span><span class="sxs-lookup"><span data-stu-id="55251-326">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="55251-327">**Сбой получения** (41)</span><span class="sxs-lookup"><span data-stu-id="55251-327">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="55251-328">**Сбой получателя** (42)</span><span class="sxs-lookup"><span data-stu-id="55251-328">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="55251-329">**Ошибка передачи удаленного узла** (43)</span><span class="sxs-lookup"><span data-stu-id="55251-329">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="55251-330">**Ресурсы с емкостью или с приближением** (44)</span><span class="sxs-lookup"><span data-stu-id="55251-330">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="55251-331">**Чрезмерное время ответа** (45)</span><span class="sxs-lookup"><span data-stu-id="55251-331">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="55251-332">**Чрезмерная частота** повторной передачи (46)</span><span class="sxs-lookup"><span data-stu-id="55251-332">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="55251-333">**Ошибка программного обеспечения** (47)</span><span class="sxs-lookup"><span data-stu-id="55251-333">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="55251-334">**Программное обеспечение аварийно завершено** (48)</span><span class="sxs-lookup"><span data-stu-id="55251-334">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="55251-335">**Ошибка программного обеспечения (неправильные результаты)** (49)</span><span class="sxs-lookup"><span data-stu-id="55251-335">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="55251-336">**Проблема с емкостью хранилища** (50)</span><span class="sxs-lookup"><span data-stu-id="55251-336">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="55251-337">**Недопустимая температура** (51)</span><span class="sxs-lookup"><span data-stu-id="55251-337">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="55251-338">**Пересечение пороговых значений** (52)</span><span class="sxs-lookup"><span data-stu-id="55251-338">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="55251-339">**Проблема синхронизации** (53)</span><span class="sxs-lookup"><span data-stu-id="55251-339">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="55251-340">**Обнаружена утечка токсичную** (54)</span><span class="sxs-lookup"><span data-stu-id="55251-340">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="55251-341">**Сбой передачи** (55)</span><span class="sxs-lookup"><span data-stu-id="55251-341">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="55251-342">**Сбой передатчика** (56)</span><span class="sxs-lookup"><span data-stu-id="55251-342">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="55251-343">**Базовый ресурс недоступен** (57)</span><span class="sxs-lookup"><span data-stu-id="55251-343">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="55251-344">**Несоответствие версий** (58)</span><span class="sxs-lookup"><span data-stu-id="55251-344">**Version Mismatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="55251-345">**Предыдущее оповещение сброшено** (59)</span><span class="sxs-lookup"><span data-stu-id="55251-345">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="55251-346">**Неудачные попытки входа** (60)</span><span class="sxs-lookup"><span data-stu-id="55251-346">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="55251-347">**Обнаружен вирус по** (61)</span><span class="sxs-lookup"><span data-stu-id="55251-347">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="55251-348">**Нарушение безопасности оборудования** (62)</span><span class="sxs-lookup"><span data-stu-id="55251-348">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="55251-349">**Обнаружен отказ в обслуживании** (63)</span><span class="sxs-lookup"><span data-stu-id="55251-349">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="55251-350">**Несоответствие учетных данных безопасности** (64)</span><span class="sxs-lookup"><span data-stu-id="55251-350">**Security Credential Mismatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="55251-351">**Несанкционированный доступ** (65)</span><span class="sxs-lookup"><span data-stu-id="55251-351">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="55251-352">**Получен сигнал** (66)</span><span class="sxs-lookup"><span data-stu-id="55251-352">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="55251-353">**Потери указателя** (67)</span><span class="sxs-lookup"><span data-stu-id="55251-353">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="55251-354">**Несовпадение полезных данных** (68)</span><span class="sxs-lookup"><span data-stu-id="55251-354">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="55251-355">**Ошибка передачи** (69)</span><span class="sxs-lookup"><span data-stu-id="55251-355">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="55251-356">**Чрезмерная частота ошибок** (70)</span><span class="sxs-lookup"><span data-stu-id="55251-356">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="55251-357">**Проблема трассировки** (71)</span><span class="sxs-lookup"><span data-stu-id="55251-357">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="55251-358">**Элемент недоступен** (72)</span><span class="sxs-lookup"><span data-stu-id="55251-358">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="55251-359">**Отсутствует элемент** (73)</span><span class="sxs-lookup"><span data-stu-id="55251-359">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="55251-360">**Потери нескольких кадров** (74)</span><span class="sxs-lookup"><span data-stu-id="55251-360">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="55251-361">**Сбой широковещательного канала** (75)</span><span class="sxs-lookup"><span data-stu-id="55251-361">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="55251-362">**Получено недопустимое сообщение** (76)</span><span class="sxs-lookup"><span data-stu-id="55251-362">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="55251-363">**Сбой маршрутизации** (77)</span><span class="sxs-lookup"><span data-stu-id="55251-363">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="55251-364">**Сбой объединительной платы** (78)</span><span class="sxs-lookup"><span data-stu-id="55251-364">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="55251-365">**Дублирование идентификаторов** (79)</span><span class="sxs-lookup"><span data-stu-id="55251-365">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="55251-366">**Сбой пути защиты** (80)</span><span class="sxs-lookup"><span data-stu-id="55251-366">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="55251-367">**Потери или несоответствие синхронизации** (81)</span><span class="sxs-lookup"><span data-stu-id="55251-367">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="55251-368">**Проблема с терминалом** (82)</span><span class="sxs-lookup"><span data-stu-id="55251-368">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="55251-369">**Сбой часов реального времени** (83)</span><span class="sxs-lookup"><span data-stu-id="55251-369">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="55251-370">**Сбой антенны** (84)</span><span class="sxs-lookup"><span data-stu-id="55251-370">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="55251-371">**Сбой зарядки аккумулятора** (85)</span><span class="sxs-lookup"><span data-stu-id="55251-371">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="55251-372">**Сбой диска** (86)</span><span class="sxs-lookup"><span data-stu-id="55251-372">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="55251-373">**Частота сбоев прыгающее»** (87)</span><span class="sxs-lookup"><span data-stu-id="55251-373">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="55251-374">**Потери избыточности** (88)</span><span class="sxs-lookup"><span data-stu-id="55251-374">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="55251-375">**Сбой источника питания** (89)</span><span class="sxs-lookup"><span data-stu-id="55251-375">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="55251-376">**Проблема качества сигнала** (90)</span><span class="sxs-lookup"><span data-stu-id="55251-376">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="55251-377">**Заряд аккумулятора** (91)</span><span class="sxs-lookup"><span data-stu-id="55251-377">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="55251-378">**Сбой аккумулятора** (92)</span><span class="sxs-lookup"><span data-stu-id="55251-378">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="55251-379">**Коммерческая проблема электропитания** (93)</span><span class="sxs-lookup"><span data-stu-id="55251-379">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="55251-380">**Сбой вентилятора** (94)</span><span class="sxs-lookup"><span data-stu-id="55251-380">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="55251-381">**Сбой подсистемы** (95)</span><span class="sxs-lookup"><span data-stu-id="55251-381">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="55251-382">**Сбой датчика** (96)</span><span class="sxs-lookup"><span data-stu-id="55251-382">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="55251-383">**Сбой предохранителя** (97)</span><span class="sxs-lookup"><span data-stu-id="55251-383">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="55251-384">**Сбой генератора** (98)</span><span class="sxs-lookup"><span data-stu-id="55251-384">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="55251-385">**Низкий аккумулятор** (99)</span><span class="sxs-lookup"><span data-stu-id="55251-385">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="55251-386">**Низкое топливо** (100)</span><span class="sxs-lookup"><span data-stu-id="55251-386">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="55251-387">**Нижняя вода** (101)</span><span class="sxs-lookup"><span data-stu-id="55251-387">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="55251-388">**Взрывной газ** (102)</span><span class="sxs-lookup"><span data-stu-id="55251-388">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="55251-389">**High подойдет к концу** (103)</span><span class="sxs-lookup"><span data-stu-id="55251-389">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="55251-390">**ICE накрутки** (104)</span><span class="sxs-lookup"><span data-stu-id="55251-390">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="55251-391">**Тест состояния** (105)</span><span class="sxs-lookup"><span data-stu-id="55251-391">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="55251-392">**Несоответствие памяти** (106)</span><span class="sxs-lookup"><span data-stu-id="55251-392">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="55251-393">**Недостаточно циклов ЦП** (107)</span><span class="sxs-lookup"><span data-stu-id="55251-393">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="55251-394">**Проблема программной среды** (108)</span><span class="sxs-lookup"><span data-stu-id="55251-394">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="55251-395">**Сбой загрузки программного обеспечения** (109)</span><span class="sxs-lookup"><span data-stu-id="55251-395">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="55251-396">**Элемент повторно инициализирован** (110)</span><span class="sxs-lookup"><span data-stu-id="55251-396">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="55251-397">**Время ожидания** (111)</span><span class="sxs-lookup"><span data-stu-id="55251-397">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="55251-398">**Регистрация проблем** (112)</span><span class="sxs-lookup"><span data-stu-id="55251-398">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="55251-399">**Обнаружена утечка** (113)</span><span class="sxs-lookup"><span data-stu-id="55251-399">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="55251-400">**Сбой механизма защиты** (114)</span><span class="sxs-lookup"><span data-stu-id="55251-400">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="55251-401">**Сбой защиты ресурса** (115)</span><span class="sxs-lookup"><span data-stu-id="55251-401">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="55251-402">**Несогласованность базы данных** (116)</span><span class="sxs-lookup"><span data-stu-id="55251-402">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="55251-403">**Сбой проверки подлинности** (117)</span><span class="sxs-lookup"><span data-stu-id="55251-403">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="55251-404">**Нарушение конфиденциальности** (118)</span><span class="sxs-lookup"><span data-stu-id="55251-404">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="55251-405">**Несанкционированный кабель** (119)</span><span class="sxs-lookup"><span data-stu-id="55251-405">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="55251-406">**Отложенная информация** (120)</span><span class="sxs-lookup"><span data-stu-id="55251-406">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="55251-407">**Дублирование данных** (121)</span><span class="sxs-lookup"><span data-stu-id="55251-407">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="55251-408">**Отсутствует информация** (122)</span><span class="sxs-lookup"><span data-stu-id="55251-408">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="55251-409">**Изменение сведений** (123)</span><span class="sxs-lookup"><span data-stu-id="55251-409">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="55251-410">**Непоследовательная информация** (124)</span><span class="sxs-lookup"><span data-stu-id="55251-410">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="55251-411">**Истек срок действия ключа** (125)</span><span class="sxs-lookup"><span data-stu-id="55251-411">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="55251-412">**Сбой отказа от отрицания** (126)</span><span class="sxs-lookup"><span data-stu-id="55251-412">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="55251-413">**Активность за нерабочее время** (127)</span><span class="sxs-lookup"><span data-stu-id="55251-413">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="55251-414">Не **обслуживается** (128)</span><span class="sxs-lookup"><span data-stu-id="55251-414">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="55251-415">**Процедурная ошибка** (129)</span><span class="sxs-lookup"><span data-stu-id="55251-415">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="55251-416">**Непредвиденные сведения** (130)</span><span class="sxs-lookup"><span data-stu-id="55251-416">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="55251-417">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="55251-417">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55251-418">**пробаблекауседескриптион**</span><span class="sxs-lookup"><span data-stu-id="55251-418">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-419">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55251-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55251-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55251-421">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Ошибка CIM**.**Пробаблекаусе**")</span><span class="sxs-lookup"><span data-stu-id="55251-421">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="55251-422">Произвольная строка, описывающая вероятную причину ошибки, если свойство **пробаблекаусе** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="55251-422">A free-form string that describes the probable cause of the error, when the **ProbableCause** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="55251-423">**рекоммендедактионс**</span><span class="sxs-lookup"><span data-stu-id="55251-423">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55251-424">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="55251-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55251-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55251-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55251-426">Массив строк произвольной формы, описывающих Рекомендуемые действия, которые необходимо выполнить для разрешения ошибки.</span><span class="sxs-lookup"><span data-stu-id="55251-426">An array of free-form strings that describe the recommended actions to take to resolve the error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55251-427">Требования</span><span class="sxs-lookup"><span data-stu-id="55251-427">Requirements</span></span>



| <span data-ttu-id="55251-428">Требование</span><span class="sxs-lookup"><span data-stu-id="55251-428">Requirement</span></span> | <span data-ttu-id="55251-429">Значение</span><span class="sxs-lookup"><span data-stu-id="55251-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55251-430">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55251-430">Minimum supported client</span></span><br/> | <span data-ttu-id="55251-431">Windows 8</span><span class="sxs-lookup"><span data-stu-id="55251-431">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="55251-432">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55251-432">Minimum supported server</span></span><br/> | <span data-ttu-id="55251-433">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55251-433">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="55251-434">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="55251-434">Namespace</span></span><br/>                | <span data-ttu-id="55251-435">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="55251-435">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="55251-436">MOF</span><span class="sxs-lookup"><span data-stu-id="55251-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55251-437"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55251-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="55251-438">DLL</span><span class="sxs-lookup"><span data-stu-id="55251-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55251-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="55251-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

