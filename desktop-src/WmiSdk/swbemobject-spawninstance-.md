---
description: Используйте метод Спавнинстанце \_ объекта SWbemObject для создания нового экземпляра класса.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Метод SWbemObject.SpawnInstance_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272564"
---
# <a name="swbemobjectspawninstance_-method"></a><span data-ttu-id="68227-103">SWbemObject. Спавнинстанце, \_ метод</span><span class="sxs-lookup"><span data-stu-id="68227-103">SWbemObject.SpawnInstance\_ method</span></span>

<span data-ttu-id="68227-104">Используйте метод **спавнинстанце \_** объекта [**SWbemObject**](swbemobject.md) для создания нового экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="68227-104">Use the **SpawnInstance\_** method of the [**SWbemObject**](swbemobject.md) object to create a new instance of a class.</span></span> <span data-ttu-id="68227-105">Текущий объект должен быть определением класса, полученным от WMI с помощью метода, такого как [**SwbemServices. Get**](swbemservices-get.md) или [**SWbemServices.Exeккуери**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="68227-105">The current object must be a class definition obtained from WMI via a method such as [**SWbemServices.Get**](swbemservices-get.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="68227-106">Затем используйте это определение класса для создания новых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="68227-106">Then, use this class definition to create new instances.</span></span> <span data-ttu-id="68227-107">Создайте каждый новый экземпляр локально в процессе, а затем вызовите метод [**SWbemObject. \_**](swbemobject-put-.md) Create, чтобы создать экземпляр в WMI.</span><span class="sxs-lookup"><span data-stu-id="68227-107">Create each new instance locally within the process, and then call [**SWbemObject.Put\_**](swbemobject-put-.md) to actually create the instance within WMI.</span></span>

> [!Note]  
> <span data-ttu-id="68227-108">Порождение экземпляра из экземпляра поддерживается, но возвращаемый экземпляр пуст.</span><span class="sxs-lookup"><span data-stu-id="68227-108">Spawning an instance from an instance is supported, but the returned instance is empty.</span></span>

 

<span data-ttu-id="68227-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="68227-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68227-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68227-110">Syntax</span></span>


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="68227-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="68227-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68227-112">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="68227-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68227-113">Зарезервировано и должно быть равно нулю, если указано.</span><span class="sxs-lookup"><span data-stu-id="68227-113">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68227-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68227-114">Return value</span></span>

<span data-ttu-id="68227-115">В случае успеха этот вызов возвращает объект [**SWbemObject**](swbemobject.md) , содержащий новый экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="68227-115">If successful, this call returns an [**SWbemObject**](swbemobject.md) object that contains a new instance of the class.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68227-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="68227-116">Error codes</span></span>

<span data-ttu-id="68227-117">После завершения метода **спавнинстанце \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="68227-117">After the completion of the **SpawnInstance\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="68227-118">**вбемерринкомплетекласс** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="68227-118">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="68227-119">Текущий объект не является допустимым определением класса и не может создавать новые экземпляры.</span><span class="sxs-lookup"><span data-stu-id="68227-119">Current object is not a valid class definition, and it cannot spawn new instances.</span></span> <span data-ttu-id="68227-120">Либо он неполон, либо он не был зарегистрирован в WMI с помощью [**SWbemObject. \_ постановки**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="68227-120">Either it is incomplete, or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>

</dd> <dt>

<span data-ttu-id="68227-121">**вбемерриллегалоператион** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="68227-121">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="68227-122">Возвращается, если этот метод используется в экземпляре, а не в классе.</span><span class="sxs-lookup"><span data-stu-id="68227-122">Returned if this method is used on an instance instead of a class.</span></span>

</dd> <dt>

<span data-ttu-id="68227-123">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="68227-123">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="68227-124">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="68227-124">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="68227-125">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="68227-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="68227-126">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="68227-126">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68227-127">Требования</span><span class="sxs-lookup"><span data-stu-id="68227-127">Requirements</span></span>



| <span data-ttu-id="68227-128">Требование</span><span class="sxs-lookup"><span data-stu-id="68227-128">Requirement</span></span> | <span data-ttu-id="68227-129">Значение</span><span class="sxs-lookup"><span data-stu-id="68227-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68227-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68227-130">Minimum supported client</span></span><br/> | <span data-ttu-id="68227-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68227-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68227-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68227-132">Minimum supported server</span></span><br/> | <span data-ttu-id="68227-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68227-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68227-134">Header</span><span class="sxs-lookup"><span data-stu-id="68227-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="68227-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68227-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="68227-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="68227-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="68227-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68227-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="68227-138">DLL</span><span class="sxs-lookup"><span data-stu-id="68227-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68227-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68227-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="68227-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="68227-140">CLSID</span></span><br/>                    | <span data-ttu-id="68227-141">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="68227-141">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="68227-142">IID</span><span class="sxs-lookup"><span data-stu-id="68227-142">IID</span></span><br/>                      | <span data-ttu-id="68227-143">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="68227-143">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="68227-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68227-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68227-145">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="68227-145">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="68227-146">**SWbemObject. размещение\_**</span><span class="sxs-lookup"><span data-stu-id="68227-146">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)
</dt> <dt>

[<span data-ttu-id="68227-147">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="68227-147">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

 




