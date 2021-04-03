---
description: '\\Международная панель управления HKCU \\ .'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: аддхижридате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895577"
---
# <a name="addhijridate"></a><span data-ttu-id="30f88-103">аддхижридате</span><span class="sxs-lookup"><span data-stu-id="30f88-103">AddHijriDate</span></span>

<span data-ttu-id="30f88-104">**\\Международная панель управления \\ HKCU**</span><span class="sxs-lookup"><span data-stu-id="30f88-104">**HKCU\\Control Panel\\International**</span></span>



| <span data-ttu-id="30f88-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="30f88-105">Data type</span></span> | <span data-ttu-id="30f88-106">Диапазон</span><span class="sxs-lookup"><span data-stu-id="30f88-106">Range</span></span>                      | <span data-ttu-id="30f88-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="30f88-107">Default value</span></span> |
|-----------|----------------------------|---------------|
| <span data-ttu-id="30f88-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="30f88-108">REG\_SZ</span></span>   | <span data-ttu-id="30f88-109">*Допустимое значение корректировки*</span><span class="sxs-lookup"><span data-stu-id="30f88-109">*A valid adjustment value*</span></span> | <span data-ttu-id="30f88-110">(нет)</span><span class="sxs-lookup"><span data-stu-id="30f88-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="30f88-111">Описание</span><span class="sxs-lookup"><span data-stu-id="30f88-111">Description</span></span>

<span data-ttu-id="30f88-112">Указывает корректировки даты в календаре Хиджра.</span><span class="sxs-lookup"><span data-stu-id="30f88-112">Specifies adjustments to the date within the Hijri calendar.</span></span>

<span data-ttu-id="30f88-113">Календарь Хиджра — лунный календарь, используемый в мусульманском мире.</span><span class="sxs-lookup"><span data-stu-id="30f88-113">The Hijri calendar is a lunar calendar used in the Islamic world.</span></span> <span data-ttu-id="30f88-114">Месяцы начинаются и заканчиваются в соответствии с Декри, основанным на наблюдении за новым лунами.</span><span class="sxs-lookup"><span data-stu-id="30f88-114">The months begin and end according to a decree that is based on the observation of the new moon.</span></span> <span data-ttu-id="30f88-115">Трудно правильно спрогнозировать начало и конец месяцев, и существуют региональные вариации, поэтому в календарь вносится корректировка от нуля до двух дней.</span><span class="sxs-lookup"><span data-stu-id="30f88-115">It is difficult to accurately predict the beginnings and endings of the months, and there are regional variations, so an adjustment of between zero and two days is made to the calendar.</span></span>

<span data-ttu-id="30f88-116">Параметр реестра **аддхижридате** сохраняет это значение корректировки следующим образом.</span><span class="sxs-lookup"><span data-stu-id="30f88-116">The **AddHijriDate** registry value stores this adjustment value as follows.</span></span>



| <span data-ttu-id="30f88-117">Значение</span><span class="sxs-lookup"><span data-stu-id="30f88-117">Value</span></span>          | <span data-ttu-id="30f88-118">Значение</span><span class="sxs-lookup"><span data-stu-id="30f88-118">Meaning</span></span>                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30f88-119">Аддхижридате-2</span><span class="sxs-lookup"><span data-stu-id="30f88-119">AddHijriDate-2</span></span> | <span data-ttu-id="30f88-120">Вычесть два дня.</span><span class="sxs-lookup"><span data-stu-id="30f88-120">Subtract two days.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="30f88-121">аддхижридате</span><span class="sxs-lookup"><span data-stu-id="30f88-121">AddHijriDate</span></span>   | <span data-ttu-id="30f88-122">Вычесть один день.</span><span class="sxs-lookup"><span data-stu-id="30f88-122">Subtract one day.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="30f88-123">(пусто)</span><span class="sxs-lookup"><span data-stu-id="30f88-123">(blank)</span></span>        | <span data-ttu-id="30f88-124">Корректировка не требуется.</span><span class="sxs-lookup"><span data-stu-id="30f88-124">No adjustment is necessary.</span></span> <span data-ttu-id="30f88-125">(Если дата не была скорректирована, эта запись не отображается в реестре.</span><span class="sxs-lookup"><span data-stu-id="30f88-125">(If the date has not been adjusted, this entry does not appear in the registry.</span></span> <span data-ttu-id="30f88-126">Если дата была скорректирована, а затем восстановлена до исходного значения, эта запись появляется в реестре без значения.)</span><span class="sxs-lookup"><span data-stu-id="30f88-126">If the date has been adjusted and then restored to its original value, this entry appears in the registry with no value.)</span></span> |
| <span data-ttu-id="30f88-127">Аддхижридате + 1</span><span class="sxs-lookup"><span data-stu-id="30f88-127">AddHijriDate+1</span></span> | <span data-ttu-id="30f88-128">Добавьте один день.</span><span class="sxs-lookup"><span data-stu-id="30f88-128">Add one day.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="30f88-129">Аддхижридате + 2</span><span class="sxs-lookup"><span data-stu-id="30f88-129">AddHijriDate+2</span></span> | <span data-ttu-id="30f88-130">Добавьте два дня.</span><span class="sxs-lookup"><span data-stu-id="30f88-130">Add two days.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="30f88-131">Эта запись не существует в реестре по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30f88-131">This entry does not exist in the registry by default.</span></span> <span data-ttu-id="30f88-132">Его можно добавить с помощью редактора реестра Regedit.exe или с помощью метода Change, описанного ниже.</span><span class="sxs-lookup"><span data-stu-id="30f88-132">You can add it by using the registry editor Regedit.exe or by using the change method described below.</span></span>

## <a name="change-method"></a><span data-ttu-id="30f88-133">Изменение метода</span><span class="sxs-lookup"><span data-stu-id="30f88-133">Change Method</span></span>

<span data-ttu-id="30f88-134">Чтобы изменить значение этой записи или добавить ее в реестр, сначала установите файлы для наборов сложных символов и языков с письмом справа налево.</span><span class="sxs-lookup"><span data-stu-id="30f88-134">To change the value of this entry, or to add it to the registry, first install the files for complex script and right-to-left languages.</span></span> <span data-ttu-id="30f88-135">На панели управления щелкните **региональные и языковые параметры**, а затем перейдите на вкладку **языки** . В разделе **Дополнительная языковая поддержка** установите флажок, чтобы **установить файлы для наборов сложных символов и языков с письмом справа налево (включая тайский)**.</span><span class="sxs-lookup"><span data-stu-id="30f88-135">In Control Panel, click **Regional and Language Options**, then click the **Languages** tab. Under **Supplemental language support**, select the checkbox to **Install files for complex script and right-to-left languages (including Thai)**.</span></span> <span data-ttu-id="30f88-136">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="30f88-136">Click **OK**.</span></span>

<span data-ttu-id="30f88-137">Чтобы изменить значение этой записи или добавить ее в реестр, в панели управления щелкните **региональные и языковые параметры**.</span><span class="sxs-lookup"><span data-stu-id="30f88-137">To change the value of this entry, or to add it to the registry, from Control Panel, click **Regional and Language Options**.</span></span> <span data-ttu-id="30f88-138">В поле **стандарты и форматы** выберите языковой стандарт, в котором используется календарь Хиджра.</span><span class="sxs-lookup"><span data-stu-id="30f88-138">In the **Standards and Formats** field, select a locale that uses the Hijri calendar.</span></span> <span data-ttu-id="30f88-139">Нажмите кнопку " **настроить** ", а затем перейдите на вкладку " **Дата** ". В раскрывающемся списке **изменить дату календаря на:** выберите соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="30f88-139">Click the **Customize** button, then click the **Date** tab. In the **Adjust Hijri date to:** drop-down list, select the appropriate value.</span></span> <span data-ttu-id="30f88-140">Нажмите кнопку **ОК**, а затем еще раз кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="30f88-140">Click **OK**, then click **OK** again.</span></span>

## <a name="activation-method"></a><span data-ttu-id="30f88-141">Метод активации</span><span class="sxs-lookup"><span data-stu-id="30f88-141">Activation Method</span></span>

<span data-ttu-id="30f88-142">Изменения этой записи, внесенные через панель управления, вступают в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="30f88-142">Changes to this entry made through Control Panel take effect immediately.</span></span>

 

 



