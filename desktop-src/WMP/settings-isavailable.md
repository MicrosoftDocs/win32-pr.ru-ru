---
title: Settings. Available
description: Свойство Available указывает, доступен ли указанный тип сведений, или может быть выполнено указанное действие. | Settings. Available
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Универсальный проигрыватель Windows Media Settings.
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648667"
---
# <a name="settingsisavailable"></a><span data-ttu-id="cb18f-105">Settings. Available</span><span class="sxs-lookup"><span data-stu-id="cb18f-105">Settings.isAvailable</span></span>

<span data-ttu-id="cb18f-106">Свойство **Available** указывает, доступен ли указанный тип сведений, или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="cb18f-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb18f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb18f-107">Syntax</span></span>

<span data-ttu-id="cb18f-108">Player. Settings.-Available (имя)</span><span class="sxs-lookup"><span data-stu-id="cb18f-108">player.settings.isAvailable( name )</span></span>

## <a name="parameters"></a><span data-ttu-id="cb18f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb18f-109">Parameters</span></span>

<span data-ttu-id="cb18f-110">*name*</span><span class="sxs-lookup"><span data-stu-id="cb18f-110">*name*</span></span>

<span data-ttu-id="cb18f-111">Строка, содержащая одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cb18f-111">String containing one of the following values.</span></span>



| <span data-ttu-id="cb18f-112">Строка</span><span class="sxs-lookup"><span data-stu-id="cb18f-112">String</span></span>             | <span data-ttu-id="cb18f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cb18f-113">Description</span></span>                                                    |
|--------------------|----------------------------------------------------------------|
| <span data-ttu-id="cb18f-114">автозапуск</span><span class="sxs-lookup"><span data-stu-id="cb18f-114">AutoStart</span></span>          | <span data-ttu-id="cb18f-115">Определяет, можно ли задать свойство "Автозапуск".</span><span class="sxs-lookup"><span data-stu-id="cb18f-115">Determines whether the autoStart property can be set.</span></span>          |
| <span data-ttu-id="cb18f-116">Balance</span><span class="sxs-lookup"><span data-stu-id="cb18f-116">Balance</span></span>            | <span data-ttu-id="cb18f-117">Определяет, можно ли задать свойство Balance.</span><span class="sxs-lookup"><span data-stu-id="cb18f-117">Determines whether the balance property can be set.</span></span>            |
| <span data-ttu-id="cb18f-118">BaseURL</span><span class="sxs-lookup"><span data-stu-id="cb18f-118">BaseURL</span></span>            | <span data-ttu-id="cb18f-119">Определяет, можно ли задать свойство baseURL.</span><span class="sxs-lookup"><span data-stu-id="cb18f-119">Determines whether the baseURL property can be set.</span></span>            |
| <span data-ttu-id="cb18f-120">дефаултфраме</span><span class="sxs-lookup"><span data-stu-id="cb18f-120">DefaultFrame</span></span>       | <span data-ttu-id="cb18f-121">Определяет, можно ли задать свойство Дефаултфраме.</span><span class="sxs-lookup"><span data-stu-id="cb18f-121">Determines whether the defaultFrame property can be set.</span></span>       |
| <span data-ttu-id="cb18f-122">енаблиррордиалогс</span><span class="sxs-lookup"><span data-stu-id="cb18f-122">EnableErrorDialogs</span></span> | <span data-ttu-id="cb18f-123">Определяет, можно ли задать свойство Енаблиррордиалогс.</span><span class="sxs-lookup"><span data-stu-id="cb18f-123">Determines whether the enableErrorDialogs property can be set.</span></span> |
| <span data-ttu-id="cb18f-124">Режим</span><span class="sxs-lookup"><span data-stu-id="cb18f-124">GetMode</span></span>            | <span data-ttu-id="cb18f-125">Определяет, можно ли вызывать метод метода мода.</span><span class="sxs-lookup"><span data-stu-id="cb18f-125">Determines whether the getMode method can be called.</span></span>           |
| <span data-ttu-id="cb18f-126">инвокеурлс</span><span class="sxs-lookup"><span data-stu-id="cb18f-126">InvokeURLs</span></span>         | <span data-ttu-id="cb18f-127">Определяет, можно ли задать свойство Инвокеурлс.</span><span class="sxs-lookup"><span data-stu-id="cb18f-127">Determines whether the invokeURLs property can be set.</span></span>         |
| <span data-ttu-id="cb18f-128">Mute</span><span class="sxs-lookup"><span data-stu-id="cb18f-128">Mute</span></span>               | <span data-ttu-id="cb18f-129">Определяет, можно ли задать свойство "выключить звук".</span><span class="sxs-lookup"><span data-stu-id="cb18f-129">Determines whether the mute property can be set.</span></span>               |
| <span data-ttu-id="cb18f-130">плайкаунт</span><span class="sxs-lookup"><span data-stu-id="cb18f-130">PlayCount</span></span>          | <span data-ttu-id="cb18f-131">Определяет, можно ли задать свойство Плайкаунт.</span><span class="sxs-lookup"><span data-stu-id="cb18f-131">Determines whether the playCount property can be set.</span></span>          |
| <span data-ttu-id="cb18f-132">Тариф</span><span class="sxs-lookup"><span data-stu-id="cb18f-132">Rate</span></span>               | <span data-ttu-id="cb18f-133">Определяет, можно ли задать свойство Rate.</span><span class="sxs-lookup"><span data-stu-id="cb18f-133">Determines whether the rate property can be set.</span></span>               |
| <span data-ttu-id="cb18f-134">SetMode</span><span class="sxs-lookup"><span data-stu-id="cb18f-134">SetMode</span></span>            | <span data-ttu-id="cb18f-135">Определяет, можно ли вызывать метод setMode.</span><span class="sxs-lookup"><span data-stu-id="cb18f-135">Determines whether the setMode method can be called.</span></span>           |
| <span data-ttu-id="cb18f-136">Том</span><span class="sxs-lookup"><span data-stu-id="cb18f-136">Volume</span></span>             | <span data-ttu-id="cb18f-137">Определяет, можно ли задать свойство "том".</span><span class="sxs-lookup"><span data-stu-id="cb18f-137">Determines whether the volume property can be set.</span></span>             |



 

## <a name="return-values"></a><span data-ttu-id="cb18f-138">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cb18f-138">Return Values</span></span>

<span data-ttu-id="cb18f-139">Этот метод возвращает **логическое** значение.</span><span class="sxs-lookup"><span data-stu-id="cb18f-139">This method returns a **Boolean** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb18f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="cb18f-140">Requirements</span></span>



| <span data-ttu-id="cb18f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="cb18f-141">Requirement</span></span> | <span data-ttu-id="cb18f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="cb18f-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb18f-143">Версия</span><span class="sxs-lookup"><span data-stu-id="cb18f-143">Version</span></span><br/> | <span data-ttu-id="cb18f-144">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="cb18f-144">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cb18f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cb18f-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="cb18f-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb18f-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb18f-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb18f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb18f-148">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="cb18f-148">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





