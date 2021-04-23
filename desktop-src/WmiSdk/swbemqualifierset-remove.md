---
description: Метод Remove объекта Свбемкуалифиерсет удаляет именованный квалификатор из коллекции.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Метод Свбемкуалифиерсет. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544655"
---
# <a name="swbemqualifiersetremove-method"></a><span data-ttu-id="4cefb-103">Свбемкуалифиерсет. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="4cefb-103">SWbemQualifierSet.Remove method</span></span>

<span data-ttu-id="4cefb-104">Метод **Remove** объекта [**свбемкуалифиерсет**](swbemqualifierset.md) удаляет именованный квалификатор из коллекции.</span><span class="sxs-lookup"><span data-stu-id="4cefb-104">The **Remove** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object deletes a named qualifier from the collection.</span></span>

<span data-ttu-id="4cefb-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4cefb-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4cefb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cefb-106">Syntax</span></span>


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4cefb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cefb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cefb-108">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cefb-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cefb-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4cefb-109">Required.</span></span> <span data-ttu-id="4cefb-110">Имя удаляемого квалификатора.</span><span class="sxs-lookup"><span data-stu-id="4cefb-110">Name of the qualifier to remove.</span></span>

</dd> <dt>

<span data-ttu-id="4cefb-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4cefb-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cefb-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4cefb-112">Reserved.</span></span> <span data-ttu-id="4cefb-113">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="4cefb-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cefb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cefb-114">Return value</span></span>

<span data-ttu-id="4cefb-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4cefb-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4cefb-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4cefb-116">Error codes</span></span>

<span data-ttu-id="4cefb-117">После завершения метода **Remove** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="4cefb-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4cefb-118">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4cefb-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4cefb-119">Недопустимый параметр *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="4cefb-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4cefb-120">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4cefb-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4cefb-121">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4cefb-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4cefb-122">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="4cefb-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="4cefb-123">Указанный квалификатор не существует.</span><span class="sxs-lookup"><span data-stu-id="4cefb-123">Specified qualifier does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="4cefb-124">**вбемерринвалидоператион** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="4cefb-124">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="4cefb-125">Удаление этого квалификатора недопустимо.</span><span class="sxs-lookup"><span data-stu-id="4cefb-125">Removing this qualifier is illegal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cefb-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cefb-126">Remarks</span></span>

<span data-ttu-id="4cefb-127">Невозможно выполнить итерацию коллекции при удалении элементов, так как при удалении элемента из коллекции указатель коллекции перемещается к следующему элементу.</span><span class="sxs-lookup"><span data-stu-id="4cefb-127">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="4cefb-128">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="4cefb-128">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cefb-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4cefb-129">Requirements</span></span>



| <span data-ttu-id="4cefb-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4cefb-130">Requirement</span></span> | <span data-ttu-id="4cefb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4cefb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cefb-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cefb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4cefb-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cefb-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4cefb-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cefb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4cefb-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cefb-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4cefb-136">Header</span><span class="sxs-lookup"><span data-stu-id="4cefb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cefb-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cefb-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cefb-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4cefb-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="4cefb-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4cefb-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4cefb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4cefb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cefb-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cefb-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4cefb-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="4cefb-142">CLSID</span></span><br/>                    | <span data-ttu-id="4cefb-143">\_СВБЕМКУАЛИФИЕРСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="4cefb-143">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="4cefb-144">IID</span><span class="sxs-lookup"><span data-stu-id="4cefb-144">IID</span></span><br/>                      | <span data-ttu-id="4cefb-145">IID \_ исвбемкуалифиерсет</span><span class="sxs-lookup"><span data-stu-id="4cefb-145">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="4cefb-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cefb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cefb-147">**свбемкуалифиерсет**</span><span class="sxs-lookup"><span data-stu-id="4cefb-147">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="4cefb-148">**Свбемкуалифиерсет. Add**</span><span class="sxs-lookup"><span data-stu-id="4cefb-148">**SWbemQualifierSet.Add**</span></span>](swbemqualifierset-add.md)
</dt> </dl>

 

 




