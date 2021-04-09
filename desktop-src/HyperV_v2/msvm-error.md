---
description: Содержит сведения о серьезности, причинах, рекомендуемых действиях и других данных, связанных со сбоем операции CIM.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Класс Msvm_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080857"
---
# <a name="msvm_error-class"></a><span data-ttu-id="53757-103">Мсвм, \_ класс ошибок</span><span class="sxs-lookup"><span data-stu-id="53757-103">Msvm\_Error class</span></span>

<span data-ttu-id="53757-104">Специализированный класс, который содержит сведения о серьезности, причине, рекомендуемых действиях и других данных, связанных со сбоем операции CIM.</span><span class="sxs-lookup"><span data-stu-id="53757-104">A specialized class that contains information about the severity, cause, recommended actions, and other data related to the failure of a CIM Operation.</span></span>

<span data-ttu-id="53757-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="53757-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="53757-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53757-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
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

## <a name="members"></a><span data-ttu-id="53757-107">Члены</span><span class="sxs-lookup"><span data-stu-id="53757-107">Members</span></span>

<span data-ttu-id="53757-108">Класс **\_ ошибок мсвм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="53757-108">The **Msvm\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="53757-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="53757-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53757-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="53757-110">Properties</span></span>

<span data-ttu-id="53757-111">Класс **\_ Error мсвм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="53757-111">The **Msvm\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53757-112">**Цимстатускоде**</span><span class="sxs-lookup"><span data-stu-id="53757-112">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53757-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53757-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-115">Код состояния CIM, характеризующий этот экземпляр.</span><span class="sxs-lookup"><span data-stu-id="53757-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="53757-116">Это свойство определяет коды состояния, которые могут возвращаться с помощью согласованного сервера или прослушивателя CIM.</span><span class="sxs-lookup"><span data-stu-id="53757-116">This property defines the status codes that may be return by a conforming CIM Server or Listener.</span></span> <span data-ttu-id="53757-117">Не все коды состояния допустимы для каждой операции.</span><span class="sxs-lookup"><span data-stu-id="53757-117">Not all status codes are valid for each operation.</span></span> <span data-ttu-id="53757-118">Спецификация каждой операции должна определять коды состояния, которые могут быть возвращены этой операцией.</span><span class="sxs-lookup"><span data-stu-id="53757-118">The specification for each operation should define the status codes that may be returned by that operation.</span></span> <span data-ttu-id="53757-119">Определены следующие значения для кода состояния CIM.</span><span class="sxs-lookup"><span data-stu-id="53757-119">The following values for CIM status code are defined.</span></span> <span data-ttu-id="53757-120">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-120">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="53757-121">Значение</span><span class="sxs-lookup"><span data-stu-id="53757-121">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="53757-122">Значение</span><span class="sxs-lookup"><span data-stu-id="53757-122">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <span data-ttu-id="53757-123"><dt>**Модель CIM \_ Ошибка \_ ошибки**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53757-123"><dt>**CIM\_ERR\_FAILED**</dt> <dt>1</dt></span></span> </dl>                                                                       | <span data-ttu-id="53757-124">Произошла общая ошибка, которая не охватывает более конкретный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="53757-124">A general error occurred that is not covered by a more specific error code.</span></span><br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <span data-ttu-id="53757-125"><dt>**Модель CIM \_ ERR \_ \_ отказано в доступе**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53757-125"><dt>**CIM\_ERR\_ACCESS\_DENIED**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="53757-126">Доступ к ресурсу CIM недоступен для клиента.</span><span class="sxs-lookup"><span data-stu-id="53757-126">Access to a CIM resource was not available to the client.</span></span><br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <span data-ttu-id="53757-127"><dt>**Модель CIM \_ ERR \_ недопустимое \_ пространство имен**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="53757-127"><dt>**CIM\_ERR\_INVALID\_NAMESPACE**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="53757-128">Целевое пространство имен не существует.</span><span class="sxs-lookup"><span data-stu-id="53757-128">The target namespace does not exist.</span></span><br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <span data-ttu-id="53757-129"><dt>**Модель CIM \_ ERR — \_ Недопустимый \_ параметр**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="53757-129"><dt>**CIM\_ERR\_INVALID\_PARAMETER**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="53757-130">Одно или несколько значений параметров, переданных в метод, недопустимы.</span><span class="sxs-lookup"><span data-stu-id="53757-130">One or more parameter values passed to the method were invalid.</span></span><br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <span data-ttu-id="53757-131"><dt>**Модель CIM \_ ERR — \_ Недопустимый \_ класс**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="53757-131"><dt>**CIM\_ERR\_INVALID\_CLASS**</dt> <dt>5</dt></span></span> </dl>                                                 | <span data-ttu-id="53757-132">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="53757-132">The specified class does not exist.</span></span><br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <span data-ttu-id="53757-133"><dt>**Модель CIM \_ Ошибка \_ не \_ найдена**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="53757-133"><dt>**CIM\_ERR\_NOT\_FOUND**</dt> <dt>6</dt></span></span> </dl>                                                             | <span data-ttu-id="53757-134">Не удалось найти запрошенный объект.</span><span class="sxs-lookup"><span data-stu-id="53757-134">The requested object could not be found.</span></span><br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <span data-ttu-id="53757-135"><dt>**Модель CIM \_ ERR \_ не \_ поддерживается**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="53757-135"><dt>**CIM\_ERR\_NOT\_SUPPORTED**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="53757-136">Запрошенная операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="53757-136">The requested operation is not supported.</span></span><br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <span data-ttu-id="53757-137"><dt>**Модель CIM \_ \_Класс Err \_ имеет \_ дочерние элементы**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="53757-137"><dt>**CIM\_ERR\_CLASS\_HAS\_CHILDREN**</dt> <dt>8</dt></span></span> </dl>                                 | <span data-ttu-id="53757-138">Операция не может быть выполнена для этого класса, так как у него есть экземпляры.</span><span class="sxs-lookup"><span data-stu-id="53757-138">Operation cannot be carried out on this class because it has instances.</span></span><br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <span data-ttu-id="53757-139"><dt>**Модель CIM \_ \_Класс Err \_ имеет \_ экземпляры**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="53757-139"><dt>**CIM\_ERR\_CLASS\_HAS\_INSTANCES**</dt> <dt>9</dt></span></span> </dl>                              | <span data-ttu-id="53757-140">Операция не может быть выполнена для этого класса, так как у него есть экземпляры.</span><span class="sxs-lookup"><span data-stu-id="53757-140">Operation cannot be carried out on this class since it has instances.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <span data-ttu-id="53757-141"><dt>**Модель CIM \_ ERR \_ Недопустимый \_ Суперкласс**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="53757-141"><dt>**CIM\_ERR\_INVALID\_SUPERCLASS**</dt> <dt>10</dt></span></span> </dl>                                 | <span data-ttu-id="53757-142">Операция не может быть выполнена, так как указанный суперкласс не существует.</span><span class="sxs-lookup"><span data-stu-id="53757-142">Operation cannot be carried out since the specified superclass does not exist.</span></span><br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <span data-ttu-id="53757-143"><dt>**Модель CIM \_ ERR \_ уже \_ существует**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="53757-143"><dt>**CIM\_ERR\_ALREADY\_EXISTS**</dt> <dt>11</dt></span></span> </dl>                                             | <span data-ttu-id="53757-144">Операция не может быть выполнена, так как объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="53757-144">Operation cannot be carried out because an object already exists.</span></span><br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <span data-ttu-id="53757-145"><dt>**Модель CIM \_ Ошибка \_ нет \_ такого \_ Свойства**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="53757-145"><dt>**CIM\_ERR\_NO\_SUCH\_PROPERTY**</dt> <dt>12</dt></span></span> </dl>                                      | <span data-ttu-id="53757-146">Указанное свойство не существует.</span><span class="sxs-lookup"><span data-stu-id="53757-146">The specified Property does not exist.</span></span><br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <span data-ttu-id="53757-147"><dt>**Модель CIM \_ \_Несоответствие \_ типа Err**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="53757-147"><dt>**CIM\_ERR\_TYPE\_MISMATCH**</dt> <dt>13</dt></span></span> </dl>                                                | <span data-ttu-id="53757-148">Переданное значение несовместимо с типом.</span><span class="sxs-lookup"><span data-stu-id="53757-148">The value supplied is incompatible with the type.</span></span><br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <span data-ttu-id="53757-149"><dt>**Модель CIM \_ \_Язык запросов \_ Err \_ не \_ поддерживается**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="53757-149"><dt>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED**</dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="53757-150">Язык запросов не распознан или не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="53757-150">The query language is not recognized or supported.</span></span><br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <span data-ttu-id="53757-151"><dt>**Модель CIM \_ ERR — \_ Недопустимый \_ запрос**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="53757-151"><dt>**CIM\_ERR\_INVALID\_QUERY**</dt> <dt>15</dt></span></span> </dl>                                                | <span data-ttu-id="53757-152">Недопустимый запрос для указанного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="53757-152">The query is not valid for the specified query language.</span></span><br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <span data-ttu-id="53757-153"><dt>**Модель CIM \_ \_Метод Err \_ \_ недоступен**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="53757-153"><dt>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE**</dt> <dt>16</dt></span></span> </dl>                          | <span data-ttu-id="53757-154">Не удалось выполнить внешний метод.</span><span class="sxs-lookup"><span data-stu-id="53757-154">The extrinsic method could not be executed.</span></span><br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <span data-ttu-id="53757-155"><dt>**Модель CIM \_ \_Метод Err \_ не \_ найден**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="53757-155"><dt>**CIM\_ERR\_METHOD\_NOT\_FOUND**</dt> <dt>17</dt></span></span> </dl>                                      | <span data-ttu-id="53757-156">Указанный внешний метод не существует.</span><span class="sxs-lookup"><span data-stu-id="53757-156">The specified extrinsic method does not exist.</span></span><br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <span data-ttu-id="53757-157"><dt>**Модель CIM \_ Ошибка \_ непредвиденного \_ ответа**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="53757-157"><dt>**CIM\_ERR\_UNEXPECTED\_RESPONSE**</dt> <dt>18</dt></span></span> </dl>                              | <span data-ttu-id="53757-158">Возвращенный ответ на асинхронную операцию не ожидался.</span><span class="sxs-lookup"><span data-stu-id="53757-158">The returned response to the asynchronous operation was not expected.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <span data-ttu-id="53757-159"><dt>**Модель CIM \_ ERR \_ Недопустимый \_ ответ на \_ адрес**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="53757-159"><dt>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION**</dt> <dt>19</dt></span></span> </dl>  | <span data-ttu-id="53757-160">Указано недопустимое назначение для асинхронного ответа.</span><span class="sxs-lookup"><span data-stu-id="53757-160">The specified destination for the asynchronous response is not valid.</span></span><br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <span data-ttu-id="53757-161"><dt>**Модель CIM \_ \_Пространство имен Err \_ не \_ пусто**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="53757-161"><dt>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY**</dt> <dt>20</dt></span></span> </dl>                             | <span data-ttu-id="53757-162">Указанное пространство имен не пусто.</span><span class="sxs-lookup"><span data-stu-id="53757-162">The specified namespace is not empty.</span></span><br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="53757-163"><dt>**Зарезервировано DMTF**</dt> <dt>21 = *значение*</dt></span><span class="sxs-lookup"><span data-stu-id="53757-163"><dt>**DMTF Reserved**</dt> <dt>21 = *value* </dt></span></span> </dl>                            | <span data-ttu-id="53757-164">Зарезервированные значения.</span><span class="sxs-lookup"><span data-stu-id="53757-164">Reserved values.</span></span><br/>                                                               |



 

</dd> <dt>

<span data-ttu-id="53757-165">**Цимстатускодедескриптион**</span><span class="sxs-lookup"><span data-stu-id="53757-165">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="53757-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53757-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-168">Строка, содержащая понятное для пользователя описание свойства **Цимстатускоде** .</span><span class="sxs-lookup"><span data-stu-id="53757-168">A string containing a user-readable description of the **CIMStatusCode** property.</span></span> <span data-ttu-id="53757-169">Это описание может расширяться, но должно быть совместимо с определением **Цимстатускоде**.</span><span class="sxs-lookup"><span data-stu-id="53757-169">This description may extend, but must be consistent with, the definition of **CIMStatusCode**.</span></span> <span data-ttu-id="53757-170">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-170">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-171">**еррорсаурце**</span><span class="sxs-lookup"><span data-stu-id="53757-171">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="53757-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53757-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-174">Идентифицирующие сведения сущности (экземпляра), генерирующие ошибку.</span><span class="sxs-lookup"><span data-stu-id="53757-174">The identifying information of the entity (the instance) generating the error.</span></span> <span data-ttu-id="53757-175">Если сущность моделируется в схеме CIM, это свойство содержит путь к экземпляру, закодированный в виде строкового параметра.</span><span class="sxs-lookup"><span data-stu-id="53757-175">If this entity is modeled in the CIM Schema, this property contains the path of the instance encoded as a string parameter.</span></span> <span data-ttu-id="53757-176">Если модель не моделируется, свойство содержит определенную строку, которая именует сущность, вызвавшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="53757-176">If not modeled, the property contains some identifying string that names the entity that generated the error.</span></span> <span data-ttu-id="53757-177">Путь или идентифицирующая строка форматируются в соответствии со свойством **еррорсаурцеформат** .</span><span class="sxs-lookup"><span data-stu-id="53757-177">The path or identifying string is formatted per the **ErrorSourceFormat** property.</span></span> <span data-ttu-id="53757-178">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-178">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-179">**еррорсаурцеформат**</span><span class="sxs-lookup"><span data-stu-id="53757-179">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-180">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53757-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53757-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-182">Формат свойства **еррорсаурце** интерпретируется на основе значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="53757-182">The format of the **ErrorSource** property is interpretable based on the value of this property.</span></span> <span data-ttu-id="53757-183">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85))и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="53757-183">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)), and it is always set to 0.</span></span>



| <span data-ttu-id="53757-184">Значение</span><span class="sxs-lookup"><span data-stu-id="53757-184">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="53757-185">Значение</span><span class="sxs-lookup"><span data-stu-id="53757-185">Meaning</span></span>                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="53757-186"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53757-186"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="53757-187">Неизвестный или неосмысленный формат, интерпретируемый клиентским приложением CIM.</span><span class="sxs-lookup"><span data-stu-id="53757-187">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span><br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="53757-188"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53757-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="53757-189">Формат определяется значением свойства **осереррорсаурцеформат** .</span><span class="sxs-lookup"><span data-stu-id="53757-189">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span><br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <span data-ttu-id="53757-190"><dt>**Цимобжександле**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53757-190"><dt>**CIMObjectHandle**</dt> <dt>2 </dt></span></span> </dl> | <span data-ttu-id="53757-191">Объект CIM, закодированный с помощью синтаксиса MOF, определенного для Обжександле, не являющегося терминалом, используется для определения сущности.</span><span class="sxs-lookup"><span data-stu-id="53757-191">A CIM Object Handle, encoded using the MOF syntax defined for the objectHandle non-terminal, is used to identify the entity.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53757-192">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="53757-192">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-193">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53757-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53757-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-195">Основная классификация ошибки.</span><span class="sxs-lookup"><span data-stu-id="53757-195">Primary classification of the error.</span></span> <span data-ttu-id="53757-196">Определены следующие значения.</span><span class="sxs-lookup"><span data-stu-id="53757-196">The following values are defined.</span></span> <span data-ttu-id="53757-197">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-197">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="53757-198">Значение</span><span class="sxs-lookup"><span data-stu-id="53757-198">Value</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="53757-199">Значение</span><span class="sxs-lookup"><span data-stu-id="53757-199">Meaning</span></span>                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="53757-200"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53757-200"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="53757-201"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53757-201"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <span data-ttu-id="53757-202"><dt>**Ошибка связи**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53757-202"><dt>**Communications Error**</dt> <dt>2</dt></span></span> </dl>                               | <span data-ttu-id="53757-203">Ошибки этого типа связаны с процедурами и (или) процессами, необходимыми для передачи информации из одной точки в другую.</span><span class="sxs-lookup"><span data-stu-id="53757-203">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span><br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <span data-ttu-id="53757-204"><dt>**Ошибка качества обслуживания**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="53757-204"><dt>**Quality of Service Error**</dt> <dt>3</dt></span></span> </dl>               | <span data-ttu-id="53757-205">Ошибки этого типа связаны с ошибками, приводящими к снижению функциональности или производительности.</span><span class="sxs-lookup"><span data-stu-id="53757-205">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span><br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <span data-ttu-id="53757-206"><dt>**Программная ошибка**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="53757-206"><dt>**Software Error**</dt> <dt>4</dt></span></span> </dl>                                                       | <span data-ttu-id="53757-207">Ошибка этого типа связана с программным обеспечением или ошибкой обработки.</span><span class="sxs-lookup"><span data-stu-id="53757-207">Error of this type are principally associated with a software or processing fault.</span></span><br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <span data-ttu-id="53757-208"><dt>**Аппаратная ошибка**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="53757-208"><dt>**Hardware Error**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="53757-209">Ошибки этого типа связаны с оборудованием или сбоем оборудования.</span><span class="sxs-lookup"><span data-stu-id="53757-209">Errors of this type are principally associated with an equipment or hardware failure.</span></span><br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <span data-ttu-id="53757-210"><dt>**Ошибка окружающей среды**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="53757-210"><dt>**Environmental Error**</dt> <dt>6</dt></span></span> </dl>                                   | <span data-ttu-id="53757-211">Ошибки этого типа связаны с условием сбоя, связанным с этим средством, или с другими аспектами среды.</span><span class="sxs-lookup"><span data-stu-id="53757-211">Errors of this type are principally associated with a failure condition relating to the facility, or other environmental considerations.</span></span><br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <span data-ttu-id="53757-212"><dt>**Ошибка безопасности**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="53757-212"><dt>**Security Error**</dt> <dt>7</dt></span></span> </dl>                                                       | <span data-ttu-id="53757-213">Ошибки этого типа связаны с нарушениями безопасности, обнаружением вирусов и аналогичными проблемами.</span><span class="sxs-lookup"><span data-stu-id="53757-213">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span><br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <span data-ttu-id="53757-214"><dt>**Ошибка превышения лимита подписки**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="53757-214"><dt>**Oversubscription Error**</dt> <dt>8</dt></span></span> </dl>                       | <span data-ttu-id="53757-215">Ошибки этого типа связаны с ошибкой при выделении достаточного количества ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="53757-215">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span><br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <span data-ttu-id="53757-216"><dt>**Ошибка недоступного ресурса**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="53757-216"><dt>**Unavailable Resource Error**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="53757-217">Ошибки этого типа связаны с ошибкой доступа к требуемому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="53757-217">Errors of this type are principally associated with the failure to access a required resource.</span></span><br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <span data-ttu-id="53757-218"><dt>**Ошибка неподдерживаемой операции**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="53757-218"><dt>**Unsupported Operation Error**</dt> <dt>10 </dt></span></span> </dl> | <span data-ttu-id="53757-219">Ошибки этого типа связаны с неподдерживаемыми запросами.</span><span class="sxs-lookup"><span data-stu-id="53757-219">Errors of this type are principally associated with requests that are not supported.</span></span><br/>                                                          |



 

</dd> <dt>

<span data-ttu-id="53757-220">**Message**</span><span class="sxs-lookup"><span data-stu-id="53757-220">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="53757-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53757-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-223">Форматированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="53757-223">The formatted message.</span></span> <span data-ttu-id="53757-224">Это сообщение создается путем применения динамического содержимого сообщения, описанного в **мессажеаргументс**, к строке формата, однозначно идентифицируемой в области **Овнинжентити**, по **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="53757-224">This message is constructed by applying the dynamic content of the message, described in **MessageArguments**, to the format string uniquely identified, within the scope of the **OwningEntity**, by **MessageID**.</span></span> <span data-ttu-id="53757-225">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-225">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-226">**мессажеаргументс**</span><span class="sxs-lookup"><span data-stu-id="53757-226">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-227">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="53757-227">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="53757-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-229">Массив, содержащий динамическое содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="53757-229">An array containing the dynamic content of the message.</span></span> <span data-ttu-id="53757-230">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-230">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-231">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="53757-231">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="53757-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53757-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-234">Непрозрачная строка, однозначно идентифицирующая в области **овнинжентити** формат сообщения.</span><span class="sxs-lookup"><span data-stu-id="53757-234">An opaque string that uniquely identifies, within the scope of the **OwningEntity**, the format of the message.</span></span> <span data-ttu-id="53757-235">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-235">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-236">**осереррорсаурцеформат**</span><span class="sxs-lookup"><span data-stu-id="53757-236">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="53757-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53757-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-239">Строка, определяющая "другие" значения для **еррорсаурцеформат**.</span><span class="sxs-lookup"><span data-stu-id="53757-239">A string defining "Other" values for **ErrorSourceFormat**.</span></span> <span data-ttu-id="53757-240">Это значение должно быть равно значению, отличному от NULL, если для **еррорсаурцеформат** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="53757-240">This value must be set to a non-NULL value when **ErrorSourceFormat** is set to a value of 1 (Other).</span></span> <span data-ttu-id="53757-241">Для всех остальных значений **еррорсаурцеформат** значение этой строки должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="53757-241">For all other values of **ErrorSourceFormat**, the value of this string must be set to **Null**.</span></span> <span data-ttu-id="53757-242">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-242">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-243">**осереррортипе**</span><span class="sxs-lookup"><span data-stu-id="53757-243">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="53757-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53757-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-246">Строка, описывающая **ErrorType** , если в качестве **ErrorType** задано значение 1, (другое).</span><span class="sxs-lookup"><span data-stu-id="53757-246">A string that describes the **ErrorType** when 1, (Other), is specified as the **ErrorType**.</span></span> <span data-ttu-id="53757-247">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-247">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-248">**овнинжентити**</span><span class="sxs-lookup"><span data-stu-id="53757-248">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="53757-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53757-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-251">Строка, однозначно идентифицирующая сущность, которая владеет определением формата сообщения, описанного в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="53757-251">A string that uniquely identifies the entity that owns the definition of the format of the message described in this instance.</span></span> <span data-ttu-id="53757-252">**Овнинжентити** должен включать в себя авторские права или уникальные имена, которые принадлежат бизнес-сущности или стандартам, определяющим формат.</span><span class="sxs-lookup"><span data-stu-id="53757-252">**OwningEntity** must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity or standards body defining the format.</span></span> <span data-ttu-id="53757-253">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-253">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-254">**перцеиведсеверити**</span><span class="sxs-lookup"><span data-stu-id="53757-254">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-255">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53757-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53757-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-257">Перечислимое значение, описывающее серьезность ошибки из точки зрения уведомления: 2-Low следует использовать для некритических проблем, таких как недопустимые параметры, неправильное использование, неподдерживаемые функции.</span><span class="sxs-lookup"><span data-stu-id="53757-257">An enumerated value that describes the severity of the error from the notifier's point of view: 2 - Low should be used for noncritical issues such as invalid parameters, incorrect usage, unsupported functionality.</span></span> <span data-ttu-id="53757-258">3 — средний следует использовать, чтобы указать, что требуется действие, но в настоящее время ситуация не является серьезной.</span><span class="sxs-lookup"><span data-stu-id="53757-258">3 - Medium should be used to indicate action is needed, but the situation is not serious at this time.</span></span> <span data-ttu-id="53757-259">4 — высокий — следует использовать, чтобы указать, что требуется действие.</span><span class="sxs-lookup"><span data-stu-id="53757-259">4 - High should be used to indicate action is needed now.</span></span> <span data-ttu-id="53757-260">5 — Неустранимая ошибка следует использовать для обозначения потери данных или неустранимой ошибки системы или службы.</span><span class="sxs-lookup"><span data-stu-id="53757-260">5 - Fatal should be used to indicate a loss of data or unrecoverable system or service failure.</span></span> <span data-ttu-id="53757-261">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-261">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="53757-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="53757-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53757-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Низкий** (2)</span><span class="sxs-lookup"><span data-stu-id="53757-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (2)</span></span>
</dt> <dt>

<span data-ttu-id="53757-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Средний** (3)</span><span class="sxs-lookup"><span data-stu-id="53757-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (3)</span></span>
</dt> <dt>

<span data-ttu-id="53757-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Высокий** (4)</span><span class="sxs-lookup"><span data-stu-id="53757-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (4)</span></span>
</dt> <dt>

<span data-ttu-id="53757-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Неустранимая** (5)</span><span class="sxs-lookup"><span data-stu-id="53757-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="53757-267">**пробаблекаусе**</span><span class="sxs-lookup"><span data-stu-id="53757-267">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-268">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53757-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53757-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-270">Перечислимое значение, описывающее вероятную причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="53757-270">An enumerated value that describes the probable cause of the error.</span></span> <span data-ttu-id="53757-271">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-271">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="53757-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="53757-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53757-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="53757-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="53757-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Ошибка адаптера или карты** (2)</span><span class="sxs-lookup"><span data-stu-id="53757-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter/Card Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="53757-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Сбой подсистемы приложения** (3)</span><span class="sxs-lookup"><span data-stu-id="53757-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Application Subsystem Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="53757-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Полоса пропускания снижена** (4)</span><span class="sxs-lookup"><span data-stu-id="53757-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bandwidth Reduced** (4)</span></span>
</dt> <dt>

<span data-ttu-id="53757-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Ошибка установки соединения** (5)</span><span class="sxs-lookup"><span data-stu-id="53757-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Connection Establishment Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="53757-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Ошибка протокола связи** (6)</span><span class="sxs-lookup"><span data-stu-id="53757-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Communications Protocol Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="53757-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Сбой подсистемы связи** (7)</span><span class="sxs-lookup"><span data-stu-id="53757-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Communications Subsystem Failure** (7)</span></span>
</dt> <dt>

<span data-ttu-id="53757-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Ошибка настройки или настройки** (8)</span><span class="sxs-lookup"><span data-stu-id="53757-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Configuration/Customization Error** (8)</span></span>
</dt> <dt>

<span data-ttu-id="53757-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Перегрузка** (9)</span><span class="sxs-lookup"><span data-stu-id="53757-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestion** (9)</span></span>
</dt> <dt>

<span data-ttu-id="53757-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Поврежденные данные** (10)</span><span class="sxs-lookup"><span data-stu-id="53757-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Corrupt Data** (10)</span></span>
</dt> <dt>

<span data-ttu-id="53757-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**Превышен предел циклов ЦП** (11)</span><span class="sxs-lookup"><span data-stu-id="53757-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU Cycles Limit Exceeded** (11)</span></span>
</dt> <dt>

<span data-ttu-id="53757-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Набор данных/ошибка модема** (12)</span><span class="sxs-lookup"><span data-stu-id="53757-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Dataset/Modem Error** (12)</span></span>
</dt> <dt>

<span data-ttu-id="53757-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Сигнал пониженной функциональности** (13)</span><span class="sxs-lookup"><span data-stu-id="53757-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Degraded Signal** (13)</span></span>
</dt> <dt>

<span data-ttu-id="53757-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-ошибка интерфейса DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="53757-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE Interface Error** (14)</span></span>
</dt> <dt>

<span data-ttu-id="53757-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Открыта дверца корпуса** (15)</span><span class="sxs-lookup"><span data-stu-id="53757-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Enclosure Door Open** (15)</span></span>
</dt> <dt>

<span data-ttu-id="53757-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Неисправность оборудования** (16)</span><span class="sxs-lookup"><span data-stu-id="53757-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Equipment Malfunction** (16)</span></span>
</dt> <dt>

<span data-ttu-id="53757-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Чрезмерная вибрация** (17)</span><span class="sxs-lookup"><span data-stu-id="53757-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Excessive Vibration** (17)</span></span>
</dt> <dt>

<span data-ttu-id="53757-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Ошибка формата файла** (18)</span><span class="sxs-lookup"><span data-stu-id="53757-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**File Format Error** (18)</span></span>
</dt> <dt>

<span data-ttu-id="53757-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Обнаружена Пожарная** программа (19)</span><span class="sxs-lookup"><span data-stu-id="53757-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire Detected** (19)</span></span>
</dt> <dt>

<span data-ttu-id="53757-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Обнаружен Flood** (20)</span><span class="sxs-lookup"><span data-stu-id="53757-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood Detected** (20)</span></span>
</dt> <dt>

<span data-ttu-id="53757-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Ошибка кадрирования** (21)</span><span class="sxs-lookup"><span data-stu-id="53757-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Framing Error** (21)</span></span>
</dt> <dt>

<span data-ttu-id="53757-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**Проблема с кондиционированием** (22)</span><span class="sxs-lookup"><span data-stu-id="53757-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC Problem** (22)</span></span>
</dt> <dt>

<span data-ttu-id="53757-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Недопустимая влажность** (23)</span><span class="sxs-lookup"><span data-stu-id="53757-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humidity Unacceptable** (23)</span></span>
</dt> <dt>

<span data-ttu-id="53757-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**Ошибка устройства ввода-вывода** (24)</span><span class="sxs-lookup"><span data-stu-id="53757-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/O Device Error** (24)</span></span>
</dt> <dt>

<span data-ttu-id="53757-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Ошибка устройства ввода** (25)</span><span class="sxs-lookup"><span data-stu-id="53757-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Input Device Error** (25)</span></span>
</dt> <dt>

<span data-ttu-id="53757-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**Ошибка локальной сети** (26)</span><span class="sxs-lookup"><span data-stu-id="53757-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN Error** (26)</span></span>
</dt> <dt>

<span data-ttu-id="53757-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Обнаружена Нетоксичнуюная утечка** (27)</span><span class="sxs-lookup"><span data-stu-id="53757-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Non-Toxic Leak Detected** (27)</span></span>
</dt> <dt>

<span data-ttu-id="53757-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Ошибка передачи локального узла** (28)</span><span class="sxs-lookup"><span data-stu-id="53757-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Local Node Transmission Error** (28)</span></span>
</dt> <dt>

<span data-ttu-id="53757-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Потери кадра** (29)</span><span class="sxs-lookup"><span data-stu-id="53757-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Loss of Frame** (29)</span></span>
</dt> <dt>

<span data-ttu-id="53757-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Потери сигнала** (30)</span><span class="sxs-lookup"><span data-stu-id="53757-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Loss of Signal** (30)</span></span>
</dt> <dt>

<span data-ttu-id="53757-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**31 материал исчерпан** (31)</span><span class="sxs-lookup"><span data-stu-id="53757-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Material Supply Exhausted** (31)</span></span>
</dt> <dt>

<span data-ttu-id="53757-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Проблема мультиплексора** (32)</span><span class="sxs-lookup"><span data-stu-id="53757-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer Problem** (32)</span></span>
</dt> <dt>

<span data-ttu-id="53757-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Недостаточно памяти** (33)</span><span class="sxs-lookup"><span data-stu-id="53757-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Out of Memory** (33)</span></span>
</dt> <dt>

<span data-ttu-id="53757-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Ошибка устройства вывода** (34)</span><span class="sxs-lookup"><span data-stu-id="53757-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Output Device Error** (34)</span></span>
</dt> <dt>

<span data-ttu-id="53757-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>Снижение **производительности** (35)</span><span class="sxs-lookup"><span data-stu-id="53757-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Performance Degraded** (35)</span></span>
</dt> <dt>

<span data-ttu-id="53757-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Проблема с питанием** (36)</span><span class="sxs-lookup"><span data-stu-id="53757-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Power Problem** (36)</span></span>
</dt> <dt>

<span data-ttu-id="53757-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Неприемлемое давление** (37)</span><span class="sxs-lookup"><span data-stu-id="53757-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressure Unacceptable** (37)</span></span>
</dt> <dt>

<span data-ttu-id="53757-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Проблема с процессором (внутренняя ошибка компьютера)** (38)</span><span class="sxs-lookup"><span data-stu-id="53757-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Processor Problem (Internal Machine Error)** (38)</span></span>
</dt> <dt>

<span data-ttu-id="53757-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Сбой насоса** (39)</span><span class="sxs-lookup"><span data-stu-id="53757-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pump Failure** (39)</span></span>
</dt> <dt>

<span data-ttu-id="53757-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Превышен размер очереди** (40)</span><span class="sxs-lookup"><span data-stu-id="53757-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Queue Size Exceeded** (40)</span></span>
</dt> <dt>

<span data-ttu-id="53757-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Сбой получения** (41)</span><span class="sxs-lookup"><span data-stu-id="53757-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Receive Failure** (41)</span></span>
</dt> <dt>

<span data-ttu-id="53757-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Сбой получателя** (42)</span><span class="sxs-lookup"><span data-stu-id="53757-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Receiver Failure** (42)</span></span>
</dt> <dt>

<span data-ttu-id="53757-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Ошибка передачи удаленного узла** (43)</span><span class="sxs-lookup"><span data-stu-id="53757-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remote Node Transmission Error** (43)</span></span>
</dt> <dt>

<span data-ttu-id="53757-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Ресурсы с емкостью или с приближением** (44)</span><span class="sxs-lookup"><span data-stu-id="53757-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Resource at or Nearing Capacity** (44)</span></span>
</dt> <dt>

<span data-ttu-id="53757-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Чрезмерное время ответа** (45)</span><span class="sxs-lookup"><span data-stu-id="53757-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Response Time Excessive** (45)</span></span>
</dt> <dt>

<span data-ttu-id="53757-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Чрезмерная частота** повторной передачи (46)</span><span class="sxs-lookup"><span data-stu-id="53757-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Retransmission Rate Excessive** (46)</span></span>
</dt> <dt>

<span data-ttu-id="53757-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Ошибка программного обеспечения** (47)</span><span class="sxs-lookup"><span data-stu-id="53757-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (47)</span></span>
</dt> <dt>

<span data-ttu-id="53757-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Программное обеспечение аварийно завершено** (48)</span><span class="sxs-lookup"><span data-stu-id="53757-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Software Program Abnormally Terminated** (48)</span></span>
</dt> <dt>

<span data-ttu-id="53757-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Ошибка программного обеспечения (неправильные результаты)** (49)</span><span class="sxs-lookup"><span data-stu-id="53757-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Software Program Error (Incorrect Results)** (49)</span></span>
</dt> <dt>

<span data-ttu-id="53757-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Проблема с емкостью хранилища** (50)</span><span class="sxs-lookup"><span data-stu-id="53757-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="53757-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Недопустимая температура** (51)</span><span class="sxs-lookup"><span data-stu-id="53757-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperature Unacceptable** (51)</span></span>
</dt> <dt>

<span data-ttu-id="53757-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Пересечение пороговых значений** (52)</span><span class="sxs-lookup"><span data-stu-id="53757-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Threshold Crossed** (52)</span></span>
</dt> <dt>

<span data-ttu-id="53757-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Проблема синхронизации** (53)</span><span class="sxs-lookup"><span data-stu-id="53757-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Timing Problem** (53)</span></span>
</dt> <dt>

<span data-ttu-id="53757-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Обнаружена утечка токсичную** (54)</span><span class="sxs-lookup"><span data-stu-id="53757-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Toxic Leak Detected** (54)</span></span>
</dt> <dt>

<span data-ttu-id="53757-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Сбой передачи** (55)</span><span class="sxs-lookup"><span data-stu-id="53757-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Transmit Failure** (55)</span></span>
</dt> <dt>

<span data-ttu-id="53757-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Сбой передатчика** (56)</span><span class="sxs-lookup"><span data-stu-id="53757-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Transmitter Failure** (56)</span></span>
</dt> <dt>

<span data-ttu-id="53757-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Базовый ресурс недоступен** (57)</span><span class="sxs-lookup"><span data-stu-id="53757-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Underlying Resource Unavailable** (57)</span></span>
</dt> <dt>

<span data-ttu-id="53757-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Несоответствие версий** (58)</span><span class="sxs-lookup"><span data-stu-id="53757-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Version Mismatch** (58)</span></span>
</dt> <dt>

<span data-ttu-id="53757-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Предыдущее оповещение сброшено** (59)</span><span class="sxs-lookup"><span data-stu-id="53757-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> <dt>

<span data-ttu-id="53757-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**60 неудачных попыток входа** (60)</span><span class="sxs-lookup"><span data-stu-id="53757-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 Login Attempts Failed** (60)</span></span>
</dt> <dt>

<span data-ttu-id="53757-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Обнаружен вирус по** (61)</span><span class="sxs-lookup"><span data-stu-id="53757-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software Virus Detected** (61)</span></span>
</dt> <dt>

<span data-ttu-id="53757-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Нарушение безопасности оборудования** (62)</span><span class="sxs-lookup"><span data-stu-id="53757-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardware Security Breached** (62)</span></span>
</dt> <dt>

<span data-ttu-id="53757-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Обнаружен отказ в обслуживании** (63)</span><span class="sxs-lookup"><span data-stu-id="53757-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial of Service Detected** (63)</span></span>
</dt> <dt>

<span data-ttu-id="53757-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Несоответствие учетных данных безопасности** (64)</span><span class="sxs-lookup"><span data-stu-id="53757-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Security Credential Mismatch** (64)</span></span>
</dt> <dt>

<span data-ttu-id="53757-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Несанкционированный доступ** (65)</span><span class="sxs-lookup"><span data-stu-id="53757-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Unauthorized Access** (65)</span></span>
</dt> <dt>

<span data-ttu-id="53757-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Получен сигнал** (66)</span><span class="sxs-lookup"><span data-stu-id="53757-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm Received** (66)</span></span>
</dt> <dt>

<span data-ttu-id="53757-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Потери указателя** (67)</span><span class="sxs-lookup"><span data-stu-id="53757-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Loss of Pointer** (67)</span></span>
</dt> <dt>

<span data-ttu-id="53757-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Несовпадение полезных данных** (68)</span><span class="sxs-lookup"><span data-stu-id="53757-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Payload Mismatch** (68)</span></span>
</dt> <dt>

<span data-ttu-id="53757-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Ошибка передачи** (69)</span><span class="sxs-lookup"><span data-stu-id="53757-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Transmission Error** (69)</span></span>
</dt> <dt>

<span data-ttu-id="53757-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Чрезмерная частота ошибок** (70)</span><span class="sxs-lookup"><span data-stu-id="53757-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Excessive Error Rate** (70)</span></span>
</dt> <dt>

<span data-ttu-id="53757-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Проблема трассировки** (71)</span><span class="sxs-lookup"><span data-stu-id="53757-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Trace Problem** (71)</span></span>
</dt> <dt>

<span data-ttu-id="53757-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Элемент недоступен** (72)</span><span class="sxs-lookup"><span data-stu-id="53757-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element Unavailable** (72)</span></span>
</dt> <dt>

<span data-ttu-id="53757-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Отсутствует элемент** (73)</span><span class="sxs-lookup"><span data-stu-id="53757-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Element Missing** (73)</span></span>
</dt> <dt>

<span data-ttu-id="53757-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Потери нескольких кадров** (74)</span><span class="sxs-lookup"><span data-stu-id="53757-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Loss of Multi Frame** (74)</span></span>
</dt> <dt>

<span data-ttu-id="53757-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Сбой широковещательного канала** (75)</span><span class="sxs-lookup"><span data-stu-id="53757-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Broadcast Channel Failure** (75)</span></span>
</dt> <dt>

<span data-ttu-id="53757-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Получено недопустимое сообщение** (76)</span><span class="sxs-lookup"><span data-stu-id="53757-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Invalid Message Received** (76)</span></span>
</dt> <dt>

<span data-ttu-id="53757-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Сбой маршрутизации** (77)</span><span class="sxs-lookup"><span data-stu-id="53757-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routing Failure** (77)</span></span>
</dt> <dt>

<span data-ttu-id="53757-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Сбой объединительной платы** (78)</span><span class="sxs-lookup"><span data-stu-id="53757-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplane Failure** (78)</span></span>
</dt> <dt>

<span data-ttu-id="53757-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Дублирование идентификаторов** (79)</span><span class="sxs-lookup"><span data-stu-id="53757-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Identifier Duplication** (79)</span></span>
</dt> <dt>

<span data-ttu-id="53757-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Сбой пути защиты** (80)</span><span class="sxs-lookup"><span data-stu-id="53757-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Protection Path Failure** (80)</span></span>
</dt> <dt>

<span data-ttu-id="53757-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Потери или несоответствие синхронизации** (81)</span><span class="sxs-lookup"><span data-stu-id="53757-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Sync Loss or Mismatch** (81)</span></span>
</dt> <dt>

<span data-ttu-id="53757-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Проблема с терминалом** (82)</span><span class="sxs-lookup"><span data-stu-id="53757-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminal Problem** (82)</span></span>
</dt> <dt>

<span data-ttu-id="53757-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Сбой часов реального времени** (83)</span><span class="sxs-lookup"><span data-stu-id="53757-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Real Time Clock Failure** (83)</span></span>
</dt> <dt>

<span data-ttu-id="53757-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Сбой антенны** (84)</span><span class="sxs-lookup"><span data-stu-id="53757-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antenna Failure** (84)</span></span>
</dt> <dt>

<span data-ttu-id="53757-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Сбой зарядки аккумулятора** (85)</span><span class="sxs-lookup"><span data-stu-id="53757-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Battery Charging Failure** (85)</span></span>
</dt> <dt>

<span data-ttu-id="53757-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Сбой диска** (86)</span><span class="sxs-lookup"><span data-stu-id="53757-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Disk Failure** (86)</span></span>
</dt> <dt>

<span data-ttu-id="53757-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Частота сбоев прыгающее»** (87)</span><span class="sxs-lookup"><span data-stu-id="53757-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Hopping Failure** (87)</span></span>
</dt> <dt>

<span data-ttu-id="53757-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Потери избыточности** (88)</span><span class="sxs-lookup"><span data-stu-id="53757-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Loss of Redundancy** (88)</span></span>
</dt> <dt>

<span data-ttu-id="53757-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Сбой источника питания** (89)</span><span class="sxs-lookup"><span data-stu-id="53757-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Power Supply Failure** (89)</span></span>
</dt> <dt>

<span data-ttu-id="53757-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Проблема качества сигнала** (90)</span><span class="sxs-lookup"><span data-stu-id="53757-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signal Quality Problem** (90)</span></span>
</dt> <dt>

<span data-ttu-id="53757-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 заряд аккумулятора** (91)</span><span class="sxs-lookup"><span data-stu-id="53757-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 Battery Discharging** (91)</span></span>
</dt> <dt>

<span data-ttu-id="53757-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Сбой аккумулятора** (92)</span><span class="sxs-lookup"><span data-stu-id="53757-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Battery Failure** (92)</span></span>
</dt> <dt>

<span data-ttu-id="53757-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Коммерческая проблема электропитания** (93)</span><span class="sxs-lookup"><span data-stu-id="53757-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Commercial Power Problem** (93)</span></span>
</dt> <dt>

<span data-ttu-id="53757-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Сбой вентилятора** (94)</span><span class="sxs-lookup"><span data-stu-id="53757-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Fan Failure** (94)</span></span>
</dt> <dt>

<span data-ttu-id="53757-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Сбой подсистемы** (95)</span><span class="sxs-lookup"><span data-stu-id="53757-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Engine Failure** (95)</span></span>
</dt> <dt>

<span data-ttu-id="53757-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Сбой датчика** (96)</span><span class="sxs-lookup"><span data-stu-id="53757-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensor Failure** (96)</span></span>
</dt> <dt>

<span data-ttu-id="53757-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Сбой предохранителя** (97)</span><span class="sxs-lookup"><span data-stu-id="53757-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse Failure** (97)</span></span>
</dt> <dt>

<span data-ttu-id="53757-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Сбой генератора** (98)</span><span class="sxs-lookup"><span data-stu-id="53757-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generator Failure** (98)</span></span>
</dt> <dt>

<span data-ttu-id="53757-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Низкий аккумулятор** (99)</span><span class="sxs-lookup"><span data-stu-id="53757-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Low Battery** (99)</span></span>
</dt> <dt>

<span data-ttu-id="53757-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Низкое топливо** (100)</span><span class="sxs-lookup"><span data-stu-id="53757-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Low Fuel** (100)</span></span>
</dt> <dt>

<span data-ttu-id="53757-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Нижняя вода** (101)</span><span class="sxs-lookup"><span data-stu-id="53757-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Low Water** (101)</span></span>
</dt> <dt>

<span data-ttu-id="53757-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Взрывной газ** (102)</span><span class="sxs-lookup"><span data-stu-id="53757-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Explosive Gas** (102)</span></span>
</dt> <dt>

<span data-ttu-id="53757-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**High подойдет к концу** (103)</span><span class="sxs-lookup"><span data-stu-id="53757-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**High Winds** (103)</span></span>
</dt> <dt>

<span data-ttu-id="53757-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**ICE накрутки** (104)</span><span class="sxs-lookup"><span data-stu-id="53757-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice Buildup** (104)</span></span>
</dt> <dt>

<span data-ttu-id="53757-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Тест состояния** (105)</span><span class="sxs-lookup"><span data-stu-id="53757-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Smoke** (105)</span></span>
</dt> <dt>

<span data-ttu-id="53757-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Несоответствие памяти** (106)</span><span class="sxs-lookup"><span data-stu-id="53757-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memory Mismatch** (106)</span></span>
</dt> <dt>

<span data-ttu-id="53757-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Недостаточно циклов ЦП** (107)</span><span class="sxs-lookup"><span data-stu-id="53757-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Out of CPU Cycles** (107)</span></span>
</dt> <dt>

<span data-ttu-id="53757-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Проблема программной среды** (108)</span><span class="sxs-lookup"><span data-stu-id="53757-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Software Environment Problem** (108)</span></span>
</dt> <dt>

<span data-ttu-id="53757-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Сбой загрузки программного обеспечения** (109)</span><span class="sxs-lookup"><span data-stu-id="53757-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Software Download Failure** (109)</span></span>
</dt> <dt>

<span data-ttu-id="53757-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Элемент повторно инициализирован** (110)</span><span class="sxs-lookup"><span data-stu-id="53757-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Element Reinitialized** (110)</span></span>
</dt> <dt>

<span data-ttu-id="53757-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Время ожидания** (111)</span><span class="sxs-lookup"><span data-stu-id="53757-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span></span>
</dt> <dt>

<span data-ttu-id="53757-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Регистрация проблем** (112)</span><span class="sxs-lookup"><span data-stu-id="53757-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Logging Problems** (112)</span></span>
</dt> <dt>

<span data-ttu-id="53757-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Обнаружена утечка** (113)</span><span class="sxs-lookup"><span data-stu-id="53757-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Leak Detected** (113)</span></span>
</dt> <dt>

<span data-ttu-id="53757-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Сбой механизма защиты** (114)</span><span class="sxs-lookup"><span data-stu-id="53757-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Protection Mechanism Failure** (114)</span></span>
</dt> <dt>

<span data-ttu-id="53757-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Защита ресурса не пройдена** (115)</span><span class="sxs-lookup"><span data-stu-id="53757-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protecting Resource Failure** (115)</span></span>
</dt> <dt>

<span data-ttu-id="53757-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Несогласованность базы данных** (116)</span><span class="sxs-lookup"><span data-stu-id="53757-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Database Inconsistency** (116)</span></span>
</dt> <dt>

<span data-ttu-id="53757-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Сбой проверки подлинности** (117)</span><span class="sxs-lookup"><span data-stu-id="53757-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentication Failure** (117)</span></span>
</dt> <dt>

<span data-ttu-id="53757-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Нарушение конфиденциальности** (118)</span><span class="sxs-lookup"><span data-stu-id="53757-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Breach of Confidentiality** (118)</span></span>
</dt> <dt>

<span data-ttu-id="53757-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Несанкционированный кабель** (119)</span><span class="sxs-lookup"><span data-stu-id="53757-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Cable Tamper** (119)</span></span>
</dt> <dt>

<span data-ttu-id="53757-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Отложенная информация** (120)</span><span class="sxs-lookup"><span data-stu-id="53757-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Delayed Information** (120)</span></span>
</dt> <dt>

<span data-ttu-id="53757-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Дублирование данных** (121)</span><span class="sxs-lookup"><span data-stu-id="53757-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Duplicate Information** (121)</span></span>
</dt> <dt>

<span data-ttu-id="53757-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Отсутствует информация** (122)</span><span class="sxs-lookup"><span data-stu-id="53757-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Information Missing** (122)</span></span>
</dt> <dt>

<span data-ttu-id="53757-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Изменение сведений** (123)</span><span class="sxs-lookup"><span data-stu-id="53757-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Information Modification** (123)</span></span>
</dt> <dt>

<span data-ttu-id="53757-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Непоследовательная информация** (124)</span><span class="sxs-lookup"><span data-stu-id="53757-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Information Out of Sequence** (124)</span></span>
</dt> <dt>

<span data-ttu-id="53757-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Истек срок действия ключа** (125)</span><span class="sxs-lookup"><span data-stu-id="53757-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Key Expired** (125)</span></span>
</dt> <dt>

<span data-ttu-id="53757-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Сбой отказа от отрицания** (126)</span><span class="sxs-lookup"><span data-stu-id="53757-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Non-Repudiation Failure** (126)</span></span>
</dt> <dt>

<span data-ttu-id="53757-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Активность за нерабочее время** (127)</span><span class="sxs-lookup"><span data-stu-id="53757-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Out of Hours Activity** (127)</span></span>
</dt> <dt>

<span data-ttu-id="53757-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>Не **обслуживается** (128)</span><span class="sxs-lookup"><span data-stu-id="53757-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out of Service** (128)</span></span>
</dt> <dt>

<span data-ttu-id="53757-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Процедурная ошибка** (129)</span><span class="sxs-lookup"><span data-stu-id="53757-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Procedural Error** (129)</span></span>
</dt> <dt>

<span data-ttu-id="53757-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Непредвиденные сведения** (130)</span><span class="sxs-lookup"><span data-stu-id="53757-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unexpected Information** (130 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="53757-403">**пробаблекауседескриптион**</span><span class="sxs-lookup"><span data-stu-id="53757-403">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-404">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="53757-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53757-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-406">Строка, описывающая вероятную причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="53757-406">A string that describes the probable cause of the error.</span></span> <span data-ttu-id="53757-407">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-407">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="53757-408">**рекоммендедактионс**</span><span class="sxs-lookup"><span data-stu-id="53757-408">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53757-409">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="53757-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="53757-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53757-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53757-411">Строка, описывающая рекомендуемые действия, которые необходимо выполнить для устранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="53757-411">A string that describes recommended actions to take to resolve the error.</span></span> <span data-ttu-id="53757-412">Это свойство наследуется [**от \_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53757-412">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53757-413">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53757-413">Remarks</span></span>

<span data-ttu-id="53757-414">Доступ к классу **\_ ошибок мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="53757-414">Access to the **Msvm\_Error** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="53757-415">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="53757-415">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="53757-416">Требования</span><span class="sxs-lookup"><span data-stu-id="53757-416">Requirements</span></span>



| <span data-ttu-id="53757-417">Требование</span><span class="sxs-lookup"><span data-stu-id="53757-417">Requirement</span></span> | <span data-ttu-id="53757-418">Значение</span><span class="sxs-lookup"><span data-stu-id="53757-418">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53757-419">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53757-419">Minimum supported client</span></span><br/> | <span data-ttu-id="53757-420">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="53757-420">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="53757-421">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53757-421">Minimum supported server</span></span><br/> | <span data-ttu-id="53757-422">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="53757-422">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53757-423">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="53757-423">Namespace</span></span><br/>                | <span data-ttu-id="53757-424">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="53757-424">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="53757-425">MOF</span><span class="sxs-lookup"><span data-stu-id="53757-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53757-426"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53757-426"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53757-427">DLL</span><span class="sxs-lookup"><span data-stu-id="53757-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53757-428"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53757-428"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53757-429">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53757-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53757-430">**\_Ошибка CIM**</span><span class="sxs-lookup"><span data-stu-id="53757-430">**CIM\_Error**</span></span>](cim-error.md)
</dt> <dt>

<span data-ttu-id="53757-431">[**\_Ошибка CIM**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="53757-431">[**CIM\_Error**](/previous-versions//cc150671(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="53757-432">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="53757-432">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

