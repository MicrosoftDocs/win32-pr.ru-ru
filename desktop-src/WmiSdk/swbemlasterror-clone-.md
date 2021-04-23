---
description: Метод Clone \_ объекта свбемластеррор возвращает новый объект, который является клоном текущего объекта свбемластеррор.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: Метод SWbemLastError.Clone_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693266"
---
# <a name="swbemlasterrorclone_-method"></a><span data-ttu-id="8bb21-103">Свбемластеррор. Clone, \_ метод</span><span class="sxs-lookup"><span data-stu-id="8bb21-103">SWbemLastError.Clone\_ method</span></span>

<span data-ttu-id="8bb21-104">Метод **Clone \_** объекта [**свбемластеррор**](swbemlasterror.md) возвращает новый объект, который является клоном текущего объекта **свбемластеррор** .</span><span class="sxs-lookup"><span data-stu-id="8bb21-104">The **Clone\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a new object that is a clone of the current **SWbemLastError** object.</span></span>

<span data-ttu-id="8bb21-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8bb21-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb21-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bb21-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="8bb21-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bb21-107">Parameters</span></span>

<span data-ttu-id="8bb21-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8bb21-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8bb21-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bb21-109">Return value</span></span>

<span data-ttu-id="8bb21-110">Если метод **Clone \_** успешно выполнен, он возвращает новый объект [**свбемластеррор**](swbemlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8bb21-110">If the **Clone\_** method is successful, it returns a new [**SWbemLastError**](swbemlasterror.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8bb21-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8bb21-111">Error codes</span></span>

<span data-ttu-id="8bb21-112">После завершения метода **Clone \_** объект **Err** может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="8bb21-112">Upon the completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="8bb21-113">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8bb21-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8bb21-114">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8bb21-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8bb21-115">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8bb21-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8bb21-116">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="8bb21-116">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8bb21-117">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8bb21-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8bb21-118">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="8bb21-118">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bb21-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bb21-119">Remarks</span></span>

<span data-ttu-id="8bb21-120">Используйте метод **Clone \_** для дублирования определения или экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="8bb21-120">Use the **Clone\_** method to duplicate a class definition or instance.</span></span> <span data-ttu-id="8bb21-121">Этот метод полезен, если необходимо создать резервную копию исходной копии объекта при изменении новой копии.</span><span class="sxs-lookup"><span data-stu-id="8bb21-121">This method is useful when you need to back up the original copy of the object while you modify a new copy.</span></span> <span data-ttu-id="8bb21-122">Кроме того, используйте этот метод, чтобы создать множество новых экземпляров из одного экземпляра источника.</span><span class="sxs-lookup"><span data-stu-id="8bb21-122">Also, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="8bb21-123">Например, используйте [**SWbemObject. спавнинстанце \_**](swbemobject-spawninstance-.md) , чтобы создать один начальный экземпляр и использовать **свбемластеррор. Clone \_** для быстрого создания копий экземпляра 100.</span><span class="sxs-lookup"><span data-stu-id="8bb21-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance and use **SWbemLastError.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="8bb21-124">Впоследствии можно изменить объекты, указав конкретные значения для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="8bb21-124">Subsequently, you can modify the objects, giving specific values to each object.</span></span>

<span data-ttu-id="8bb21-125">Этот метод невозможно использовать для преобразования определения класса в экземпляр или для преобразования экземпляра в определение класса.</span><span class="sxs-lookup"><span data-stu-id="8bb21-125">It is not possible to use this method to convert a class definition to an instance or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb21-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8bb21-126">Requirements</span></span>



| <span data-ttu-id="8bb21-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8bb21-127">Requirement</span></span> | <span data-ttu-id="8bb21-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8bb21-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb21-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bb21-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb21-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bb21-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8bb21-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bb21-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb21-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bb21-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8bb21-133">Header</span><span class="sxs-lookup"><span data-stu-id="8bb21-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb21-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb21-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bb21-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8bb21-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="8bb21-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8bb21-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8bb21-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8bb21-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bb21-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bb21-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8bb21-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="8bb21-139">CLSID</span></span><br/>                    | <span data-ttu-id="8bb21-140">\_СВБЕМЛАСТЕРРОР CLSID</span><span class="sxs-lookup"><span data-stu-id="8bb21-140">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="8bb21-141">IID</span><span class="sxs-lookup"><span data-stu-id="8bb21-141">IID</span></span><br/>                      | <span data-ttu-id="8bb21-142">IID \_ исвбемластеррор</span><span class="sxs-lookup"><span data-stu-id="8bb21-142">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




