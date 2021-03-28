---
description: Расширяет объект IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Объект IShellDispatch3 (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984664"
---
# <a name="ishelldispatch3-object"></a><span data-ttu-id="ecb16-103">Объект IShellDispatch3</span><span class="sxs-lookup"><span data-stu-id="ecb16-103">IShellDispatch3 object</span></span>

<span data-ttu-id="ecb16-104">Расширяет объект [**IShellDispatch2**](ishelldispatch2-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ecb16-104">Extends the [**IShellDispatch2**](ishelldispatch2-object.md) object.</span></span> <span data-ttu-id="ecb16-105">**IShellDispatch3** поддерживает один новый метод в дополнение к свойствам и методам, поддерживаемым **IShellDispatch2**.</span><span class="sxs-lookup"><span data-stu-id="ecb16-105">**IShellDispatch3** supports one new method in addition to the properties and methods supported by **IShellDispatch2**.</span></span>

> [!Note]  
> <span data-ttu-id="ecb16-106">**IShellDispatch3** реализован и доступен через объект [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="ecb16-106">**IShellDispatch3** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="ecb16-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="ecb16-107">Members</span></span>

<span data-ttu-id="ecb16-108">Объект **IShellDispatch3** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ecb16-108">The **IShellDispatch3** object has these types of members:</span></span>

-   [<span data-ttu-id="ecb16-109">Методы</span><span class="sxs-lookup"><span data-stu-id="ecb16-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ecb16-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ecb16-110">Methods</span></span>

<span data-ttu-id="ecb16-111">Объект **IShellDispatch3** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="ecb16-111">The **IShellDispatch3** object has these methods.</span></span>



| <span data-ttu-id="ecb16-112">Метод</span><span class="sxs-lookup"><span data-stu-id="ecb16-112">Method</span></span>                                             | <span data-ttu-id="ecb16-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ecb16-113">Description</span></span>                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="ecb16-114">**аддторецент**</span><span class="sxs-lookup"><span data-stu-id="ecb16-114">**AddToRecent**</span></span>](ishelldispatch3-addtorecent.md) | <span data-ttu-id="ecb16-115">Добавляет файл в список последних использованных файлов (MRU).</span><span class="sxs-lookup"><span data-stu-id="ecb16-115">Adds a file to the most recently used (MRU) list.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ecb16-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecb16-116">Remarks</span></span>

<span data-ttu-id="ecb16-117">Обсуждение служб Windows см. в документации по [службам](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="ecb16-117">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb16-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ecb16-118">Requirements</span></span>



| <span data-ttu-id="ecb16-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ecb16-119">Requirement</span></span> | <span data-ttu-id="ecb16-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ecb16-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb16-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecb16-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb16-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ecb16-122">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ecb16-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecb16-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb16-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ecb16-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ecb16-125">Header</span><span class="sxs-lookup"><span data-stu-id="ecb16-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecb16-126"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb16-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ecb16-127">IDL</span><span class="sxs-lookup"><span data-stu-id="ecb16-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ecb16-128"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ecb16-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ecb16-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb16-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecb16-130"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb16-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb16-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecb16-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb16-132">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ecb16-132">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="ecb16-133">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="ecb16-133">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="ecb16-134">**ишеллдиспатч**</span><span class="sxs-lookup"><span data-stu-id="ecb16-134">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="ecb16-135">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="ecb16-135">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> </dl>

 

 
