---
description: Метод Item объекта Свбемкуалифиерсет Возвращает именованный объект Свбемкуалифиер из коллекции. Это метод по умолчанию для этого объекта.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Метод Свбемкуалифиерсет. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913191"
---
# <a name="swbemqualifiersetitem-method"></a><span data-ttu-id="76b79-104">Свбемкуалифиерсет. Item, метод</span><span class="sxs-lookup"><span data-stu-id="76b79-104">SWbemQualifierSet.Item method</span></span>

<span data-ttu-id="76b79-105">Метод **Item** объекта [**свбемкуалифиерсет**](swbemqualifierset.md) Возвращает именованный объект [**свбемкуалифиер**](swbemqualifier.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="76b79-105">The **Item** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span> <span data-ttu-id="76b79-106">Это метод по умолчанию для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="76b79-106">This is the default method of this object.</span></span>

<span data-ttu-id="76b79-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="76b79-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76b79-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76b79-108">Syntax</span></span>


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="76b79-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="76b79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76b79-110">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76b79-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76b79-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="76b79-111">Required.</span></span> <span data-ttu-id="76b79-112">Имя извлекаемого описателя.</span><span class="sxs-lookup"><span data-stu-id="76b79-112">Name of the qualifier to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="76b79-113">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="76b79-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76b79-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="76b79-114">Reserved.</span></span> <span data-ttu-id="76b79-115">Значение по умолчанию — 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="76b79-115">The default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76b79-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76b79-116">Return value</span></span>

<span data-ttu-id="76b79-117">В случае успешного выполнения возвращается запрошенный объект [**свбемкуалифиер**](swbemqualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="76b79-117">If successful, the requested [**SWbemQualifier**](swbemqualifier.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="76b79-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="76b79-118">Error codes</span></span>

<span data-ttu-id="76b79-119">После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="76b79-119">After completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="76b79-120">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="76b79-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="76b79-121">Недопустимый параметр *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="76b79-121">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="76b79-122">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="76b79-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="76b79-123">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="76b79-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="76b79-124">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="76b79-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="76b79-125">Указанный квалификатор не существует.</span><span class="sxs-lookup"><span data-stu-id="76b79-125">Specified qualifier does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76b79-126">Требования</span><span class="sxs-lookup"><span data-stu-id="76b79-126">Requirements</span></span>



| <span data-ttu-id="76b79-127">Требование</span><span class="sxs-lookup"><span data-stu-id="76b79-127">Requirement</span></span> | <span data-ttu-id="76b79-128">Значение</span><span class="sxs-lookup"><span data-stu-id="76b79-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76b79-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76b79-129">Minimum supported client</span></span><br/> | <span data-ttu-id="76b79-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76b79-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76b79-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76b79-131">Minimum supported server</span></span><br/> | <span data-ttu-id="76b79-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76b79-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76b79-133">Header</span><span class="sxs-lookup"><span data-stu-id="76b79-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="76b79-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="76b79-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="76b79-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="76b79-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="76b79-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76b79-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76b79-137">DLL</span><span class="sxs-lookup"><span data-stu-id="76b79-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76b79-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76b79-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="76b79-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="76b79-139">CLSID</span></span><br/>                    | <span data-ttu-id="76b79-140">\_СВБЕМКУАЛИФИЕРСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="76b79-140">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="76b79-141">IID</span><span class="sxs-lookup"><span data-stu-id="76b79-141">IID</span></span><br/>                      | <span data-ttu-id="76b79-142">IID \_ исвбемкуалифиерсет</span><span class="sxs-lookup"><span data-stu-id="76b79-142">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="76b79-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76b79-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76b79-144">**свбемкуалифиерсет**</span><span class="sxs-lookup"><span data-stu-id="76b79-144">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="76b79-145">**свбемкуалифиер**</span><span class="sxs-lookup"><span data-stu-id="76b79-145">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

 




