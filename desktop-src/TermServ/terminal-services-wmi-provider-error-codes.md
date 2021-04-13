---
title: Коды ошибок поставщика WMI службы удаленных рабочих столов (Вбемкли. h)
description: Ошибки, возвращенные поставщиком WMI службы удаленных рабочих столов. Список других ошибок WMI см. в разделе константы ошибок WMI.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535375"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a><span data-ttu-id="b8ac9-104">Коды ошибок поставщика WMI службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="b8ac9-104">Remote Desktop Services WMI provider error codes</span></span>

<span data-ttu-id="b8ac9-105">В следующем списке перечислены ошибки WMI, возвращенные поставщиком WMI службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-105">The following list lists the WMI errors returned by the Remote Desktop Services WMI provider.</span></span> <span data-ttu-id="b8ac9-106">Список других ошибок WMI см. в разделе [**константы ошибок WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="b8ac9-106">For a list of other WMI errors, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="b8ac9-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**\_сбой WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-108">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-108">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-109">Сбой вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-109">The method call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-111">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-111">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-112">Объект не найден.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-112">The object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_ \_ сбой поставщика WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-114">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-114">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-115">Произошел сбой поставщика в некоторый момент, кроме инициализации.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-115">The provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_несоответствие типов электронной почты WBEM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-117">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-117">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-118">Обнаружено несоответствие типов.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-118">A type mismatch has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ \_ \_ , нехваткой \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-120">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-120">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-121">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-121">There was not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_ \_ Недопустимый параметр "WBEM E" \_**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-123">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-123">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-124">Один из параметров вызова указан неправильно.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-124">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-126">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-126">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-127">Ресурс (обычно удаленный сервер) в данный момент недоступен.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-127">The resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-129">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-129">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-130">Эта функция или операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-130">The feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ недопустимое \_ пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-132">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-132">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-133">Заданное пространство имен не найдено.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-133">The specified namespace could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_ \_ Недопустимый \_ объект для WBEM**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-135">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-135">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-136">Задан недопустимый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-136">The specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ Ошибка инициализации WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-138">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-138">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-139">Не удалось инициализировать модуль, например поставщик, по внутренним причинам.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-139">A module, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ недействительная \_ Операция WBEM E**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-141">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-141">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-142">Запрошенная операция недопустима.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-142">The requested operation is not valid.</span></span> <span data-ttu-id="b8ac9-143">Эта ошибка обычно является ответом на недопустимые попытки удалить классы или свойства.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-143">This error usually applies to invalid attempts to delete classes or properties.</span></span> <span data-ttu-id="b8ac9-144">Эта ошибка возвращается при попытке изменить свойство переопределения сервера с помощью элемента управления групповой политики.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-144">This error is returned on an attempt to modify a server-override property through group policy control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ \_ Недопустимый запрос для WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-146">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-146">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-147">Синтаксически недопустимый запрос.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-147">The query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_ \_ Недопустимый \_ тип запроса WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-149">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-149">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-150">Запрошенный язык запросов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-150">The requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-152">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-152">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-153">В операции размещения был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-153">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ \_ Недопустимый \_ синтаксис WBEM E**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-155">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-155">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-156">Синтаксически недопустимый запрос.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-156">Query is not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**\_только для \_ чтения с WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-158">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-158">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-159">Попытка изменить свойство, доступное в режиме "только чтение".</span><span class="sxs-lookup"><span data-stu-id="b8ac9-159">The property that you are attempting to modify is read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_поставщик WBEM \_ E \_ не \_ поддерживает**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-161">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-161">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-162">Поставщик не может выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-162">The provider cannot perform the requested operation.</span></span> <span data-ttu-id="b8ac9-163">Эта операция может включать слишком сложный запрос, получение экземпляра, создание класса, обновление класса, удаление класса или перечисление класса.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-163">The operation could include a query that is too complex, retrieving an instance, creating a class, updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**\_ \_ недопустимое \_ значение NULL для WBEM E**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-165">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-165">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-166"> /  Для свойства, которое не может иметь значение null, было указано Nothing  / , например, оно помечено квалификатором [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**индексированного**](/windows/desktop/WmiSdk/optional-qualifiers)или [**Not \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) .</span><span class="sxs-lookup"><span data-stu-id="b8ac9-166">A value of **Nothing**/**NULL** was specified for a property that cannot be **Nothing**/**NULL**, such as one that is marked by a [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Indexed**](/windows/desktop/WmiSdk/optional-qualifiers), or [**Not\_Null**](/windows/desktop/WmiSdk/optional-qualifiers) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_значение WBEM E \_ выходит за пределы допустимого \_ \_ \_ диапазона**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-168">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-168">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-169">Запрос выполнен за пределами допустимого интервала значений или же запрос несовместим с типом.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-169">The request was made with an out-of-range value, or is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ \_ Недопустимый \_ метод WBEM E**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-171">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-171">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-172">Запрошенный метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-172">The requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E \_ недопустимые \_ \_ Параметры метода**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-174">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-174">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-175">Предоставленные параметры метода недопустимы.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-175">The parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ac9-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ Недопустимый \_ \_ путь к объекту**</span><span class="sxs-lookup"><span data-stu-id="b8ac9-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8ac9-177">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="b8ac9-177">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="b8ac9-178">Указан недопустимый путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="b8ac9-178">The specified object path was not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8ac9-179">Требования</span><span class="sxs-lookup"><span data-stu-id="b8ac9-179">Requirements</span></span>



| <span data-ttu-id="b8ac9-180">Требование</span><span class="sxs-lookup"><span data-stu-id="b8ac9-180">Requirement</span></span> | <span data-ttu-id="b8ac9-181">Значение</span><span class="sxs-lookup"><span data-stu-id="b8ac9-181">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ac9-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8ac9-182">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ac9-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8ac9-183">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="b8ac9-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8ac9-184">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ac9-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8ac9-185">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="b8ac9-186">Header</span><span class="sxs-lookup"><span data-stu-id="b8ac9-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ac9-187"><dt>Вбемкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ac9-187"><dt>Wbemcli.h</dt></span></span> </dl> |



 

