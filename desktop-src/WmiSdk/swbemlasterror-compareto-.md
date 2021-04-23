---
description: Метод CompareTo \_ объекта свбемластеррор сравнивает два объекта SWbemObject. Это сравнение зависит от определенных ограничений, основанных на значениях, указанных в параметре Ифлагс.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: Метод SWbemLastError.CompareTo_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711647"
---
# <a name="swbemlasterrorcompareto_-method"></a><span data-ttu-id="93033-104">Свбемластеррор. CompareTo, \_ метод</span><span class="sxs-lookup"><span data-stu-id="93033-104">SWbemLastError.CompareTo\_ method</span></span>

<span data-ttu-id="93033-105">Метод **CompareTo \_** объекта [**Свбемластеррор**](swbemlasterror.md) сравнивает два объекта [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="93033-105">The **CompareTo\_** method of the [**SWbemLastError**](swbemlasterror.md) object compares two [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="93033-106">Это сравнение зависит от определенных ограничений, основанных на значениях, указанных в параметре *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="93033-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="93033-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="93033-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="93033-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93033-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="93033-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="93033-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93033-110">*обжвбемобжект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93033-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93033-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="93033-111">Required.</span></span> <span data-ttu-id="93033-112">Объект класса [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="93033-112">An [**SWbemObject**](swbemobject.md) class object.</span></span> <span data-ttu-id="93033-113">Этот параметр является объектом, с которым сравнивается первый объект.</span><span class="sxs-lookup"><span data-stu-id="93033-113">This parameter is the object with which the first object is compared.</span></span> <span data-ttu-id="93033-114">Объект должен быть допустимым экземпляром **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="93033-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="93033-115">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="93033-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93033-116">Целое число, задающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="93033-116">An integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="93033-117">Этот параметр задает характеристики объекта, которые следует учитывать при сравнении объектов.</span><span class="sxs-lookup"><span data-stu-id="93033-117">This parameter specifies the object characteristics to consider when object comparisons are made.</span></span> <span data-ttu-id="93033-118">**Вбемкомпарисонфлагинклудеалл** можно использовать, чтобы учесть все компоненты (по умолчанию) или любое сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="93033-118">You can use **wbemComparisonFlagIncludeAll** to consider all features (default) or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="93033-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>Вбемкомпарисонфлагинклудеалл \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="93033-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="93033-120">Вызывает сравнение всех свойств, квалификаторов и флагов.</span><span class="sxs-lookup"><span data-stu-id="93033-120">Causes all properties, qualifiers, and flavors to be compared.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="93033-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>Вбемкомпарисонфлагигнорекуалифиерс \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="93033-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="93033-122">Приводит к тому, что все квалификаторы (включая **ключ** и **динамический**) будут игнорироваться при сравнении.</span><span class="sxs-lookup"><span data-stu-id="93033-122">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="93033-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>Вбемкомпарисонфлагигнореобжектсаурце \* \* \* \* (0x2)</span><span class="sxs-lookup"><span data-stu-id="93033-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="93033-124">Приводит к тому, что источник объектов, а именно сервер и пространство имен, из которых они пришли, пропускается в сравнении с другими объектами.</span><span class="sxs-lookup"><span data-stu-id="93033-124">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="93033-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>Вбемкомпарисонфлагигноредефаултвалуес \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="93033-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="93033-126">Приводит к игнорированию значений свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93033-126">Causes the default values of properties to be ignored.</span></span> <span data-ttu-id="93033-127">Этот флаг имеет смысл только при сравнении классов.</span><span class="sxs-lookup"><span data-stu-id="93033-127">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="93033-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>Вбемкомпарисонфлагигнорекласс \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="93033-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="93033-129">Предписывает системе предположить, что сравниваемые объекты являются экземплярами одного и того же класса.</span><span class="sxs-lookup"><span data-stu-id="93033-129">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="93033-130">Следовательно, этот флаг сравнивает только сведения, относящиеся к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="93033-130">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="93033-131">Этот флаг позволяет оптимизировать производительность.</span><span class="sxs-lookup"><span data-stu-id="93033-131">Use this flag to optimize performance.</span></span> <span data-ttu-id="93033-132">Если объекты не являются экземплярами одного класса, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="93033-132">If the objects are not of the same class, the results are undefined.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="93033-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>Вбемкомпарисонфлагигнорекасе \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="93033-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="93033-134">Приводит к сравнению строковых значений без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="93033-134">Causes string values to be compared in a case-insensitive manner.</span></span> <span data-ttu-id="93033-135">Это применимо как к строкам, так и к значениям квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="93033-135">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="93033-136">Имена свойств и квалификаторов всегда сравниваются без учета регистра, независимо от того, установлен данный флаг или нет.</span><span class="sxs-lookup"><span data-stu-id="93033-136">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="93033-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>Вбемкомпарисонфлагигнорефлавор \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="93033-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="93033-138">Приводит к игнорированию разновидностей квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="93033-138">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="93033-139">Этот флаг позволяет учитывать значения квалификаторов, но при этом игнорируются такие свойства флага, как правила распространения и ограничения на перезапись.</span><span class="sxs-lookup"><span data-stu-id="93033-139">This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93033-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93033-140">Return value</span></span>

<span data-ttu-id="93033-141">Метод **CompareTo \_** возвращает логическое значение **true** , если объекты совпадают; в противном случае возвращает **false**.</span><span class="sxs-lookup"><span data-stu-id="93033-141">The **CompareTo\_** method returns the Boolean value **TRUE** if the objects match; otherwise, it returns **FALSE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="93033-142">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="93033-142">Error codes</span></span>

<span data-ttu-id="93033-143">После завершения метода **CompareTo \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="93033-143">Upon the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="93033-144">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="93033-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="93033-145">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="93033-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="93033-146">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="93033-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="93033-147">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="93033-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="93033-148">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="93033-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="93033-149">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="93033-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93033-150">Требования</span><span class="sxs-lookup"><span data-stu-id="93033-150">Requirements</span></span>



| <span data-ttu-id="93033-151">Требование</span><span class="sxs-lookup"><span data-stu-id="93033-151">Requirement</span></span> | <span data-ttu-id="93033-152">Значение</span><span class="sxs-lookup"><span data-stu-id="93033-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93033-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93033-153">Minimum supported client</span></span><br/> | <span data-ttu-id="93033-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93033-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93033-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93033-155">Minimum supported server</span></span><br/> | <span data-ttu-id="93033-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93033-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93033-157">Header</span><span class="sxs-lookup"><span data-stu-id="93033-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="93033-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="93033-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="93033-159">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="93033-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="93033-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="93033-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="93033-161">DLL</span><span class="sxs-lookup"><span data-stu-id="93033-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93033-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93033-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="93033-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="93033-163">CLSID</span></span><br/>                    | <span data-ttu-id="93033-164">\_СВБЕМЛАСТЕРРОР CLSID</span><span class="sxs-lookup"><span data-stu-id="93033-164">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="93033-165">IID</span><span class="sxs-lookup"><span data-stu-id="93033-165">IID</span></span><br/>                      | <span data-ttu-id="93033-166">IID \_ исвбемластеррор</span><span class="sxs-lookup"><span data-stu-id="93033-166">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="93033-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93033-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93033-168">**свбемластеррор**</span><span class="sxs-lookup"><span data-stu-id="93033-168">**SWbemLastError**</span></span>](swbemlasterror.md)
</dt> <dt>

[<span data-ttu-id="93033-169">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="93033-169">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




