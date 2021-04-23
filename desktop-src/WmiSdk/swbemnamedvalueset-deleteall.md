---
description: Метод DeleteAll объекта Свбемнамедвалуесет удаляет все именованные значения из коллекции, тем самым удаляя их.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: Свбемнамедвалуесет. DeleteAll, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264995"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a><span data-ttu-id="24692-103">Свбемнамедвалуесет. DeleteAll, метод</span><span class="sxs-lookup"><span data-stu-id="24692-103">SWbemNamedValueSet.DeleteAll method</span></span>

<span data-ttu-id="24692-104">Метод **DeleteAll** объекта [**свбемнамедвалуесет**](swbemnamedvalueset.md) удаляет все именованные значения из коллекции, тем самым удаляя их.</span><span class="sxs-lookup"><span data-stu-id="24692-104">The **DeleteAll** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object removes all named values from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="24692-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24692-105">Syntax</span></span>


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="24692-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24692-106">Parameters</span></span>

<span data-ttu-id="24692-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="24692-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24692-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24692-108">Return value</span></span>

<span data-ttu-id="24692-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="24692-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="24692-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="24692-110">Error codes</span></span>

<span data-ttu-id="24692-111">После завершения метода **DeleteAll** объект **Err** может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="24692-111">Upon completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="24692-112">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="24692-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="24692-113">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="24692-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24692-114">Требования</span><span class="sxs-lookup"><span data-stu-id="24692-114">Requirements</span></span>



| <span data-ttu-id="24692-115">Требование</span><span class="sxs-lookup"><span data-stu-id="24692-115">Requirement</span></span> | <span data-ttu-id="24692-116">Значение</span><span class="sxs-lookup"><span data-stu-id="24692-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24692-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24692-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24692-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24692-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24692-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24692-119">Minimum supported server</span></span><br/> | <span data-ttu-id="24692-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24692-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24692-121">Header</span><span class="sxs-lookup"><span data-stu-id="24692-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="24692-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="24692-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="24692-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="24692-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="24692-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="24692-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="24692-125">DLL</span><span class="sxs-lookup"><span data-stu-id="24692-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24692-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24692-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="24692-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="24692-127">CLSID</span></span><br/>                    | <span data-ttu-id="24692-128">\_СВБЕМНАМЕДВАЛУЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="24692-128">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="24692-129">IID</span><span class="sxs-lookup"><span data-stu-id="24692-129">IID</span></span><br/>                      | <span data-ttu-id="24692-130">IID \_ исвбемнамедвалуесет</span><span class="sxs-lookup"><span data-stu-id="24692-130">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="24692-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24692-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24692-132">**свбемнамедвалуесет**</span><span class="sxs-lookup"><span data-stu-id="24692-132">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> <dt>

[<span data-ttu-id="24692-133">**Свбемнамедвалуесет. Remove**</span><span class="sxs-lookup"><span data-stu-id="24692-133">**SWbemNamedValueSet.Remove**</span></span>](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




