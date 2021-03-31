---
description: Расширяет функциональные возможности SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Объект Свбемсервицесекс (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155818"
---
# <a name="swbemservicesex-object"></a><span data-ttu-id="c282c-103">Объект Свбемсервицесекс</span><span class="sxs-lookup"><span data-stu-id="c282c-103">SWbemServicesEx object</span></span>

<span data-ttu-id="c282c-104">Объект **свбемсервицесекс** расширяет функциональные возможности [**SwbemServices**](swbemservices.md).</span><span class="sxs-lookup"><span data-stu-id="c282c-104">The **SWbemServicesEx** object extends the functionality of [**SWbemServices**](swbemservices.md).</span></span> <span data-ttu-id="c282c-105">Методы [**помещения**](swbemservicesex-put.md) и [**путасинк**](swbemservicesex-putasync.md) позволяют сохранять класс или экземпляр в нескольких пространствах имен или в пространстве имен, отличном от того, где был создан экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c282c-105">The [**Put**](swbemservicesex-put.md) and [**PutAsync**](swbemservicesex-putasync.md) methods allow a class or an instance to be saved to multiple namespaces or to a different namespace than the one where an instance was created.</span></span> <span data-ttu-id="c282c-106">Не удается создать этот объект с [помощью вызова функции](/previous-versions//xzysf6hc(v=vs.85)) VBScript.</span><span class="sxs-lookup"><span data-stu-id="c282c-106">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="c282c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="c282c-107">Members</span></span>

<span data-ttu-id="c282c-108">Объект **свбемсервицесекс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c282c-108">The **SWbemServicesEx** object has these types of members:</span></span>

-   [<span data-ttu-id="c282c-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c282c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c282c-110">Методы</span><span class="sxs-lookup"><span data-stu-id="c282c-110">Methods</span></span>

<span data-ttu-id="c282c-111">Объект **свбемсервицесекс** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="c282c-111">The **SWbemServicesEx** object has these methods.</span></span>



| <span data-ttu-id="c282c-112">Метод</span><span class="sxs-lookup"><span data-stu-id="c282c-112">Method</span></span>                                       | <span data-ttu-id="c282c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c282c-113">Description</span></span>                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c282c-114">**PUT**</span><span class="sxs-lookup"><span data-stu-id="c282c-114">**Put**</span></span>](swbemservicesex-put.md)           | <span data-ttu-id="c282c-115">Сохраняет объект в пространство имен, привязанное к объекту **свбемсервицесекс** , и возвращает объект [**свбемобжектпас**](swbemobjectpath.md) , содержащий путь к объекту, в который были записаны данные.</span><span class="sxs-lookup"><span data-stu-id="c282c-115">Saves the object to the namespace bound to the **SWbemServicesEx** object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span><br/> |
| [<span data-ttu-id="c282c-116">**путасинк**</span><span class="sxs-lookup"><span data-stu-id="c282c-116">**PutAsync**</span></span>](swbemservicesex-putasync.md) | <span data-ttu-id="c282c-117">Асинхронно сохраняет объект в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="c282c-117">Saves an object asynchronously to a namespace.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="c282c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c282c-118">Remarks</span></span>

<span data-ttu-id="c282c-119">Методы в этом классе могут вызываться либо в режиме семисинчронаус, либо в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="c282c-119">The methods in this class can be called in either the semisynchronous mode or the asynchronous mode.</span></span> <span data-ttu-id="c282c-120">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c282c-120">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c282c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c282c-121">Requirements</span></span>



| <span data-ttu-id="c282c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c282c-122">Requirement</span></span> | <span data-ttu-id="c282c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c282c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c282c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c282c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c282c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c282c-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c282c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c282c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c282c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c282c-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c282c-128">Header</span><span class="sxs-lookup"><span data-stu-id="c282c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c282c-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c282c-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c282c-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c282c-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="c282c-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c282c-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c282c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c282c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c282c-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c282c-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c282c-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="c282c-134">CLSID</span></span><br/>                    | <span data-ttu-id="c282c-135">\_ИСВБЕМСЕРВИЦЕСЕКС CLSID</span><span class="sxs-lookup"><span data-stu-id="c282c-135">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="c282c-136">IID</span><span class="sxs-lookup"><span data-stu-id="c282c-136">IID</span></span><br/>                      | <span data-ttu-id="c282c-137">IID \_ исвбемсервицесекс</span><span class="sxs-lookup"><span data-stu-id="c282c-137">IID\_ISWbemServicesEx</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="c282c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c282c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c282c-139">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="c282c-139">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="c282c-140">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="c282c-140">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

