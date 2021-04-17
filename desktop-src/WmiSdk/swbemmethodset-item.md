---
description: Метод Item объекта Свбеммесодсет Возвращает именованный объект Свбеммесод из коллекции.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Метод Свбеммесодсет. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692699"
---
# <a name="swbemmethodsetitem-method"></a><span data-ttu-id="a197b-103">Свбеммесодсет. Item, метод</span><span class="sxs-lookup"><span data-stu-id="a197b-103">SWbemMethodSet.Item method</span></span>

<span data-ttu-id="a197b-104">Метод **Item** объекта [**свбеммесодсет**](swbemmethodset.md) Возвращает именованный объект [**свбеммесод**](swbemmethod.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="a197b-104">The **Item** method of the [**SWbemMethodSet**](swbemmethodset.md) object returns a named [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span>

<span data-ttu-id="a197b-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a197b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a197b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a197b-106">Syntax</span></span>


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a197b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a197b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a197b-108">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a197b-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a197b-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a197b-109">Required.</span></span> <span data-ttu-id="a197b-110">Имя извлекаемого метода.</span><span class="sxs-lookup"><span data-stu-id="a197b-110">Name of the method to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a197b-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a197b-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a197b-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a197b-112">Reserved.</span></span> <span data-ttu-id="a197b-113">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="a197b-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a197b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a197b-114">Return value</span></span>

<span data-ttu-id="a197b-115">В случае успешного выполнения запрошенный объект [**свбеммесод**](swbemmethod.md) возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a197b-115">If successful, the requested [**SWbemMethod**](swbemmethod.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a197b-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a197b-116">Error codes</span></span>

<span data-ttu-id="a197b-117">После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="a197b-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a197b-118">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a197b-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a197b-119">Недопустимый параметр *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="a197b-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a197b-120">**вбемеррфаилед** -2147749894</span><span class="sxs-lookup"><span data-stu-id="a197b-120">**wbemErrFailed** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="a197b-121">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a197b-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a197b-122">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="a197b-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="a197b-123">Указанный метод не существует.</span><span class="sxs-lookup"><span data-stu-id="a197b-123">The specified method does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a197b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a197b-124">Requirements</span></span>



| <span data-ttu-id="a197b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a197b-125">Requirement</span></span> | <span data-ttu-id="a197b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a197b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a197b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a197b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a197b-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a197b-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a197b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a197b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a197b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a197b-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a197b-131">Header</span><span class="sxs-lookup"><span data-stu-id="a197b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a197b-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a197b-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a197b-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a197b-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="a197b-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a197b-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a197b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a197b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a197b-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a197b-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a197b-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="a197b-137">CLSID</span></span><br/>                    | <span data-ttu-id="a197b-138">\_СВБЕММЕСОДСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="a197b-138">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="a197b-139">IID</span><span class="sxs-lookup"><span data-stu-id="a197b-139">IID</span></span><br/>                      | <span data-ttu-id="a197b-140">IID \_ исвбеммесодсет</span><span class="sxs-lookup"><span data-stu-id="a197b-140">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="a197b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a197b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a197b-142">**свбеммесодсет**</span><span class="sxs-lookup"><span data-stu-id="a197b-142">**SWbemMethodSet**</span></span>](swbemmethodset.md)
</dt> <dt>

[<span data-ttu-id="a197b-143">**свбеммесод**</span><span class="sxs-lookup"><span data-stu-id="a197b-143">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> </dl>

 

 




