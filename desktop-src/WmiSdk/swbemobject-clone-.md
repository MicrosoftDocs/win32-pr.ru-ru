---
description: Метод Clone \_ объекта SWbemObject возвращает новый объект, который является клоном текущего объекта.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: Метод SWbemObject.Clone_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081352"
---
# <a name="swbemobjectclone_-method"></a><span data-ttu-id="79875-103">SWbemObject. Clone, \_ метод</span><span class="sxs-lookup"><span data-stu-id="79875-103">SWbemObject.Clone\_ method</span></span>

<span data-ttu-id="79875-104">Метод **Clone \_** объекта [**SWbemObject**](swbemobject.md) возвращает новый объект, который является клоном текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="79875-104">The **Clone\_** method of the [**SWbemObject**](swbemobject.md) object returns a new object that is a clone of the current object.</span></span>

<span data-ttu-id="79875-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="79875-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="79875-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79875-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="79875-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="79875-107">Parameters</span></span>

<span data-ttu-id="79875-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="79875-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79875-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79875-109">Return value</span></span>

<span data-ttu-id="79875-110">В случае успешного выполнения этот метод возвращает новый объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="79875-110">If successful, this method returns a new [**SWbemObject**](swbemobject.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="79875-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="79875-111">Error codes</span></span>

<span data-ttu-id="79875-112">После завершения метода **Clone \_** объект **Err** может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="79875-112">After completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="79875-113">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="79875-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="79875-114">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="79875-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="79875-115">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="79875-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="79875-116">В качестве параметра не указано **ничего** , и это неприемлемо в этом использовании.</span><span class="sxs-lookup"><span data-stu-id="79875-116">**Nothing** was specified as a parameter, and it is not acceptable in this usage.</span></span>

</dd> <dt>

<span data-ttu-id="79875-117">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="79875-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="79875-118">Недостаточно памяти для клонирования объекта.</span><span class="sxs-lookup"><span data-stu-id="79875-118">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79875-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79875-119">Remarks</span></span>

<span data-ttu-id="79875-120">Используйте метод **Clone \_** для дублирования определения класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="79875-120">Use the **Clone\_** method to duplicate a class definition or an instance.</span></span> <span data-ttu-id="79875-121">Это полезно, если требуется исходная копия объекта для резервного копирования при изменении новой копии.</span><span class="sxs-lookup"><span data-stu-id="79875-121">This is useful when you need the original copy of the object for backup purposes while you are modifying a new copy.</span></span> <span data-ttu-id="79875-122">Аналогичным образом, используйте этот метод, чтобы создать множество новых экземпляров из одного экземпляра источника.</span><span class="sxs-lookup"><span data-stu-id="79875-122">Likewise, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="79875-123">Например, используйте [**SWbemObject. спавнинстанце \_**](swbemobject-spawninstance-.md) для создания одного начального экземпляра и используйте **SWbemObject. Clone \_** для быстрого создания копий экземпляра 100.</span><span class="sxs-lookup"><span data-stu-id="79875-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance, and use **SWbemObject.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="79875-124">Впоследствии можно изменить объекты, предоставив каждому из них определенные значения.</span><span class="sxs-lookup"><span data-stu-id="79875-124">Subsequently, you can modify the objects, giving each one specific values.</span></span>

<span data-ttu-id="79875-125">Этот метод невозможно использовать для преобразования определения класса в экземпляр или для преобразования экземпляра в определение класса.</span><span class="sxs-lookup"><span data-stu-id="79875-125">It is not possible to use this method to convert a class definition to an instance, or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="79875-126">Требования</span><span class="sxs-lookup"><span data-stu-id="79875-126">Requirements</span></span>



| <span data-ttu-id="79875-127">Требование</span><span class="sxs-lookup"><span data-stu-id="79875-127">Requirement</span></span> | <span data-ttu-id="79875-128">Значение</span><span class="sxs-lookup"><span data-stu-id="79875-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79875-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79875-129">Minimum supported client</span></span><br/> | <span data-ttu-id="79875-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79875-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79875-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79875-131">Minimum supported server</span></span><br/> | <span data-ttu-id="79875-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79875-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79875-133">Header</span><span class="sxs-lookup"><span data-stu-id="79875-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="79875-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79875-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="79875-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="79875-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="79875-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79875-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79875-137">DLL</span><span class="sxs-lookup"><span data-stu-id="79875-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79875-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79875-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="79875-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="79875-139">CLSID</span></span><br/>                    | <span data-ttu-id="79875-140">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="79875-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="79875-141">IID</span><span class="sxs-lookup"><span data-stu-id="79875-141">IID</span></span><br/>                      | <span data-ttu-id="79875-142">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="79875-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




