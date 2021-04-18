---
title: Доступный DVD-диск.
description: Свойство Available указывает, доступен ли указанный тип сведений, или может быть выполнено указанное действие. | Доступный DVD-диск.
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- Проигрыватель Windows Media. доступ к DVD.
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693980"
---
# <a name="dvdisavailable"></a><span data-ttu-id="83256-105">Доступный DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="83256-105">DVD.isAvailable</span></span>

<span data-ttu-id="83256-106">Свойство **Available** указывает, доступен ли указанный тип сведений, или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="83256-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="83256-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="83256-107">Parameters</span></span>

<span data-ttu-id="83256-108">*name*</span><span class="sxs-lookup"><span data-stu-id="83256-108">*name*</span></span>

<span data-ttu-id="83256-109">**Строка** , содержащая одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="83256-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="83256-110">Строка</span><span class="sxs-lookup"><span data-stu-id="83256-110">String</span></span>     | <span data-ttu-id="83256-111">Описание</span><span class="sxs-lookup"><span data-stu-id="83256-111">Description</span></span>                                                                            |
|------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83256-112">Назад</span><span class="sxs-lookup"><span data-stu-id="83256-112">back</span></span>       | <span data-ttu-id="83256-113">Определяет, доступен ли метод **Back** .</span><span class="sxs-lookup"><span data-stu-id="83256-113">Determines whether the **back** method is available.</span></span>                                   |
| <span data-ttu-id="83256-114">оптически</span><span class="sxs-lookup"><span data-stu-id="83256-114">dvd</span></span>        | <span data-ttu-id="83256-115">Определяет, загружен ли DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="83256-115">Determines whether the DVD is loaded.</span></span>                                                  |
| <span data-ttu-id="83256-116">двддекодер</span><span class="sxs-lookup"><span data-stu-id="83256-116">dvdDecoder</span></span> | <span data-ttu-id="83256-117">Определяет, установлен ли декодер DVD в системе.</span><span class="sxs-lookup"><span data-stu-id="83256-117">Determines whether the DVD decoder is installed on system.</span></span>                             |
| <span data-ttu-id="83256-118">resume</span><span class="sxs-lookup"><span data-stu-id="83256-118">resume</span></span>     | <span data-ttu-id="83256-119">Определяет, доступен ли метод **Resume** .</span><span class="sxs-lookup"><span data-stu-id="83256-119">Determines whether the **resume** method is available.</span></span>                                 |
| <span data-ttu-id="83256-120">титлемену</span><span class="sxs-lookup"><span data-stu-id="83256-120">titleMenu</span></span>  | <span data-ttu-id="83256-121">Определяет, доступен ли метод **титлемену** .</span><span class="sxs-lookup"><span data-stu-id="83256-121">Determines whether the **titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="83256-122">топмену</span><span class="sxs-lookup"><span data-stu-id="83256-122">topMenu</span></span>    | <span data-ttu-id="83256-123">Определяет, доступен ли метод **топмену** .</span><span class="sxs-lookup"><span data-stu-id="83256-123">Determines whether the **topMenu** method is available.</span></span> <span data-ttu-id="83256-124">Обычно называется корневым меню.</span><span class="sxs-lookup"><span data-stu-id="83256-124">Commonly called the root menu.</span></span> |



 

## <a name="return-values"></a><span data-ttu-id="83256-125">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="83256-125">Return Values</span></span>

<span data-ttu-id="83256-126">Этот метод возвращает **логическое значение** , доступное только для чтения, указывающее, доступен ли указанный параметр.</span><span class="sxs-lookup"><span data-stu-id="83256-126">This method returns a read-only **Boolean** indicating whether the specified parameter is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="83256-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83256-127">Remarks</span></span>

<span data-ttu-id="83256-128">Возможности DVD проигрывателя Windows Media не будут работать на компьютерах, на которых не установлены сторонние декодеры DVD.</span><span class="sxs-lookup"><span data-stu-id="83256-128">The DVD features of Windows Media Player will not work on computers that do not have third-party DVD decoders installed.</span></span> <span data-ttu-id="83256-129">Можно определить, доступен ли декодер, **вызвав «** двддекодер».</span><span class="sxs-lookup"><span data-stu-id="83256-129">You can determine whether a decoder is available by calling **isAvailable**("dvdDecoder").</span></span>

<span data-ttu-id="83256-130">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="83256-130">Every DVD is authored differently.</span></span> <span data-ttu-id="83256-131">Методы, доступные во время воспроизведения DVD-диска и навигации, зависят от способа создания DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="83256-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

<span data-ttu-id="83256-132">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="83256-132">**Windows Media Player 10 Mobile:** This property always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="83256-133">Требования</span><span class="sxs-lookup"><span data-stu-id="83256-133">Requirements</span></span>



| <span data-ttu-id="83256-134">Требование</span><span class="sxs-lookup"><span data-stu-id="83256-134">Requirement</span></span> | <span data-ttu-id="83256-135">Значение</span><span class="sxs-lookup"><span data-stu-id="83256-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83256-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83256-136">Minimum supported client</span></span><br/> | <span data-ttu-id="83256-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="83256-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83256-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83256-138">Minimum supported server</span></span><br/> | <span data-ttu-id="83256-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83256-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83256-140">Версия</span><span class="sxs-lookup"><span data-stu-id="83256-140">Version</span></span><br/>                  | <span data-ttu-id="83256-141">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="83256-141">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="83256-142">DLL</span><span class="sxs-lookup"><span data-stu-id="83256-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83256-143"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83256-143"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83256-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83256-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83256-145">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="83256-145">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





