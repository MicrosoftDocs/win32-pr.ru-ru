---
title: ИВМПДВД. доступ (VB и C)
description: Свойство Available (метод Get- \_ Available в C \) возвращает значение, указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- Проигрыватель Windows Media ИВМПДВД. Available (VB и C)
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689110"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a><span data-ttu-id="f186d-104">ИВМПДВД. доступ (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="f186d-104">IWMPDVD.isAvailable (VB and C#)</span></span>

<span data-ttu-id="f186d-105">Свойство **Available** (метод Get- **\_ Available** в C#) возвращает значение, указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="f186d-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a><span data-ttu-id="f186d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f186d-106">Parameters</span></span>

<span data-ttu-id="f186d-107">*бстритем*</span><span class="sxs-lookup"><span data-stu-id="f186d-107">*bstrItem*</span></span>

<span data-ttu-id="f186d-108">Строка System. String, которая является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f186d-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="f186d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f186d-109">Value</span></span>      | <span data-ttu-id="f186d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f186d-110">Description</span></span>                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f186d-111">Назад</span><span class="sxs-lookup"><span data-stu-id="f186d-111">back</span></span>       | <span data-ttu-id="f186d-112">Обнаруживает, доступен ли метод **ивмпдвд. Back** .</span><span class="sxs-lookup"><span data-stu-id="f186d-112">Discovers whether the **IWMPDVD.back** method is available.</span></span>                                   |
| <span data-ttu-id="f186d-113">оптически</span><span class="sxs-lookup"><span data-stu-id="f186d-113">dvd</span></span>        | <span data-ttu-id="f186d-114">Обнаруживает, загружен ли DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="f186d-114">Discovers whether the DVD is loaded.</span></span>                                                          |
| <span data-ttu-id="f186d-115">двддекодер</span><span class="sxs-lookup"><span data-stu-id="f186d-115">dvdDecoder</span></span> | <span data-ttu-id="f186d-116">Обнаруживает, установлен ли декодер DVD в системе.</span><span class="sxs-lookup"><span data-stu-id="f186d-116">Discovers whether the DVD decoder is installed on system.</span></span>                                     |
| <span data-ttu-id="f186d-117">resume</span><span class="sxs-lookup"><span data-stu-id="f186d-117">resume</span></span>     | <span data-ttu-id="f186d-118">Обнаруживает, доступен ли метод **ивмпдвд. Resume** .</span><span class="sxs-lookup"><span data-stu-id="f186d-118">Discovers whether the **IWMPDVD.resume** method is available.</span></span>                                 |
| <span data-ttu-id="f186d-119">титлемену</span><span class="sxs-lookup"><span data-stu-id="f186d-119">titleMenu</span></span>  | <span data-ttu-id="f186d-120">Обнаруживает, доступен ли метод **ивмпдвд. титлемену** .</span><span class="sxs-lookup"><span data-stu-id="f186d-120">Discovers whether the **IWMPDVD.titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="f186d-121">топмену</span><span class="sxs-lookup"><span data-stu-id="f186d-121">topMenu</span></span>    | <span data-ttu-id="f186d-122">Обнаруживает, доступен ли метод **ивмпдвд. топмену** .</span><span class="sxs-lookup"><span data-stu-id="f186d-122">Discovers whether the **IWMPDVD.topMenu** method is available.</span></span> <span data-ttu-id="f186d-123">Обычно называется корневым меню.</span><span class="sxs-lookup"><span data-stu-id="f186d-123">Commonly called the root menu.</span></span> |



 

## <a name="property-value"></a><span data-ttu-id="f186d-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f186d-124">Property Value</span></span>

<span data-ttu-id="f186d-125">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="f186d-125">**System.Boolean**</span></span>

<span data-ttu-id="f186d-126">Значение **System. Boolean** , указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="f186d-126">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f186d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f186d-127">Remarks</span></span>

<span data-ttu-id="f186d-128">Возможности DVD проигрывателя Windows Media не будут работать на компьютерах, на которых не установлен декодер DVD.</span><span class="sxs-lookup"><span data-stu-id="f186d-128">The DVD features of Windows Media Player will not work on computers that do not have a DVD decoder installed.</span></span> <span data-ttu-id="f186d-129">Можно определить, доступен ли декодер, вызвав свойство **Available** (метод **Get- \_ Available** в C#) и передав значение **System. String** "двддекодер".</span><span class="sxs-lookup"><span data-stu-id="f186d-129">You can determine whether a decoder is available by calling the **isAvailable** property (the **get\_isAvailable** method in C#) and passing in the **System.String** value "dvdDecoder".</span></span>

<span data-ttu-id="f186d-130">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="f186d-130">Every DVD is authored differently.</span></span> <span data-ttu-id="f186d-131">Методы, доступные во время воспроизведения DVD-диска и навигации, зависят от способа создания DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="f186d-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f186d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f186d-132">Requirements</span></span>



| <span data-ttu-id="f186d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f186d-133">Requirement</span></span> | <span data-ttu-id="f186d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f186d-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f186d-135">Версия</span><span class="sxs-lookup"><span data-stu-id="f186d-135">Version</span></span><br/>   | <span data-ttu-id="f186d-136">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f186d-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f186d-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f186d-137">Namespace</span></span><br/> | <span data-ttu-id="f186d-138">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f186d-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f186d-139">Сборка</span><span class="sxs-lookup"><span data-stu-id="f186d-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f186d-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f186d-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f186d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f186d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f186d-142">**Интерфейс ИВМПДВД (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f186d-142">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f186d-143">**ИВМПДВД. Back (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f186d-143">**IWMPDVD.back (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f186d-144">**ИВМПДВД. Resume (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f186d-144">**IWMPDVD.resume (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f186d-145">**ИВМПДВД. Титлемену (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f186d-145">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f186d-146">**ИВМПДВД. Топмену (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f186d-146">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





