---
description: Свойство Parameters объекта Свбеммесод — это объект SWbemObject, свойства которого определяют выходные параметры и тип возвращаемого значения этого метода. Это свойство доступно только для чтения.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Свойство Свбеммесод. parameters (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693221"
---
# <a name="swbemmethodoutparameters-property"></a><span data-ttu-id="1d2dd-104">Свбеммесод. Parameters, свойство</span><span class="sxs-lookup"><span data-stu-id="1d2dd-104">SWbemMethod.OutParameters property</span></span>

<span data-ttu-id="1d2dd-105">Свойство **Parameters** объекта [**свбеммесод**](swbemmethod.md) — это объект [**SWbemObject**](swbemobject.md) , свойства которого определяют выходные параметры и тип возвращаемого значения этого метода.</span><span class="sxs-lookup"><span data-stu-id="1d2dd-105">The **OutParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span> <span data-ttu-id="1d2dd-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1d2dd-106">This property is read-only.</span></span>

<span data-ttu-id="1d2dd-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1d2dd-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="1d2dd-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1d2dd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2dd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d2dd-109">Syntax</span></span>


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="1d2dd-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1d2dd-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="1d2dd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d2dd-111">Remarks</span></span>

<span data-ttu-id="1d2dd-112">Дополнительные сведения об использовании этого свойства для получения выходных параметров из методов поставщика см. в разделе [конструирование объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1d2dd-112">For more information about how to use this property to obtain output parameters from provider methods, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="1d2dd-113">Обратите внимание, что любые изменения, внесенные в этот объект, не отражаются в определении базового метода.</span><span class="sxs-lookup"><span data-stu-id="1d2dd-113">Note that any changes made to this object are not reflected in the underlying method definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2dd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1d2dd-114">Requirements</span></span>



| <span data-ttu-id="1d2dd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1d2dd-115">Requirement</span></span> | <span data-ttu-id="1d2dd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1d2dd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2dd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d2dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2dd-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d2dd-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d2dd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d2dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2dd-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d2dd-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d2dd-121">Header</span><span class="sxs-lookup"><span data-stu-id="1d2dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d2dd-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d2dd-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d2dd-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1d2dd-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d2dd-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1d2dd-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1d2dd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1d2dd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d2dd-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2dd-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d2dd-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="1d2dd-127">CLSID</span></span><br/>                    | <span data-ttu-id="1d2dd-128">\_СВБЕММЕСОД CLSID</span><span class="sxs-lookup"><span data-stu-id="1d2dd-128">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="1d2dd-129">IID</span><span class="sxs-lookup"><span data-stu-id="1d2dd-129">IID</span></span><br/>                      | <span data-ttu-id="1d2dd-130">IID \_ исвбеммесод</span><span class="sxs-lookup"><span data-stu-id="1d2dd-130">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="1d2dd-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d2dd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2dd-132">**свбеммесод**</span><span class="sxs-lookup"><span data-stu-id="1d2dd-132">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="1d2dd-133">**SWbemObject.ExeКмесод\_**</span><span class="sxs-lookup"><span data-stu-id="1d2dd-133">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="1d2dd-134">**SWbemObject.ExeКмесодасинк\_**</span><span class="sxs-lookup"><span data-stu-id="1d2dd-134">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="1d2dd-135">**SWbemServices.ExeКмесод**</span><span class="sxs-lookup"><span data-stu-id="1d2dd-135">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="1d2dd-136">**SWbemServices.ExeКмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="1d2dd-136">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




