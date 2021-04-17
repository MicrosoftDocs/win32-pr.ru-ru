---
description: Интерфейс Иамтимелине предоставляет методы для управления временной шкалой, центральным объектом в службах редактирования Microsoft DirectShow (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Интерфейс Иамтимелине (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679794"
---
# <a name="iamtimeline-interface"></a><span data-ttu-id="0d5d2-103">Интерфейс Иамтимелине</span><span class="sxs-lookup"><span data-stu-id="0d5d2-103">IAMTimeline interface</span></span>

> [!Note]  
> <span data-ttu-id="0d5d2-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-104">\[Deprecated.</span></span> <span data-ttu-id="0d5d2-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d5d2-106">`IAMTimeline`Интерфейс предоставляет методы для управления временной шкалой, центральным объектом в [службах редактирования Microsoft DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-106">The `IAMTimeline` interface provides methods for manipulating the timeline, the central object in Microsoft [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="0d5d2-107">Временная шкала — это коллекция элементов, упорядоченных по времени, таких как видеоклипы, звуковые клипы, эффекты и переходы между клипами.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-107">A timeline is a collection of time-ordered elements, such as video clips, audio clips, effects, and transitions between clips.</span></span> <span data-ttu-id="0d5d2-108">Модуль подготовки отчетов использует временную шкалу для создания графа фильтра, из которого приложение может формировать отображаемые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-108">The render engine uses the timeline to create a filter graph, from which the application can generate the rendered output.</span></span>

<span data-ttu-id="0d5d2-109">`IAMTimeline` выполняет три основные службы.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-109">`IAMTimeline` performs three basic services.</span></span> <span data-ttu-id="0d5d2-110">Он</span><span class="sxs-lookup"><span data-stu-id="0d5d2-110">It</span></span>

-   <span data-ttu-id="0d5d2-111">Создает объекты на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-111">Creates the objects in the timeline.</span></span>
-   <span data-ttu-id="0d5d2-112">Выступает в качестве контейнера для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-112">Acts as a container for those objects.</span></span>
-   <span data-ttu-id="0d5d2-113">Задает и получает общие параметры временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-113">Sets and retrieves general parameters of the timeline.</span></span>

<span data-ttu-id="0d5d2-114">Чтобы создать объект временной шкалы, вызовите **CoCreateInstance** с идентификатором класса CLSID \_ амтимелине.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-114">To create the timeline object, call **CoCreateInstance** with the class identifier CLSID\_AMTimeline.</span></span>

## <a name="members"></a><span data-ttu-id="0d5d2-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="0d5d2-115">Members</span></span>

<span data-ttu-id="0d5d2-116">Интерфейс **иамтимелине** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0d5d2-116">The **IAMTimeline** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0d5d2-117">**Иамтимелине** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0d5d2-117">**IAMTimeline** also has these types of members:</span></span>

-   [<span data-ttu-id="0d5d2-118">Методы</span><span class="sxs-lookup"><span data-stu-id="0d5d2-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0d5d2-119">Методы</span><span class="sxs-lookup"><span data-stu-id="0d5d2-119">Methods</span></span>

<span data-ttu-id="0d5d2-120">Интерфейс **иамтимелине** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-120">The **IAMTimeline** interface has these methods.</span></span>



| <span data-ttu-id="0d5d2-121">Метод</span><span class="sxs-lookup"><span data-stu-id="0d5d2-121">Method</span></span>                                                             | <span data-ttu-id="0d5d2-122">Описание</span><span class="sxs-lookup"><span data-stu-id="0d5d2-122">Description</span></span>                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d5d2-123">**AddGroup**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-123">**AddGroup**</span></span>](iamtimeline-addgroup.md)                           | <span data-ttu-id="0d5d2-124">Добавляет группу на временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-124">Adds a group to the timeline.</span></span><br/>                                                                                          |
| [<span data-ttu-id="0d5d2-125">**клеараллграупс**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-125">**ClearAllGroups**</span></span>](iamtimeline-clearallgroups.md)               | <span data-ttu-id="0d5d2-126">Удаляет все группы из временной шкалы, а также все объекты, содержащиеся в этих группах.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-126">Removes all groups from the timeline, along with all objects contained in those groups.</span></span><br/>                                |
| [<span data-ttu-id="0d5d2-127">**креатимптиноде**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-127">**CreateEmptyNode**</span></span>](iamtimeline-createemptynode.md)             | <span data-ttu-id="0d5d2-128">Создает новый объект временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-128">Creates a new timeline object.</span></span><br/>                                                                                         |
| [<span data-ttu-id="0d5d2-129">**еффектсенаблед**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-129">**EffectsEnabled**</span></span>](iamtimeline-effectsenabled.md)               | <span data-ttu-id="0d5d2-130">Определяет, включены ли эффекты.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-130">Determines whether effects are enabled.</span></span><br/>                                                                                |
| [<span data-ttu-id="0d5d2-131">**енаблиффектс**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-131">**EnableEffects**</span></span>](iamtimeline-enableeffects.md)                 | <span data-ttu-id="0d5d2-132">Включает или отключает все эффекты на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-132">Enables or disables all effects in the timeline.</span></span><br/>                                                                       |
| [<span data-ttu-id="0d5d2-133">**енаблетранситионс**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-133">**EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)         | <span data-ttu-id="0d5d2-134">Включает или отключает все переходы на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-134">Enables or disables all transitions in the timeline.</span></span><br/>                                                                   |
| [<span data-ttu-id="0d5d2-135">**жеткаунтофтипе**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-135">**GetCountOfType**</span></span>](iamtimeline-getcountoftype.md)               | <span data-ttu-id="0d5d2-136">Извлекает количество объектов указанного типа, содержащихся в указанной группе и всех ее дочерних элементах.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-136">Retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span><br/> |
| [<span data-ttu-id="0d5d2-137">**жетдефаултеффект**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-137">**GetDefaultEffect**</span></span>](iamtimeline-getdefaulteffect.md)           | <span data-ttu-id="0d5d2-138">Возвращает результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-138">Retrieves the default effect.</span></span><br/>                                                                                          |
| [<span data-ttu-id="0d5d2-139">**жетдефаултеффектб**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-139">**GetDefaultEffectB**</span></span>](iamtimeline-getdefaulteffectb.md)         | <span data-ttu-id="0d5d2-140">Получает результат по умолчанию в виде значения **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="0d5d2-140">Retrieves the default effect as a **BSTR** value.</span></span><br/>                                                                      |
| [<span data-ttu-id="0d5d2-141">**жетдефаултфпс**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-141">**GetDefaultFPS**</span></span>](iamtimeline-getdefaultfps.md)                 | <span data-ttu-id="0d5d2-142">Возвращает частоту кадров вывода по умолчанию в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-142">Retrieves the default output frame rate, in frames per second.</span></span><br/>                                                         |
| [<span data-ttu-id="0d5d2-143">**жетдефаулттранситион**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-143">**GetDefaultTransition**</span></span>](iamtimeline-getdefaulttransition.md)   | <span data-ttu-id="0d5d2-144">Извлекает переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-144">Retrieves the default transition.</span></span><br/>                                                                                      |
| [<span data-ttu-id="0d5d2-145">**жетдефаулттранситионб**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-145">**GetDefaultTransitionB**</span></span>](iamtimeline-getdefaulttransitionb.md) | <span data-ttu-id="0d5d2-146">Извлекает переход по умолчанию в виде значения **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="0d5d2-146">Retrieves the default transition as a **BSTR** value.</span></span><br/>                                                                  |
| [<span data-ttu-id="0d5d2-147">**жетдиртиранже**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-147">**GetDirtyRange**</span></span>](iamtimeline-getdirtyrange.md)                 | <span data-ttu-id="0d5d2-148">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-148">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="0d5d2-149">**Длительное время**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-149">**GetDuration**</span></span>](iamtimeline-getduration.md)                     | <span data-ttu-id="0d5d2-150">Возвращает длительность временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-150">Retrieves the timeline duration.</span></span><br/>                                                                                       |
| [<span data-ttu-id="0d5d2-151">**GetDuration2**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-151">**GetDuration2**</span></span>](iamtimeline-getduration2.md)                   | <span data-ttu-id="0d5d2-152">Получает длительность временной шкалы в виде **Double**.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-152">Retrieves the timeline duration as a **double**.</span></span><br/>                                                                       |
| [<span data-ttu-id="0d5d2-153">**Группа**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-153">**GetGroup**</span></span>](iamtimeline-getgroup.md)                           | <span data-ttu-id="0d5d2-154">Извлекает указанную группу.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-154">Retrieves a specified group.</span></span><br/>                                                                                           |
| [<span data-ttu-id="0d5d2-155">**жетграупкаунт**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-155">**GetGroupCount**</span></span>](iamtimeline-getgroupcount.md)                 | <span data-ttu-id="0d5d2-156">Извлекает количество групп, содержащихся на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-156">Retrieves the number of groups that are contained in the timeline.</span></span><br/>                                                     |
| [<span data-ttu-id="0d5d2-157">**жетинсертмоде**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-157">**GetInsertMode**</span></span>](iamtimeline-getinsertmode.md)                 | <span data-ttu-id="0d5d2-158">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-158">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="0d5d2-159">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-159">**IsDirty**</span></span>](iamtimeline-isdirty.md)                             | <span data-ttu-id="0d5d2-160">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-160">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="0d5d2-161">**ремграупфромлист**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-161">**RemGroupFromList**</span></span>](iamtimeline-remgroupfromlist.md)           | <span data-ttu-id="0d5d2-162">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-162">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="0d5d2-163">**сетдефаултеффект**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-163">**SetDefaultEffect**</span></span>](iamtimeline-setdefaulteffect.md)           | <span data-ttu-id="0d5d2-164">Задает результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-164">Sets the default effect.</span></span><br/>                                                                                               |
| [<span data-ttu-id="0d5d2-165">**сетдефаултеффектб**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-165">**SetDefaultEffectB**</span></span>](iamtimeline-setdefaulteffectb.md)         | <span data-ttu-id="0d5d2-166">Устанавливает результат по умолчанию как значение **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="0d5d2-166">Sets the default effect as a **BSTR** value.</span></span><br/>                                                                           |
| [<span data-ttu-id="0d5d2-167">**сетдефаултфпс**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-167">**SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)                 | <span data-ttu-id="0d5d2-168">Задает частоту кадров вывода по умолчанию в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-168">Sets the default output frame rate, in frames per second.</span></span><br/>                                                              |
| [<span data-ttu-id="0d5d2-169">**сетдефаулттранситион**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-169">**SetDefaultTransition**</span></span>](iamtimeline-setdefaulttransition.md)   | <span data-ttu-id="0d5d2-170">Задает переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-170">Sets the default transition.</span></span><br/>                                                                                           |
| [<span data-ttu-id="0d5d2-171">**сетдефаулттранситионб**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-171">**SetDefaultTransitionB**</span></span>](iamtimeline-setdefaulttransitionb.md) | <span data-ttu-id="0d5d2-172">Задает переход по умолчанию в качестве значения BSTR.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-172">Sets the default transition as a BSTR value.</span></span><br/>                                                                           |
| [<span data-ttu-id="0d5d2-173">**сетинсертмоде**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-173">**SetInsertMode**</span></span>](iamtimeline-setinsertmode.md)                 | <span data-ttu-id="0d5d2-174">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-174">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="0d5d2-175">**сетинтерестранже**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-175">**SetInterestRange**</span></span>](iamtimeline-setinterestrange.md)           | <span data-ttu-id="0d5d2-176">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-176">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="0d5d2-177">**транситионсенаблед**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-177">**TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)       | <span data-ttu-id="0d5d2-178">Определяет, включены ли переходы.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-178">Determines whether transitions are enabled.</span></span><br/>                                                                            |
| [<span data-ttu-id="0d5d2-179">**валидатесаурценамес**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-179">**ValidateSourceNames**</span></span>](iamtimeline-validatesourcenames.md)     | <span data-ttu-id="0d5d2-180">Проверяет имена источников на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-180">Validates source names in the timeline.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="0d5d2-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d5d2-181">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0d5d2-182">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-182">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0d5d2-183">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-183">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0d5d2-184">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-184">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d5d2-185">Требования</span><span class="sxs-lookup"><span data-stu-id="0d5d2-185">Requirements</span></span>



| <span data-ttu-id="0d5d2-186">Требование</span><span class="sxs-lookup"><span data-stu-id="0d5d2-186">Requirement</span></span> | <span data-ttu-id="0d5d2-187">Значение</span><span class="sxs-lookup"><span data-stu-id="0d5d2-187">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5d2-188">Header</span><span class="sxs-lookup"><span data-stu-id="0d5d2-188">Header</span></span><br/>  | <dl> <span data-ttu-id="0d5d2-189"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d5d2-189"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0d5d2-190">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d5d2-190">Library</span></span><br/> | <dl> <span data-ttu-id="0d5d2-191"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d5d2-191"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
