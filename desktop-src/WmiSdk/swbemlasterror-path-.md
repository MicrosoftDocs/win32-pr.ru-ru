---
description: Свойство Path \_ объекта свбемластеррор возвращает объект свбемобжектпас, представляющий путь к объекту текущего класса или экземпляра. Это свойство можно передать в качестве параметра методам, которым требуется путь к объекту.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: Свойство SWbemLastError.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081002"
---
# <a name="swbemlasterrorpath_-property"></a><span data-ttu-id="e095a-104">Свбемластеррор. Path, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="e095a-104">SWbemLastError.Path\_ property</span></span>

<span data-ttu-id="e095a-105">Свойство **path \_** объекта [**свбемластеррор**](swbemlasterror.md) возвращает объект [**свбемобжектпас**](swbemobjectpath.md) , представляющий путь к объекту текущего класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e095a-105">The **Path\_** property of the [**SWbemLastError**](swbemlasterror.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="e095a-106">Это свойство можно передать в качестве параметра методам, которым требуется путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="e095a-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="e095a-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e095a-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e095a-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e095a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e095a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e095a-109">Syntax</span></span>


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="e095a-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e095a-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e095a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e095a-111">Remarks</span></span>

<span data-ttu-id="e095a-112">Можно изменить только свойство [**Class**](swbemobjectpath-class.md) возвращаемого экземпляра [**свбемобжектпас**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="e095a-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="e095a-113">При попытке изменить любое другое свойство или попытаться вызвать методы [**сетаскласс**](swbemobjectpath-setasclass.md) или [**Сетассинглетон**](swbemobjectpath-setassingleton.md) возникает ошибка **вбемеррреадонли**.</span><span class="sxs-lookup"><span data-stu-id="e095a-113">If you try to modify any other property, or try to call the [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md) methods, you get an error of **wbemErrReadOnly**.</span></span>

<span data-ttu-id="e095a-114">Поэтому нельзя изменить объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который является значением свойства [**Keys**](swbemobjectpath-keys.md) возвращаемого экземпляра [**свбемобжектпас**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="e095a-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="e095a-115">При попытке вызова метода [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)или [**DeleteAll**](swbemnamedvalueset-deleteall.md) для этого значения возникает ошибка **вбемеррреадонли** .</span><span class="sxs-lookup"><span data-stu-id="e095a-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you get a **wbemErrReadOnly** error.</span></span> <span data-ttu-id="e095a-116">Кроме того, нельзя изменить любые [**свбемнамедвалуе**](swbemnamedvalue.md) , полученные из этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="e095a-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="e095a-117">Попытки изменить свойство [**value**](swbemnamedvalue-value.md) возвращают тот же код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e095a-117">Attempts to modify the [**Value**](swbemnamedvalue-value.md) property return the same error code.</span></span>

<span data-ttu-id="e095a-118">Однако при вызове [**SWbemObject. Clone \_**](swbemobject-clone-.md) для создания копии свойство [**path \_**](swbemobject-path-.md) копии будет полностью изменяемым.</span><span class="sxs-lookup"><span data-stu-id="e095a-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**Path\_**](swbemobject-path-.md) property of the copy is fully modifiable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e095a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e095a-119">Requirements</span></span>



| <span data-ttu-id="e095a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e095a-120">Requirement</span></span> | <span data-ttu-id="e095a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e095a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e095a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e095a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e095a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e095a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e095a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e095a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e095a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e095a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e095a-126">Header</span><span class="sxs-lookup"><span data-stu-id="e095a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e095a-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e095a-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e095a-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e095a-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="e095a-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e095a-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e095a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e095a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e095a-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e095a-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e095a-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="e095a-132">CLSID</span></span><br/>                    | <span data-ttu-id="e095a-133">\_СВБЕМЛАСТЕРРОР CLSID</span><span class="sxs-lookup"><span data-stu-id="e095a-133">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="e095a-134">IID</span><span class="sxs-lookup"><span data-stu-id="e095a-134">IID</span></span><br/>                      | <span data-ttu-id="e095a-135">IID \_ исвбемластеррор</span><span class="sxs-lookup"><span data-stu-id="e095a-135">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




