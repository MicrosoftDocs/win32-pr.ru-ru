---
description: Метод CompareTo \_ объекта SWbemObject сравнивает два объекта SWbemObject. Это сравнение зависит от определенных ограничений, основанных на значениях, указанных в параметре Ифлагс.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: Метод SWbemObject.CompareTo_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f77bf9db9ee864e136ba695051445e543b466e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812412"
---
# <a name="swbemobjectcompareto_-method"></a><span data-ttu-id="6cce0-104">SWbemObject. CompareTo, \_ метод</span><span class="sxs-lookup"><span data-stu-id="6cce0-104">SWbemObject.CompareTo\_ method</span></span>

<span data-ttu-id="6cce0-105">Метод **CompareTo \_** объекта [**SWbemObject**](swbemobject.md) сравнивает два объекта **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="6cce0-105">The **CompareTo\_** method of the [**SWbemObject**](swbemobject.md) object compares two **SWbemObject** objects.</span></span> <span data-ttu-id="6cce0-106">Это сравнение зависит от определенных ограничений, основанных на значениях, указанных в параметре *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="6cce0-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="6cce0-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6cce0-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6cce0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cce0-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6cce0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cce0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cce0-110">*обжвбемобжект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cce0-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cce0-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6cce0-111">Required.</span></span> <span data-ttu-id="6cce0-112">Этот параметр является объектом [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="6cce0-112">This parameter is an [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="6cce0-113">Это объект, с которым сравнивается первый объект.</span><span class="sxs-lookup"><span data-stu-id="6cce0-113">This is the object with which the first object is compared.</span></span> <span data-ttu-id="6cce0-114">Объект должен быть допустимым экземпляром **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="6cce0-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="6cce0-115">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6cce0-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cce0-116">Задает характеристики объекта, которые следует учитывать при сравнении объекта с другими объектами.</span><span class="sxs-lookup"><span data-stu-id="6cce0-116">Specifies the object characteristics to consider when comparing an object with other objects.</span></span> <span data-ttu-id="6cce0-117">Можно использовать **вбемкомпарисонфлагинклудеалл** , чтобы расдумать все компоненты (это значение по умолчанию) или любое сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6cce0-117">You can use **wbemComparisonFlagIncludeAll** to consider all features (this is the default), or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="6cce0-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>Вбемкомпарисонфлагинклудеалл \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6cce0-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6cce0-119">Сравнивает все свойства, квалификаторы и разновидности.</span><span class="sxs-lookup"><span data-stu-id="6cce0-119">Compares all properties, qualifiers, and flavors.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="6cce0-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>Вбемкомпарисонфлагигнореобжектсаурце \* \* \* \* (0x2)</span><span class="sxs-lookup"><span data-stu-id="6cce0-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="6cce0-121">Приводит к тому, что источник объектов, а именно сервер и пространство имен, из которых они пришли, пропускается в сравнении с другими объектами.</span><span class="sxs-lookup"><span data-stu-id="6cce0-121">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="6cce0-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>Вбемкомпарисонфлагигнорекуалифиерс \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="6cce0-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="6cce0-123">Приводит к тому, что все квалификаторы (включая **ключ** и **динамический**) будут игнорироваться при сравнении.</span><span class="sxs-lookup"><span data-stu-id="6cce0-123">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="6cce0-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>Вбемкомпарисонфлагигноредефаултвалуес \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="6cce0-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="6cce0-125">Вызывает игнорирование значений свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6cce0-125">Causes default values of properties to be ignored.</span></span> <span data-ttu-id="6cce0-126">Этот флаг имеет смысл только при сравнении классов.</span><span class="sxs-lookup"><span data-stu-id="6cce0-126">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="6cce0-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>Вбемкомпарисонфлагигнорефлавор \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="6cce0-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="6cce0-128">Приводит к игнорированию разновидностей квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="6cce0-128">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="6cce0-129">Этот флаг учитывает значения квалификаторов, но не учитывает различия в разновидностях, например правила распространения и ограничения переопределения.</span><span class="sxs-lookup"><span data-stu-id="6cce0-129">This flag takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="6cce0-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>Вбемкомпарисонфлагигнорекасе \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="6cce0-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="6cce0-131">Сравнивает строковые значения без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="6cce0-131">Compares string values in a case-insensitive manner.</span></span> <span data-ttu-id="6cce0-132">Это применимо как к строкам, так и к значениям квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="6cce0-132">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="6cce0-133">Имена свойств и квалификаторов всегда сравниваются без учета регистра, независимо от того, установлен данный флаг или нет.</span><span class="sxs-lookup"><span data-stu-id="6cce0-133">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="6cce0-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>Вбемкомпарисонфлагигнорекласс \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="6cce0-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="6cce0-135">Предписывает системе предположить, что сравниваемые объекты являются экземплярами одного и того же класса.</span><span class="sxs-lookup"><span data-stu-id="6cce0-135">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="6cce0-136">Следовательно, этот флаг сравнивает только сведения, относящиеся к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="6cce0-136">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="6cce0-137">Этот флаг позволяет оптимизировать производительность.</span><span class="sxs-lookup"><span data-stu-id="6cce0-137">Use this flag to optimize performance.</span></span> <span data-ttu-id="6cce0-138">Если объекты не являются экземплярами одного класса, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="6cce0-138">If the objects are not of the same class, the results are undefined.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cce0-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cce0-139">Return value</span></span>

<span data-ttu-id="6cce0-140">Этот метод возвращает логическое значение **true** , если объекты совпадают.</span><span class="sxs-lookup"><span data-stu-id="6cce0-140">This method returns the Boolean value of **TRUE** if the objects match.</span></span> <span data-ttu-id="6cce0-141">Если объекты не совпадают, возвращается **значение false** .</span><span class="sxs-lookup"><span data-stu-id="6cce0-141">It returns **FALSE** if the objects do not match.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6cce0-142">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6cce0-142">Error codes</span></span>

<span data-ttu-id="6cce0-143">После завершения метода **CompareTo \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="6cce0-143">After the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6cce0-144">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6cce0-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6cce0-145">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6cce0-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6cce0-146">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6cce0-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6cce0-147">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="6cce0-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6cce0-148">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6cce0-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6cce0-149">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="6cce0-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6cce0-150">Требования</span><span class="sxs-lookup"><span data-stu-id="6cce0-150">Requirements</span></span>



| <span data-ttu-id="6cce0-151">Требование</span><span class="sxs-lookup"><span data-stu-id="6cce0-151">Requirement</span></span> | <span data-ttu-id="6cce0-152">Значение</span><span class="sxs-lookup"><span data-stu-id="6cce0-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cce0-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cce0-153">Minimum supported client</span></span><br/> | <span data-ttu-id="6cce0-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cce0-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6cce0-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cce0-155">Minimum supported server</span></span><br/> | <span data-ttu-id="6cce0-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cce0-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6cce0-157">Header</span><span class="sxs-lookup"><span data-stu-id="6cce0-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cce0-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cce0-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6cce0-159">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6cce0-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="6cce0-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6cce0-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6cce0-161">DLL</span><span class="sxs-lookup"><span data-stu-id="6cce0-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cce0-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cce0-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6cce0-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="6cce0-163">CLSID</span></span><br/>                    | <span data-ttu-id="6cce0-164">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="6cce0-164">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="6cce0-165">IID</span><span class="sxs-lookup"><span data-stu-id="6cce0-165">IID</span></span><br/>                      | <span data-ttu-id="6cce0-166">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="6cce0-166">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="6cce0-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cce0-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cce0-168">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="6cce0-168">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




