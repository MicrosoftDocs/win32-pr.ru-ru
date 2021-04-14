---
description: Метод Add объекта Свбемкуалифиерсет добавляет объект Свбемкуалифиер в коллекцию Свбемкуалифиерсет. Если квалификатор с таким именем уже существует в коллекции, он будет заменен.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Метод Свбемкуалифиерсет. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349202"
---
# <a name="swbemqualifiersetadd-method"></a><span data-ttu-id="e2b3f-104">Свбемкуалифиерсет. Add, метод</span><span class="sxs-lookup"><span data-stu-id="e2b3f-104">SWbemQualifierSet.Add method</span></span>

<span data-ttu-id="e2b3f-105">Метод **Add** объекта [**Свбемкуалифиерсет**](swbemqualifierset.md) добавляет объект [**свбемкуалифиер**](swbemqualifier.md) в коллекцию **свбемкуалифиерсет** .</span><span class="sxs-lookup"><span data-stu-id="e2b3f-105">The **Add** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span> <span data-ttu-id="e2b3f-106">Если квалификатор с таким именем уже существует в коллекции, он будет заменен.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-106">If a qualifier with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="e2b3f-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e2b3f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b3f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2b3f-108">Syntax</span></span>


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e2b3f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2b3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b3f-110">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2b3f-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-111">Required.</span></span> <span data-ttu-id="e2b3f-112">Имя нового квалификатора.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-112">Name of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-113">*варвал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2b3f-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-114">Required.</span></span> <span data-ttu-id="e2b3f-115">Значение Variant нового квалификатора.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-115">Variant value of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-116">*бпропагатестосубклассес* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e2b3f-116">*bPropagatesToSubclasses* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-117">Логическое значение, указывающее, распространяется ли новый квалификатор на подклассы.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-117">Boolean value that indicates if this new qualifier is propagated to subclasses.</span></span> <span data-ttu-id="e2b3f-118">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-118">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-119">*бпропагатестоинстанцес* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e2b3f-119">*bPropagatesToInstances* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-120">Логическое значение, указывающее, распространяется ли новый квалификатор на экземпляры.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-120">Boolean value that indicates if this new qualifier is propagated to instances.</span></span> <span data-ttu-id="e2b3f-121">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-121">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-122">*боверридабле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e2b3f-122">*bOverridable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-123">Логическое значение, указывающее, можно ли переопределить этот квалификатор при распространении.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span> <span data-ttu-id="e2b3f-124">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-124">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-125">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e2b3f-125">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-126">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-126">Reserved.</span></span> <span data-ttu-id="e2b3f-127">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-127">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b3f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2b3f-128">Return value</span></span>

<span data-ttu-id="e2b3f-129">В случае успеха этот метод возвращает объект [**свбемкуалифиер**](swbemqualifier.md) , представляющий новый квалификатор.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-129">If successful, this method returns an [**SWbemQualifier**](swbemqualifier.md) object that represents the new qualifier.</span></span> <span data-ttu-id="e2b3f-130">В противном случае возвращается **пустой** объект.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-130">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e2b3f-131">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e2b3f-131">Error codes</span></span>

<span data-ttu-id="e2b3f-132">После завершения метода **Add** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-132">After completion of the **Add** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e2b3f-133">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e2b3f-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-134">Недопустимый параметр *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="e2b3f-134">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-135">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e2b3f-135">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-136">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-137">**вбемеррканнотбекэй** -2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="e2b3f-137">**wbemErrCannotBeKey** - 2147749919 (0x8004101F)</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-138">Недопустимая попытка указать квалификатор **ключа** для свойства, которое не может быть ключом.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-138">There was an illegal attempt to specify a **Key** qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="e2b3f-139">Ключи указываются в определении класса объекта и не могут быть изменены для каждого отдельного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-139">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-140">**вбемерринвалидкуалифиертипе** -2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="e2b3f-140">**wbemErrInvalidQualifierType** - 2147749929 (0x80041029)</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-141">Параметр *варвал* не является допустимым типом квалификатора.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-141">The *varVal* parameter is not of a legal qualifier type.</span></span>

</dd> <dt>

<span data-ttu-id="e2b3f-142">**вбемерроверриденоталловед** -2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="e2b3f-142">**wbemErrOverrideNotAllowed** - 2147749914 (0x8004101A)</span></span>
</dt> <dd>

<span data-ttu-id="e2b3f-143">Невозможно выполнить операцию **свбемкуалифиерсет. Add** над этим квалификатором, так как объект-владелец не допускает переопределения.</span><span class="sxs-lookup"><span data-stu-id="e2b3f-143">It is not possible to perform the **SWbemQualifierSet.Add** operation on this qualifier because the owning object does not permit overrides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2b3f-144">Требования</span><span class="sxs-lookup"><span data-stu-id="e2b3f-144">Requirements</span></span>



| <span data-ttu-id="e2b3f-145">Требование</span><span class="sxs-lookup"><span data-stu-id="e2b3f-145">Requirement</span></span> | <span data-ttu-id="e2b3f-146">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b3f-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b3f-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2b3f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b3f-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2b3f-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2b3f-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2b3f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b3f-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2b3f-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2b3f-151">Header</span><span class="sxs-lookup"><span data-stu-id="e2b3f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2b3f-152"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2b3f-152"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2b3f-153">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e2b3f-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2b3f-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2b3f-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2b3f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="e2b3f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2b3f-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2b3f-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e2b3f-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="e2b3f-157">CLSID</span></span><br/>                    | <span data-ttu-id="e2b3f-158">\_СВБЕМКУАЛИФИЕРСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="e2b3f-158">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="e2b3f-159">IID</span><span class="sxs-lookup"><span data-stu-id="e2b3f-159">IID</span></span><br/>                      | <span data-ttu-id="e2b3f-160">IID \_ исвбемкуалифиерсет</span><span class="sxs-lookup"><span data-stu-id="e2b3f-160">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="e2b3f-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2b3f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b3f-162">**свбемкуалифиерсет**</span><span class="sxs-lookup"><span data-stu-id="e2b3f-162">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="e2b3f-163">**Свбемкуалифиерсет. Remove**</span><span class="sxs-lookup"><span data-stu-id="e2b3f-163">**SWbemQualifierSet.Remove**</span></span>](swbemqualifierset-remove.md)
</dt> </dl>

 

 




