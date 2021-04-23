---
description: Используйте метод Спавндериведкласс \_ объекта SWbemObject для создания объекта производного класса из текущего объекта. Объект должен быть определением класса, который станет родительским классом порожденного объекта.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Метод SWbemObject.SpawnDerivedClass_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263799"
---
# <a name="swbemobjectspawnderivedclass_-method"></a><span data-ttu-id="e6990-104">SWbemObject. Спавндериведкласс, \_ метод</span><span class="sxs-lookup"><span data-stu-id="e6990-104">SWbemObject.SpawnDerivedClass\_ method</span></span>

<span data-ttu-id="e6990-105">Используйте метод **спавндериведкласс \_** объекта [**SWbemObject**](swbemobject.md) для создания объекта производного класса из текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="e6990-105">Use the **SpawnDerivedClass\_** method of the [**SWbemObject**](swbemobject.md) object to create a derived class object from the current object.</span></span> <span data-ttu-id="e6990-106">Объект должен быть определением класса, который станет родительским классом порожденного объекта.</span><span class="sxs-lookup"><span data-stu-id="e6990-106">The object must be a class definition that becomes the parent class of the spawned object.</span></span>

<span data-ttu-id="e6990-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e6990-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6990-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6990-108">Syntax</span></span>


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e6990-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6990-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6990-110">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="e6990-110">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6990-111">Зарезервировано и должно быть равно 0 (нулю), если оно указано.</span><span class="sxs-lookup"><span data-stu-id="e6990-111">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6990-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6990-112">Return value</span></span>

<span data-ttu-id="e6990-113">Если вызов выполнен успешно, объект [**SWbemObject**](swbemobject.md) содержит новый объект определения класса.</span><span class="sxs-lookup"><span data-stu-id="e6990-113">If the call is successful, the [**SWbemObject**](swbemobject.md) object contains the new class definition object.</span></span> <span data-ttu-id="e6990-114">При возникновении ошибки объект не возвращается.</span><span class="sxs-lookup"><span data-stu-id="e6990-114">No object returns when there is an error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6990-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e6990-115">Error codes</span></span>

<span data-ttu-id="e6990-116">После завершения метода **спавндериведкласс \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="e6990-116">After the completion of the **SpawnDerivedClass\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e6990-117">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e6990-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e6990-118">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e6990-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e6990-119">**вбемерриллегалоператион** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="e6990-119">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="e6990-120">Пользователь запросил недопустимую операцию, например, порождение класса из экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e6990-120">User requested an illegal operation, such as spawning a class from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="e6990-121">**вбемерринкомплетекласс** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="e6990-121">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="e6990-122">Исходный класс не был полностью определен или зарегистрирован в WMI, поэтому новый производный класс не разрешен.</span><span class="sxs-lookup"><span data-stu-id="e6990-122">Source class was not completely defined or registered with WMI, so a new derived class is not permitted.</span></span>

</dd> <dt>

<span data-ttu-id="e6990-123">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="e6990-123">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="e6990-124">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="e6990-124">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6990-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6990-125">Remarks</span></span>

<span data-ttu-id="e6990-126">Возвращаемый объект автоматически становится подклассом текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="e6990-126">The object that is returned automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="e6990-127">Это поведение не может быть переопределено.</span><span class="sxs-lookup"><span data-stu-id="e6990-127">This behavior cannot be overridden.</span></span> <span data-ttu-id="e6990-128">Нет других методов, с помощью которых можно создавать производные классы.</span><span class="sxs-lookup"><span data-stu-id="e6990-128">There is no other method by which you can create derived classes.</span></span>

<span data-ttu-id="e6990-129">Нельзя создать производный класс из класса, который является локальным для собственного клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="e6990-129">You cannot create a derived class from a class that is local to your own client process.</span></span> <span data-ttu-id="e6990-130">Прежде чем использовать этот метод для создания производного класса, необходимо создать базовый класс.</span><span class="sxs-lookup"><span data-stu-id="e6990-130">Before use this method to create a derived class, you must create the base class.</span></span> <span data-ttu-id="e6990-131">Чтобы создать базовый класс, вызовите [**SWbemObject. \_**](swbemobject-put-.md)WHERE и получите базовый класс с помощью [**SwbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="e6990-131">To create the base class, call [**SWbemObject.Put\_**](swbemobject-put-.md), and retrieve the base class using [**SWbemServices.Get**](swbemservices-get.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6990-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e6990-132">Requirements</span></span>



| <span data-ttu-id="e6990-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e6990-133">Requirement</span></span> | <span data-ttu-id="e6990-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e6990-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6990-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6990-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e6990-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6990-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e6990-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6990-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e6990-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6990-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e6990-139">Header</span><span class="sxs-lookup"><span data-stu-id="e6990-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6990-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6990-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6990-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e6990-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6990-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e6990-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e6990-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e6990-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6990-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6990-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6990-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="e6990-145">CLSID</span></span><br/>                    | <span data-ttu-id="e6990-146">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="e6990-146">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="e6990-147">IID</span><span class="sxs-lookup"><span data-stu-id="e6990-147">IID</span></span><br/>                      | <span data-ttu-id="e6990-148">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="e6990-148">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




