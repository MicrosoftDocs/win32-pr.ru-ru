---
description: Метод Свбемрефрешер. Add добавляет новый объект Свбемрефрешаблеитем в коллекцию в объекте Свбемрефрешер. Свбемрефрешаблеитем объект в коллекцию в объекте Свбемрефрешер.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Метод Свбемрефрешер. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703443"
---
# <a name="swbemrefresheradd-method"></a><span data-ttu-id="76efd-103">Свбемрефрешер. Add, метод</span><span class="sxs-lookup"><span data-stu-id="76efd-103">SWbemRefresher.Add method</span></span>

<span data-ttu-id="76efd-104">Метод **свбемрефрешер. Add** добавляет новый объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) в коллекцию в объекте [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="76efd-104">The **SWbemRefresher.Add** method adds a new [**SWbemRefreshableItem**](swbemrefreshableitem.md) object to the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="76efd-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="76efd-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76efd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76efd-106">Syntax</span></span>


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="76efd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="76efd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76efd-108">*обжвбемсервице*</span><span class="sxs-lookup"><span data-stu-id="76efd-108">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="76efd-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="76efd-109">Required.</span></span> <span data-ttu-id="76efd-110">Объект [**SwbemServices**](swbemservices.md) , представляющий соединение с пространством имен, в котором находится объект, добавляемый в обновитель.</span><span class="sxs-lookup"><span data-stu-id="76efd-110">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="76efd-111">*стринстанцепас*</span><span class="sxs-lookup"><span data-stu-id="76efd-111">*strInstancePath*</span></span> 
</dt> <dd>

<span data-ttu-id="76efd-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="76efd-112">Required.</span></span> <span data-ttu-id="76efd-113">Строка, содержащая относительный путь к объекту в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="76efd-113">String that contains the relative path of the object in the namespace.</span></span> <span data-ttu-id="76efd-114">Путь должен содержать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="76efd-114">The path must contain an instance.</span></span> <span data-ttu-id="76efd-115">Свойство [**index**](swbemrefreshableitem-index.md) возвращаемого [**свбемрефрешаблеитем**](swbemrefreshableitem.md) представляет индекс объекта в коллекции обновитель.</span><span class="sxs-lookup"><span data-stu-id="76efd-115">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="76efd-116">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="76efd-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76efd-117">Строка, содержащая путь к объекту, для которого выполняется метод.</span><span class="sxs-lookup"><span data-stu-id="76efd-117">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="76efd-118">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="76efd-118">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76efd-119">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="76efd-119">Typically, this is undefined.</span></span> <span data-ttu-id="76efd-120">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает.</span><span class="sxs-lookup"><span data-stu-id="76efd-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="76efd-121">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="76efd-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76efd-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76efd-122">Return value</span></span>

<span data-ttu-id="76efd-123">Если вызов выполнен успешно, возвращается объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) , содержащий один обновляемый объект.</span><span class="sxs-lookup"><span data-stu-id="76efd-123">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains a single refreshable object is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="76efd-124">Требования</span><span class="sxs-lookup"><span data-stu-id="76efd-124">Requirements</span></span>



| <span data-ttu-id="76efd-125">Требование</span><span class="sxs-lookup"><span data-stu-id="76efd-125">Requirement</span></span> | <span data-ttu-id="76efd-126">Значение</span><span class="sxs-lookup"><span data-stu-id="76efd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76efd-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76efd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="76efd-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76efd-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76efd-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76efd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="76efd-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76efd-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76efd-131">Header</span><span class="sxs-lookup"><span data-stu-id="76efd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="76efd-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="76efd-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="76efd-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="76efd-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="76efd-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76efd-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76efd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="76efd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76efd-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76efd-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="76efd-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="76efd-137">CLSID</span></span><br/>                    | <span data-ttu-id="76efd-138">\_СВБЕМРЕФРЕШЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="76efd-138">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="76efd-139">IID</span><span class="sxs-lookup"><span data-stu-id="76efd-139">IID</span></span><br/>                      | <span data-ttu-id="76efd-140">IID \_ исвбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="76efd-140">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="76efd-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76efd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76efd-142">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="76efd-142">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




