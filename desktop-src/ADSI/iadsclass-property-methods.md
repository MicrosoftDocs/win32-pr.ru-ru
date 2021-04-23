---
title: Методы свойств Иадскласс (iAds. h)
description: Методы свойств интерфейса Иадскласс получают или устанавливают следующие свойства. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадскласс ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136882"
---
# <a name="iadsclass-property-methods"></a><span data-ttu-id="bcdc6-105">Методы свойств Иадскласс</span><span class="sxs-lookup"><span data-stu-id="bcdc6-105">IADsClass Property Methods</span></span>

<span data-ttu-id="bcdc6-106">Методы свойств интерфейса [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) получают или устанавливают следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-106">The property methods of the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface get or set the following properties.</span></span> <span data-ttu-id="bcdc6-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="bcdc6-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="bcdc6-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="bcdc6-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="bcdc6-109">**Выделяет**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-109">**Abstract**</span></span>
<span data-ttu-id="bcdc6-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-111">Логическое значение, указывающее, является ли этот класс абстрактным или неабстрактным.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-111">Boolean value that indicates if this class is Abstract or non-abstract.</span></span> <span data-ttu-id="bcdc6-112">Если **значение равно true**, этот класс является абстрактным и не может быть создан напрямую в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-112">When **TRUE**, this class is an Abstract class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="bcdc6-113">Абстрактные классы могут использоваться только как классы суперклассов.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-113">Abstract classes can only be used as super classes.</span></span>

<dt>

<span data-ttu-id="bcdc6-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-115">Тип данных скрипта: **логическое значение**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-115">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-116">**ауксдериведфром**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-116">**AuxDerivedFrom**</span></span>
<span data-ttu-id="bcdc6-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-118">Массив ADsPath строк, указывающий классы Super, от которых наследует этот класс.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-118">Array of ADsPath strings that indicate the super Auxiliary classes this class derives from.</span></span>

<dt>

<span data-ttu-id="bcdc6-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-120">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-121">**Четки**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-121">**Auxiliary**</span></span>
<span data-ttu-id="bcdc6-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-123">Логическое значение, указывающее, является ли этот класс вспомогательным.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-123">Boolean value that indicates whether or not this class is Auxiliary.</span></span> <span data-ttu-id="bcdc6-124">Если **значение равно true**, этот класс является вспомогательным классом и не может быть создан напрямую в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-124">When **TRUE**, this class is an Auxiliary class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="bcdc6-125">Вспомогательные классы могут использоваться только как суперклассы других вспомогательных классов или как источник дополнительных свойств в структурных классах.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-125">Auxiliary classes can only be used as super classes of other Auxiliary classes or as a source of additional properties on structural classes.</span></span>

<dt>

<span data-ttu-id="bcdc6-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-127">Тип данных скрипта: **логическое значение**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-127">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-128">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-128">**CLSID**</span></span>
<span data-ttu-id="bcdc6-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-130">Необязательный CLSID, зависящий от поставщика, определяющий COM-объект, реализующий этот класс.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-130">Optional provider-specific CLSID identifying the COM object that implements this class.</span></span>

<dt>

<span data-ttu-id="bcdc6-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-132">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-133">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-133">**Container**</span></span>
<span data-ttu-id="bcdc6-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-135">Логическое значение, указывающее, может ли этот класс быть контейнером других классов объектов.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-135">Boolean value that indicates if this class can be a container of other object classes.</span></span> <span data-ttu-id="bcdc6-136">Если это значение равно **true**, можно вызвать метод **Get \_ Container** , чтобы получить массив классов объектов, которые может содержать этот класс.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-136">If this value is **TRUE**, you can call the **get\_Container** method to get an array of the object classes that this class can contain.</span></span>

<dt>

<span data-ttu-id="bcdc6-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-138">Тип данных скрипта: **логическое значение**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-138">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-139">**Containment**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-139">**Containment**</span></span>
<span data-ttu-id="bcdc6-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-141">Массив **BSTR** , в котором каждый элемент является именем класса объекта, который может содержать этот класс.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-141">A **BSTR** array in which each element is the name of an object class that this class can contain.</span></span>

<dt>

<span data-ttu-id="bcdc6-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-143">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-143">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-144">**дериведфром**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-144">**DerivedFrom**</span></span>
<span data-ttu-id="bcdc6-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-146">Массив ADsPath строк, указывающий, из каких классов этот класс был производным.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-146">Array of ADsPath strings that indicate which classes this class was derived from.</span></span>

<dt>

<span data-ttu-id="bcdc6-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-148">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-148">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-149">**хелпфилеконтекст**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-149">**HelpFileContext**</span></span>
<span data-ttu-id="bcdc6-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-151">Идентификатор контекста в **хелпфиленаме** , где можно найти конкретные сведения для этого класса.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-151">Context ID inside **HelpFileName** where specific information for this class can be found.</span></span>

<dt>

<span data-ttu-id="bcdc6-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-153">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-153">Scripting data type: **long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-154">**хелпфиленаме**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-154">**HelpFileName**</span></span>
<span data-ttu-id="bcdc6-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-156">Имя файла справки, в котором содержатся дополнительные сведения об объектах этого класса.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-156">Name of a help file that contains more information about objects of this class.</span></span>

<dt>

<span data-ttu-id="bcdc6-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-158">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-158">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-159">**мандаторипропертиес**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-159">**MandatoryProperties**</span></span>
<span data-ttu-id="bcdc6-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-161">**SAFEARRAY** типа **Variant**, в котором перечислены свойства, которые должны быть заданы для записи этого класса в хранилище.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-161">**SAFEARRAY** of **VARIANT** s that lists the properties that must be set for this class to be written to storage.</span></span> <span data-ttu-id="bcdc6-162">Если класс содержит только одно свойство, **Get \_ мандаторипропертиес** будет возвращать **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-162">If the class only contains one property, then **get\_MandatoryProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="bcdc6-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-164">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-164">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-165">**намингпропертиес**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-165">**NamingProperties**</span></span>
<span data-ttu-id="bcdc6-166"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-166"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-167">**Массив SafeArray** типа **BSTR**, в котором перечислены свойства, используемые для именования атрибутов этого класса схемы.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-167">**SAFEARRAY** of **BSTR** s that lists the properties used to name attributes of this schema class.</span></span>

<dt>

<span data-ttu-id="bcdc6-168">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-169">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-169">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-170">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-170">**OID**</span></span>
<span data-ttu-id="bcdc6-171"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-171"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-172">Идентификатор объекта, зависящий от поставщика, который определяет этот класс.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-172">Provider-specific Object Identifier that defines this class.</span></span> <span data-ttu-id="bcdc6-173">Это обеспечивает расширение схемы с помощью Active Directory в службах каталогов, для которых требуются OID, зависящие от поставщика, для классов.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-173">This is provided to allow schema extension, using Active Directory, in directory services that require provider-specific OIDs for classes.</span></span>

<dt>

<span data-ttu-id="bcdc6-174">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-175">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-175">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-176">**OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-176">**OptionalProperties**</span></span>
<span data-ttu-id="bcdc6-177"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-177"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-178">**SAFEARRAY** типа **Variant**, в котором перечислены необязательные свойства данного класса схемы.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-178">**SAFEARRAY** of **VARIANT** s that lists the optional properties for this schema class.</span></span> <span data-ttu-id="bcdc6-179">Если класс содержит только одно свойство, **Get \_ OptionalProperties** будет возвращать **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-179">If the class only contains one property, then **get\_OptionalProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="bcdc6-180">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-181">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-181">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-182">**поссиблесупериорс**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-182">**PossibleSuperiors**</span></span>
<span data-ttu-id="bcdc6-183"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-183"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-184">Массив ADsPath строк, указывающий классы схемы, которые могут содержать экземпляры этого класса.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-184">Array of ADsPath strings that indicate the schema classes that can contain instances of this class.</span></span>

<dt>

<span data-ttu-id="bcdc6-185">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcdc6-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-186">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-186">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcdc6-187">**примаринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-187">**PrimaryInterface**</span></span>
<span data-ttu-id="bcdc6-188"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcdc6-188"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcdc6-189">Необязательный идентификатор GUID идентификатора, зависящего от поставщика, который связывает интерфейс с объектами этого класса схемы.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-189">Optional provider-specific identifier GUID that associates an interface to objects of this schema class.</span></span> <span data-ttu-id="bcdc6-190">Например, класс User, который поддерживает [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) и **примаринтерфаце** , определяется с помощью **IID \_ IADsUser**.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-190">For example, the "User" class that supports [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) and **PrimaryInterface** is identified by **IID\_IADsUser**.</span></span> <span data-ttu-id="bcdc6-191">Он должен иметь стандартный строковый формат GUID в соответствии с определением в COM.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-191">This must be in the standard string format of a GUID, as defined by COM.</span></span> <span data-ttu-id="bcdc6-192">Этот идентификатор GUID представляет собой значение, которое отображается в свойстве [**iAds:: Get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) в экземплярах этого класса для поставщиков, реализующих это свойство.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-192">This GUID is the value that appears in the [**IADs::get\_GUID**](/windows/desktop/api/Iads/nn-iads-iads) property in instances of this class for providers that implement this property.</span></span> <span data-ttu-id="bcdc6-193">Определение класса схемы по идентификатору IID основного интерфейса кода класса позволяет использовать **QueryInterface** во время выполнения, чтобы определить, имеет ли объект нужный класс.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-193">Identifying a schema class by IID of the class code's primary interface enables the use of **QueryInterface** at run time to determine whether an object is of the desired class.</span></span>

<dt>

<span data-ttu-id="bcdc6-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc6-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc6-195">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="bcdc6-196">Примеры</span><span class="sxs-lookup"><span data-stu-id="bcdc6-196">Examples</span></span>

<span data-ttu-id="bcdc6-197">В следующем примере кода показано, как использовать интерфейс [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) , чтобы определить, может ли объект быть контейнером, и, если да, выводит список имен всех содержащихся объектов.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-197">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



<span data-ttu-id="bcdc6-198">В следующем примере кода показано, как использовать интерфейс [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) , чтобы определить, может ли объект быть контейнером, и, если да, выводит список имен всех содержащихся объектов.</span><span class="sxs-lookup"><span data-stu-id="bcdc6-198">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="bcdc6-199">Требования</span><span class="sxs-lookup"><span data-stu-id="bcdc6-199">Requirements</span></span>



| <span data-ttu-id="bcdc6-200">Требование</span><span class="sxs-lookup"><span data-stu-id="bcdc6-200">Requirement</span></span> | <span data-ttu-id="bcdc6-201">Значение</span><span class="sxs-lookup"><span data-stu-id="bcdc6-201">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcdc6-202">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcdc6-202">Minimum supported client</span></span><br/> | <span data-ttu-id="bcdc6-203">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcdc6-203">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bcdc6-204">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcdc6-204">Minimum supported server</span></span><br/> | <span data-ttu-id="bcdc6-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcdc6-205">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bcdc6-206">Header</span><span class="sxs-lookup"><span data-stu-id="bcdc6-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcdc6-207"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc6-207"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="bcdc6-208">DLL</span><span class="sxs-lookup"><span data-stu-id="bcdc6-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcdc6-209"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc6-209"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="bcdc6-210">IID</span><span class="sxs-lookup"><span data-stu-id="bcdc6-210">IID</span></span><br/>                      | <span data-ttu-id="bcdc6-211">IID \_ иадскласс определен как C8F93DD0-4ae0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="bcdc6-211">IID\_IADsClass is defined as C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bcdc6-212">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcdc6-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcdc6-213">**иадскласс**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-213">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="bcdc6-214">**Иадскласс:: квалификаторы**</span><span class="sxs-lookup"><span data-stu-id="bcdc6-214">**IADsClass::Qualifiers**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





