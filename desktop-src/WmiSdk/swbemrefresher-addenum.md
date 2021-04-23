---
description: Добавляет новый перечислитель в объект Свбемрефрешер. Этот перечислитель предназначен для всех экземпляров класса, указанных в параметре Стркласс.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Свбемрефрешер. Адденум, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820221"
---
# <a name="swbemrefresheraddenum-method"></a><span data-ttu-id="256c9-104">Свбемрефрешер. Адденум, метод</span><span class="sxs-lookup"><span data-stu-id="256c9-104">SWbemRefresher.AddEnum method</span></span>

<span data-ttu-id="256c9-105">Метод **свбемрефрешер. адденум** добавляет новый перечислитель в объект [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="256c9-105">The **SWbemRefresher.AddEnum** method adds a new enumerator to the [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="256c9-106">Этот перечислитель предназначен для всех экземпляров класса, указанных в параметре *стркласс* .</span><span class="sxs-lookup"><span data-stu-id="256c9-106">This enumerator is for all the instances of the class that is specified in the *strClass* parameter.</span></span>

<span data-ttu-id="256c9-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="256c9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="256c9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="256c9-108">Syntax</span></span>


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="256c9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="256c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="256c9-110">*обжвбемсервице*</span><span class="sxs-lookup"><span data-stu-id="256c9-110">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="256c9-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="256c9-111">Required.</span></span> <span data-ttu-id="256c9-112">Объект [**SwbemServices**](swbemservices.md) , представляющий соединение с пространством имен, в котором находится объект, добавляемый в обновитель.</span><span class="sxs-lookup"><span data-stu-id="256c9-112">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="256c9-113">*стркласс*</span><span class="sxs-lookup"><span data-stu-id="256c9-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="256c9-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="256c9-114">Required.</span></span> <span data-ttu-id="256c9-115">Строка, содержащая класс, добавляемый в обновитель.</span><span class="sxs-lookup"><span data-stu-id="256c9-115">String that contains the class that is being added to the refresher.</span></span> <span data-ttu-id="256c9-116">Этот класс используется в качестве перечислителя экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="256c9-116">This class is used as an enumerator of the instances of the class.</span></span> <span data-ttu-id="256c9-117">Свойство [**index**](swbemrefreshableitem-index.md) возвращаемого [**свбемрефрешаблеитем**](swbemrefreshableitem.md) представляет индекс перечислителя в коллекции обновитель.</span><span class="sxs-lookup"><span data-stu-id="256c9-117">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the enumerator in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="256c9-118">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="256c9-118">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="256c9-119">Строка, содержащая путь к объекту, для которого выполняется метод.</span><span class="sxs-lookup"><span data-stu-id="256c9-119">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="256c9-120">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="256c9-120">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="256c9-121">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="256c9-121">Typically, this is undefined.</span></span> <span data-ttu-id="256c9-122">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает.</span><span class="sxs-lookup"><span data-stu-id="256c9-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="256c9-123">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="256c9-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="256c9-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="256c9-124">Return value</span></span>

<span data-ttu-id="256c9-125">Если вызов выполнен успешно, возвращается объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) , содержащий перечислитель для всех экземпляров указанного класса.</span><span class="sxs-lookup"><span data-stu-id="256c9-125">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains an enumerator for all the instances for the specified class is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="256c9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="256c9-126">Requirements</span></span>



| <span data-ttu-id="256c9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="256c9-127">Requirement</span></span> | <span data-ttu-id="256c9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="256c9-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="256c9-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="256c9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="256c9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="256c9-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="256c9-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="256c9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="256c9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="256c9-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="256c9-133">Header</span><span class="sxs-lookup"><span data-stu-id="256c9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="256c9-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="256c9-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="256c9-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="256c9-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="256c9-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="256c9-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="256c9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="256c9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="256c9-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="256c9-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="256c9-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="256c9-139">CLSID</span></span><br/>                    | <span data-ttu-id="256c9-140">\_СВБЕМРЕФРЕШЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="256c9-140">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="256c9-141">IID</span><span class="sxs-lookup"><span data-stu-id="256c9-141">IID</span></span><br/>                      | <span data-ttu-id="256c9-142">IID \_ исвбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="256c9-142">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="256c9-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="256c9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256c9-144">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="256c9-144">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




