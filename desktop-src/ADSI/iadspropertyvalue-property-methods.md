---
title: Методы свойств Иадспропертивалуе (iAds. h)
description: Методы свойств интерфейса Иадспропертивалуе обеспечивают доступ к свойствам, описанным в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 1039d4a9-bef8-457d-9a32-3743c14adef1
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспропертивалуе ADSI
topic_type:
- apiref
api_name:
- IADsPropertyValue Property Methods
- IADsPropertyValue.ADsType
- IADsPropertyValue.get_ADsType
- IADsPropertyValue.put_ADsType
- IADsPropertyValue.DNString
- IADsPropertyValue.get_DNString
- IADsPropertyValue.put_DNString
- IADsPropertyValue.CaseExactString
- IADsPropertyValue.get_CaseExactString
- IADsPropertyValue.put_CaseExactString
- IADsPropertyValue.CaseIgnoreString
- IADsPropertyValue.get_CaseIgnoreString
- IADsPropertyValue.put_CaseIgnoreString
- IADsPropertyValue.PrintableString
- IADsPropertyValue.get_PrintableString
- IADsPropertyValue.put_PrintableString
- IADsPropertyValue.NumericString
- IADsPropertyValue.get_NumericString
- IADsPropertyValue.put_NumericString
- IADsPropertyValue.Boolean
- IADsPropertyValue.get_Boolean
- IADsPropertyValue.put_Boolean
- IADsPropertyValue.Integer
- IADsPropertyValue.get_Integer
- IADsPropertyValue.put_Integer
- IADsPropertyValue.OctetString
- IADsPropertyValue.get_OctetString
- IADsPropertyValue.put_OctetString
- IADsPropertyValue.SecurityDescriptor
- IADsPropertyValue.get_SecurityDescriptor
- IADsPropertyValue.put_SecurityDescriptor
- IADsPropertyValue.LargeInteger
- IADsPropertyValue.get_LargeInteger
- IADsPropertyValue.put_LargeInteger
- IADsPropertyValue.UTCTime
- IADsPropertyValue.get_UTCTime
- IADsPropertyValue.put_UTCTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196e8097e5beaa5350738971be29de89b43c17a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490245"
---
# <a name="iadspropertyvalue-property-methods"></a><span data-ttu-id="fe73d-105">Методы свойств Иадспропертивалуе</span><span class="sxs-lookup"><span data-stu-id="fe73d-105">IADsPropertyValue Property Methods</span></span>

<span data-ttu-id="fe73d-106">Методы свойств интерфейса [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) обеспечивают доступ к свойствам, описанным в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fe73d-106">The property methods of the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface provide access to the properties described in the following table.</span></span> <span data-ttu-id="fe73d-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="fe73d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fe73d-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="fe73d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="fe73d-109">**адстипе**</span><span class="sxs-lookup"><span data-stu-id="fe73d-109">**ADsType**</span></span>
<span data-ttu-id="fe73d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-111">Тип данных значения свойства, взятого из перечисления [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) для свойства Value.</span><span class="sxs-lookup"><span data-stu-id="fe73d-111">The data type of the value of the property, taken from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration, of the value property.</span></span>

<dt>

<span data-ttu-id="fe73d-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="fe73d-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* ADsType
);
HRESULT put_ADsType(
  [in] LONG ADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe73d-114">**Boolean**</span></span>
<span data-ttu-id="fe73d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-116">.</span><span class="sxs-lookup"><span data-stu-id="fe73d-116">Boolean value.</span></span>

<dt>

<span data-ttu-id="fe73d-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="fe73d-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Boolean(
  [out] LONG* lnBoolean
);
HRESULT put_Boolean(
  [in] LONG lnBoolean
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-119">**касиксактстринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-119">**CaseExactString**</span></span>
<span data-ttu-id="fe73d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-121">Строка для интерпретации.</span><span class="sxs-lookup"><span data-stu-id="fe73d-121">String to be interpreted.</span></span> <span data-ttu-id="fe73d-122">С учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="fe73d-122">Case-sensitive.</span></span>

<dt>

<span data-ttu-id="fe73d-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-124">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fe73d-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseExactString(
  [out] BSTR* bstrCaseExactString
);
HRESULT put_CaseExactString(
  [in] BSTR bstrCaseExactString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-125">**касеигнорестринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-125">**CaseIgnoreString**</span></span>
<span data-ttu-id="fe73d-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-127">Строка для интерпретации.</span><span class="sxs-lookup"><span data-stu-id="fe73d-127">String to be interpreted.</span></span> <span data-ttu-id="fe73d-128">Без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="fe73d-128">Case insensitive.</span></span>

<dt>

<span data-ttu-id="fe73d-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-130">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fe73d-130">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreString(
  [out] BSTR* bstrCaseIgnoreString
);
HRESULT put_CaseIgnoreString(
  [in] BSTR bstrCaseIgnoreString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-131">**днстринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-131">**DNString**</span></span>
<span data-ttu-id="fe73d-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-133">Строка, определяющая различающееся имя (путь) объекта значения службы каталога.</span><span class="sxs-lookup"><span data-stu-id="fe73d-133">String that identifies the distinguished name (path) of a directory service value object.</span></span>

<dt>

<span data-ttu-id="fe73d-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-135">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fe73d-135">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* bstrDNString
);
HRESULT put_DNString(
  [in] BSTR bstrDNString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-136">**Integer**</span><span class="sxs-lookup"><span data-stu-id="fe73d-136">**Integer**</span></span>
<span data-ttu-id="fe73d-137"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-137"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-138">Целое значение.</span><span class="sxs-lookup"><span data-stu-id="fe73d-138">Integer value.</span></span>

<dt>

<span data-ttu-id="fe73d-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-140">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="fe73d-140">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Integer(
  [out] LONG* lnInteger
);
HRESULT put_Integer(
  [in] LONG lnInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-141">**ларжеинтежер**</span><span class="sxs-lookup"><span data-stu-id="fe73d-141">**LargeInteger**</span></span>
<span data-ttu-id="fe73d-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-143">Указатель на интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) объекта, реализующего [**иадсларжеинтежер**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) для этого значения.</span><span class="sxs-lookup"><span data-stu-id="fe73d-143">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) for this value.</span></span>

<dt>

<span data-ttu-id="fe73d-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-145">Тип данных скрипта: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="fe73d-145">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LargeInteger(
  [out] IDispatch** ppLargeInteger
);
HRESULT put_LargeInteger(
  [in] IDispatch* pLargeInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-146">**нумерикстринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-146">**NumericString**</span></span>
<span data-ttu-id="fe73d-147"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-147"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-148">Текст для интерпретации.</span><span class="sxs-lookup"><span data-stu-id="fe73d-148">Text to be interpreted.</span></span> <span data-ttu-id="fe73d-149">Числовой тип.</span><span class="sxs-lookup"><span data-stu-id="fe73d-149">Numeric type.</span></span>

<dt>

<span data-ttu-id="fe73d-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-151">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fe73d-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NumericString(
  [out] BSTR* bstrNumericString
);
HRESULT put_NumericString(
  [in] BSTR bstrNumericString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-152">**октетстринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-152">**OctetString**</span></span>
<span data-ttu-id="fe73d-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-154">Массив вариантов из однобайтовых символов.</span><span class="sxs-lookup"><span data-stu-id="fe73d-154">Variant array of one-byte characters.</span></span>

<dt>

<span data-ttu-id="fe73d-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-156">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="fe73d-156">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetString(
  [in] VARIANT* vOctetString
);
HRESULT put_OctetString(
  [in] VARIANT* vOctetString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-157">**принтаблестринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-157">**PrintableString**</span></span>
<span data-ttu-id="fe73d-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-159">Отображение или печать строки.</span><span class="sxs-lookup"><span data-stu-id="fe73d-159">Display or print string.</span></span>

<dt>

<span data-ttu-id="fe73d-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-161">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fe73d-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintableString(
  [out] BSTR* bstrPrintableString
);
HRESULT put_PrintableString(
  [in] BSTR bstrPrintableString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-162">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fe73d-162">**SecurityDescriptor**</span></span>
<span data-ttu-id="fe73d-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-164">Указатель на интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) объекта, реализующего [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) для этого значения.</span><span class="sxs-lookup"><span data-stu-id="fe73d-164">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) for this value.</span></span>

<dt>

<span data-ttu-id="fe73d-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-166">Тип данных скрипта: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="fe73d-166">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SecurityDescriptor(
  [out] IDispatch** ppSecurityDescriptor
);
HRESULT put_SecurityDescriptor(
  [in] IDispatch* pSecurityDescriptor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe73d-167">**утктиме**</span><span class="sxs-lookup"><span data-stu-id="fe73d-167">**UTCTime**</span></span>
<span data-ttu-id="fe73d-168"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe73d-168"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe73d-169">Дата типа **VT \_** , выраженная в формате всемирного координированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="fe73d-169">A date of the **VT\_DATE** type expressed in Coordinated Universal Time (UTC) format.</span></span>

<dt>

<span data-ttu-id="fe73d-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe73d-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe73d-171">Тип данных скрипта: **Дата**</span><span class="sxs-lookup"><span data-stu-id="fe73d-171">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UTCTime(
  [out] DATE* daUTCTime
);
HRESULT put_UTCTime(
  [in] DATE daUTCTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="fe73d-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe73d-172">Remarks</span></span>

<span data-ttu-id="fe73d-173">Свойства [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) задают или извлекают значение свойства указанного типа.</span><span class="sxs-lookup"><span data-stu-id="fe73d-173">The [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) properties will only set or retrieve a property value of the specified type.</span></span> <span data-ttu-id="fe73d-174">Например, свойство **касеигнорестринг** атрибута типа **\_ \_ String Адстипе DN**, например атрибут **distinguishedName** , приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="fe73d-174">For example, the **CaseIgnoreString** property on an attribute of type **ADSTYPE\_DN\_STRING**, like the **distinguishedName** attribute, will result in an error.</span></span> <span data-ttu-id="fe73d-175">Свойство **касеигнорестринг** будет работать только с атрибутами типа **ADS \_ \_ \_ строка Ignore**.</span><span class="sxs-lookup"><span data-stu-id="fe73d-175">The **CaseIgnoreString** property will only work on attributes of type **ADS\_CASE\_IGNORE\_STRING**.</span></span> <span data-ttu-id="fe73d-176">В следующей таблице значение [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) сопоставляется с соответствующим свойством **иадспропертивалуе** , которое можно использовать для доступа к этому типу атрибута.</span><span class="sxs-lookup"><span data-stu-id="fe73d-176">The following table maps the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value to the corresponding **IADsPropertyValue** property that can be used to access that attribute type.</span></span> <span data-ttu-id="fe73d-177">Если значение **адстипинум** не указано в этой таблице, оно недоступно из интерфейса **иадспропертивалуе** .</span><span class="sxs-lookup"><span data-stu-id="fe73d-177">If an **ADSTYPEENUM** value is not listed in this table, it is not available from the **IADsPropertyValue** interface.</span></span> <span data-ttu-id="fe73d-178">Для получения данных в других форматах следует использовать интерфейс [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) .</span><span class="sxs-lookup"><span data-stu-id="fe73d-178">The [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interface should be used to obtain data in the other formats.</span></span>



| <span data-ttu-id="fe73d-179">Значение [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum)</span><span class="sxs-lookup"><span data-stu-id="fe73d-179">[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value</span></span> | <span data-ttu-id="fe73d-180">[**Иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) , свойство</span><span class="sxs-lookup"><span data-stu-id="fe73d-180">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) property</span></span> |
|------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fe73d-181">**\_строка различающегося имени адстипе \_**</span><span class="sxs-lookup"><span data-stu-id="fe73d-181">**ADSTYPE\_DN\_STRING**</span></span>                  | <span data-ttu-id="fe73d-182">**днстринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-182">**DNString**</span></span>                                            |
| <span data-ttu-id="fe73d-183">**\_точный регистр \_ адстипе \_ строки**</span><span class="sxs-lookup"><span data-stu-id="fe73d-183">**ADSTYPE\_CASE\_EXACT\_STRING**</span></span>         | <span data-ttu-id="fe73d-184">**касиксактстринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-184">**CaseExactString**</span></span>                                     |
| <span data-ttu-id="fe73d-185">**АДСТИПЕ \_ не \_ учитывать регистр \_ строк**</span><span class="sxs-lookup"><span data-stu-id="fe73d-185">**ADSTYPE\_CASE\_IGNORE\_STRING**</span></span>        | <span data-ttu-id="fe73d-186">**касеигнорестринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-186">**CaseIgnoreString**</span></span>                                    |
| <span data-ttu-id="fe73d-187">**АДСТИПЕ \_ Печатная \_ строка**</span><span class="sxs-lookup"><span data-stu-id="fe73d-187">**ADSTYPE\_PRINTABLE\_STRING**</span></span>           | <span data-ttu-id="fe73d-188">**принтаблестринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-188">**PrintableString**</span></span>                                     |
| <span data-ttu-id="fe73d-189">**АДСТИПЕ \_ числовая \_ строка**</span><span class="sxs-lookup"><span data-stu-id="fe73d-189">**ADSTYPE\_NUMERIC\_STRING**</span></span>             | <span data-ttu-id="fe73d-190">**нумерикстринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-190">**NumericString**</span></span>                                       |
| <span data-ttu-id="fe73d-191">**АДСТИПЕ \_ Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe73d-191">**ADSTYPE\_BOOLEAN**</span></span>                     | <span data-ttu-id="fe73d-192">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe73d-192">**Boolean**</span></span>                                             |
| <span data-ttu-id="fe73d-193">**АДСТИПЕ \_ целое число**</span><span class="sxs-lookup"><span data-stu-id="fe73d-193">**ADSTYPE\_INTEGER**</span></span>                     | <span data-ttu-id="fe73d-194">**Integer**</span><span class="sxs-lookup"><span data-stu-id="fe73d-194">**Integer**</span></span>                                             |
| <span data-ttu-id="fe73d-195">**\_Строка октета адстипе \_**</span><span class="sxs-lookup"><span data-stu-id="fe73d-195">**ADSTYPE\_OCTET\_STRING**</span></span>               | <span data-ttu-id="fe73d-196">**октетстринг**</span><span class="sxs-lookup"><span data-stu-id="fe73d-196">**OctetString**</span></span>                                         |
| <span data-ttu-id="fe73d-197">**АДСТИПЕ \_ время в формате UTC \_**</span><span class="sxs-lookup"><span data-stu-id="fe73d-197">**ADSTYPE\_UTC\_TIME**</span></span>                   | <span data-ttu-id="fe73d-198">**утктиме**</span><span class="sxs-lookup"><span data-stu-id="fe73d-198">**UTCTime**</span></span>                                             |
| <span data-ttu-id="fe73d-199">**АДСТИПЕ \_ большое \_ целое**</span><span class="sxs-lookup"><span data-stu-id="fe73d-199">**ADSTYPE\_LARGE\_INTEGER**</span></span>              | <span data-ttu-id="fe73d-200">**ларжеинтежер**</span><span class="sxs-lookup"><span data-stu-id="fe73d-200">**LargeInteger**</span></span>                                        |
| <span data-ttu-id="fe73d-201">**\_ \_ дескриптор безопасности адстипе \_ NT**</span><span class="sxs-lookup"><span data-stu-id="fe73d-201">**ADSTYPE\_NT\_SECURITY\_DESCRIPTOR**</span></span>    | <span data-ttu-id="fe73d-202">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fe73d-202">**SecurityDescriptor**</span></span>                                  |



 

## <a name="examples"></a><span data-ttu-id="fe73d-203">Примеры</span><span class="sxs-lookup"><span data-stu-id="fe73d-203">Examples</span></span>

<span data-ttu-id="fe73d-204">В следующем примере кода показано, как получить свойство из списка свойств.</span><span class="sxs-lookup"><span data-stu-id="fe73d-204">The following code example shows how to retrieve a property from the property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Retrieve the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Retrieve a property entry. If you are certain of the property type,
' replace ADSTYPE_UNKNOWN with the actual property type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Print the property entry values.
For Each v In propEntry.Values
    Set propVal = v
    Select Case propVal.ADsType
        Case ADSTYPE_CASE_EXACT_STRING
            Debug.Print propVal.CaseExactString
        Case ADSTYPE_CASE_IGNORE_STRING
            Debug.Print propVal.CaseIgnoreString
        Case Else
            Debug.Print "Unable to handle a property of type: " & propVal.ADsType
    End Select
    
Next

Cleanup:
    If (Err.Number<>0) Then
       Debug.Print "An error has occurred. " & Err.Number
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="fe73d-205">В следующем коде показано, как использовать **иадспропертивалуе:: Get \_ касеигнорестринг** для получения значения свойства Description из списка свойств.</span><span class="sxs-lookup"><span data-stu-id="fe73d-205">The following code shows how to use **IADsPropertyValue::get\_CaseIgnoreString** to retrieve the value of the description property from a property list.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart = 0;
LONG lend = 0;
LONG lADsType = ADSTYPE_UNKNOWN;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);

if(FAILED(hr)){goto Cleanup;}

// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Retrieve the property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_CASE_IGNORE_STRING, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}

hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Retrieve the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}

SAFEARRAY *sa = V_ARRAY( &var );
 
// Retrieve the lower and upper bound. Iterate and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    if(FAILED(hr)){goto Cleanup;}

    pVal->get_ADsType(&lADsType);

    switch(lADsType)
    {
        case ADSTYPE_CASE_IGNORE_STRING:
        {
            hr = pVal->get_CaseIgnoreString(&valStr);
            break;
        }
        case ADSTYPE_CASE_EXACT_STRING:
        {
            hr = pVal->get_CaseExactString(&valStr);
            break;
        }
        default:
        {
            valStr = SysAllocString(L"Unable to handle a property of this type");
            break;
        }
    }

    if(FAILED(hr)){goto Cleanup;}
    printf(" %S ", valStr);
    SysFreeString(valStr);
    VariantClear(&varItem);
}
printf("\n");

Cleanup:
    if(pList)
        pList = NULL;

    if(pEntry)
        pEntry = NULL;

    if(pVal)
        pVal = NULL;

    if(pObj)
        pObj = NULL;

    if(pEnum)
        pEnum = NULL;

    SysFreeString(valStr);
    VariantClear(&varItem);
    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="fe73d-206">Требования</span><span class="sxs-lookup"><span data-stu-id="fe73d-206">Requirements</span></span>



| <span data-ttu-id="fe73d-207">Требование</span><span class="sxs-lookup"><span data-stu-id="fe73d-207">Requirement</span></span> | <span data-ttu-id="fe73d-208">Значение</span><span class="sxs-lookup"><span data-stu-id="fe73d-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe73d-209">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe73d-209">Minimum supported client</span></span><br/> | <span data-ttu-id="fe73d-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe73d-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe73d-211">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe73d-211">Minimum supported server</span></span><br/> | <span data-ttu-id="fe73d-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe73d-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe73d-213">Header</span><span class="sxs-lookup"><span data-stu-id="fe73d-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe73d-214"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe73d-214"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="fe73d-215">DLL</span><span class="sxs-lookup"><span data-stu-id="fe73d-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe73d-216"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe73d-216"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe73d-217">IID</span><span class="sxs-lookup"><span data-stu-id="fe73d-217">IID</span></span><br/>                      | <span data-ttu-id="fe73d-218">IID \_ иадспропертивалуе определен как 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="fe73d-218">IID\_IADsPropertyValue is defined as 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="fe73d-219">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe73d-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe73d-220">**иадспропертивалуе**</span><span class="sxs-lookup"><span data-stu-id="fe73d-220">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="fe73d-221">**адстипинум**</span><span class="sxs-lookup"><span data-stu-id="fe73d-221">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="fe73d-222">**иадспропертентри**</span><span class="sxs-lookup"><span data-stu-id="fe73d-222">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="fe73d-223">**иадспропертилист**</span><span class="sxs-lookup"><span data-stu-id="fe73d-223">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="fe73d-224">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="fe73d-224">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="fe73d-225">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fe73d-225">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="fe73d-226">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="fe73d-226">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

