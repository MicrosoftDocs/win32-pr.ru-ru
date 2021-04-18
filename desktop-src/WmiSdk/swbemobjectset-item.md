---
description: Метод Item объекта SWbemObjectSet получает объект SWbemObject из коллекции.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Метод SWbemObjectSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701948"
---
# <a name="swbemobjectsetitem-method"></a><span data-ttu-id="c9367-103">SWbemObjectSet. Item, метод</span><span class="sxs-lookup"><span data-stu-id="c9367-103">SWbemObjectSet.Item method</span></span>

<span data-ttu-id="c9367-104">Метод **Item** объекта [**SWbemObjectSet**](swbemobjectset.md) получает объект [**SWbemObject**](swbemobject.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="c9367-104">The **Item** method of the [**SWbemObjectSet**](swbemobjectset.md) object gets an [**SWbemObject**](swbemobject.md) from the collection.</span></span>

<span data-ttu-id="c9367-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c9367-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9367-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9367-106">Syntax</span></span>


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a><span data-ttu-id="c9367-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9367-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9367-108">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="c9367-108">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="c9367-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c9367-109">Required.</span></span> <span data-ttu-id="c9367-110">Относительный путь к объекту, который необходимо получить из коллекции.</span><span class="sxs-lookup"><span data-stu-id="c9367-110">Relative path of the object to retrieve from the collection.</span></span> <span data-ttu-id="c9367-111">Пример: Win32 \_ LogicalDisk = "C:"</span><span class="sxs-lookup"><span data-stu-id="c9367-111">Example: Win32\_LogicalDisk="C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9367-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9367-112">Return value</span></span>

<span data-ttu-id="c9367-113">В случае успешного выполнения запрошенный объект [**SWbemObject**](swbemobject.md) возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c9367-113">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c9367-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c9367-114">Error codes</span></span>

<span data-ttu-id="c9367-115">После завершения метода **Item** объект **Err** может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="c9367-115">Upon completion of the **Item** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="c9367-116">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c9367-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c9367-117">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c9367-117">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c9367-118">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c9367-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c9367-119">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="c9367-119">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="c9367-120">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c9367-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c9367-121">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="c9367-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c9367-122">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="c9367-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="c9367-123">Запрошенный элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="c9367-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9367-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9367-124">Remarks</span></span>

<span data-ttu-id="c9367-125">Метод **Item** может потребовать много времени процессора, поскольку для возврата результата требуется полное перечисление по поставщику элементов набора.</span><span class="sxs-lookup"><span data-stu-id="c9367-125">The **Item** method can require a lot of processor time because complete enumeration by the provider of the elements of the set is required to return the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9367-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c9367-126">Requirements</span></span>



| <span data-ttu-id="c9367-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c9367-127">Requirement</span></span> | <span data-ttu-id="c9367-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c9367-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9367-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9367-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9367-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9367-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9367-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9367-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9367-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9367-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9367-133">Header</span><span class="sxs-lookup"><span data-stu-id="c9367-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9367-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9367-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9367-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c9367-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="c9367-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c9367-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c9367-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c9367-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9367-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9367-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c9367-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="c9367-139">CLSID</span></span><br/>                    | <span data-ttu-id="c9367-140">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="c9367-140">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="c9367-141">IID</span><span class="sxs-lookup"><span data-stu-id="c9367-141">IID</span></span><br/>                      | <span data-ttu-id="c9367-142">IID \_ исвбемобжектсет</span><span class="sxs-lookup"><span data-stu-id="c9367-142">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




