---
description: Свойство Path \_ объекта SWbemObject возвращает объект свбемобжектпас, представляющий путь к объекту текущего класса или экземпляра. Это свойство можно передать в качестве параметра методам, которым требуется путь к объекту.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: Свойство SWbemObject.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265181"
---
# <a name="swbemobjectpath_-property"></a><span data-ttu-id="95181-104">SWbemObject. Path, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="95181-104">SWbemObject.Path\_ property</span></span>

<span data-ttu-id="95181-105">Свойство **path \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**свбемобжектпас**](swbemobjectpath.md) , представляющий путь к объекту текущего класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="95181-105">The **Path\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="95181-106">Это свойство можно передать в качестве параметра методам, которым требуется путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="95181-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="95181-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="95181-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="95181-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="95181-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95181-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95181-109">Syntax</span></span>


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="95181-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="95181-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="95181-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95181-111">Remarks</span></span>

<span data-ttu-id="95181-112">Можно изменить только свойство [**Class**](swbemobjectpath-class.md) возвращаемого экземпляра [**свбемобжектпас**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="95181-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="95181-113">Если вы попытаетесь изменить какое-либо другое свойство или попытаетесь вызвать методы [**сетаскласс**](swbemobjectpath-setasclass.md) или [**сетассинглетон**](swbemobjectpath-setassingleton.md), вы получите ошибку **вбемеррреадонли** .</span><span class="sxs-lookup"><span data-stu-id="95181-113">If you try to modify any other property, or try to call the methods [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md), you will get a **wbemErrReadOnly** error.</span></span>

<span data-ttu-id="95181-114">Поэтому нельзя изменить объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который является значением свойства [**Keys**](swbemobjectpath-keys.md) возвращаемого экземпляра [**свбемобжектпас**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="95181-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="95181-115">Если вы попытаетесь вызвать методы [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)или [**DeleteAll**](swbemnamedvalueset-deleteall.md) для этого значения, вы получите ошибку вбемеррреадонли.</span><span class="sxs-lookup"><span data-stu-id="95181-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you will get a wbemErrReadOnly error.</span></span> <span data-ttu-id="95181-116">Кроме того, нельзя изменить любые [**свбемнамедвалуе**](swbemnamedvalue.md) , полученные из этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="95181-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="95181-117">Попытки изменить свойство **value** возвращают тот же код ошибки.</span><span class="sxs-lookup"><span data-stu-id="95181-117">Attempts to modify the **Value** property return the same error code.</span></span>

<span data-ttu-id="95181-118">Однако при вызове [**SWbemObject. Clone \_**](swbemobject-clone-.md) для создания копии свойство [**свбемобжектпас. Path**](swbemobjectpath-path.md) копии становится полностью изменяемым.</span><span class="sxs-lookup"><span data-stu-id="95181-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**SWbemObjectPath.Path**](swbemobjectpath-path.md) property of the copy is fully modifiable.</span></span>

## <a name="examples"></a><span data-ttu-id="95181-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="95181-119">Examples</span></span>

<span data-ttu-id="95181-120">Следующий пример кода, взятый из [списка всех классов WMI cimV2](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) в коллекции TechNet, использует \_ свойство Path для ПЕРЕЧИСЛЕНИЯ всех классов WMI cimV2.</span><span class="sxs-lookup"><span data-stu-id="95181-120">The following code sample, taken from [List All the WMI cimV2 Classes](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in the TechNet Gallery, uses the Path\_ property to list all the WMI cimV2 classes.</span></span>


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a><span data-ttu-id="95181-121">Требования</span><span class="sxs-lookup"><span data-stu-id="95181-121">Requirements</span></span>



| <span data-ttu-id="95181-122">Требование</span><span class="sxs-lookup"><span data-stu-id="95181-122">Requirement</span></span> | <span data-ttu-id="95181-123">Значение</span><span class="sxs-lookup"><span data-stu-id="95181-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95181-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95181-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95181-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95181-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95181-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95181-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95181-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95181-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95181-128">Header</span><span class="sxs-lookup"><span data-stu-id="95181-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95181-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95181-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="95181-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="95181-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="95181-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="95181-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="95181-132">DLL</span><span class="sxs-lookup"><span data-stu-id="95181-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95181-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95181-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="95181-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="95181-134">CLSID</span></span><br/>                    | <span data-ttu-id="95181-135">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="95181-135">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="95181-136">IID</span><span class="sxs-lookup"><span data-stu-id="95181-136">IID</span></span><br/>                      | <span data-ttu-id="95181-137">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="95181-137">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




