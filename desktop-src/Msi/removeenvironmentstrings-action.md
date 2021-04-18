---
description: Действие Ремовинвиронментстрингс изменяет значения переменных среды.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Действие Ремовинвиронментстрингс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674502"
---
# <a name="removeenvironmentstrings-action"></a><span data-ttu-id="4d050-103">Действие Ремовинвиронментстрингс</span><span class="sxs-lookup"><span data-stu-id="4d050-103">RemoveEnvironmentStrings Action</span></span>

<span data-ttu-id="4d050-104">Действие Ремовинвиронментстрингс изменяет значения переменных среды.</span><span class="sxs-lookup"><span data-stu-id="4d050-104">The RemoveEnvironmentStrings action modifies the values of environment variables.</span></span>

<span data-ttu-id="4d050-105">Обратите внимание, что переменные среды не меняются для выполняемой установки при выполнении действия [вритинвиронментстрингс](writeenvironmentstrings-action.md) или ремовинвиронментстрингс.</span><span class="sxs-lookup"><span data-stu-id="4d050-105">Note that environment variables do not change for the installation in progress when either the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) or RemoveEnvironmentStrings action are run.</span></span> <span data-ttu-id="4d050-106">В Windows 2000 эта информация хранится в реестре и отправляется сообщение для уведомления системы об изменениях после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="4d050-106">On Windows 2000, this information is stored in the registry and a message is sent to notify the system of changes when the installation completes.</span></span> <span data-ttu-id="4d050-107">Новый процесс или другой процесс, проверяющий эти сообщения, будет использовать новые переменные среды.</span><span class="sxs-lookup"><span data-stu-id="4d050-107">A new process, or another process that checks for these messages, will use the new environment variables.</span></span>

<span data-ttu-id="4d050-108">Установщик запускает [действие вритинвиронментстрингс](writeenvironmentstrings-action.md) только во время установки или переустановки компонента и запускает действие ремовинвиронментстрингс только во время удаления компонента.</span><span class="sxs-lookup"><span data-stu-id="4d050-108">The installer runs the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) only during the installation or reinstallation of a component, and runs the RemoveEnvironmentStrings action only during the removal of a component.</span></span>

<span data-ttu-id="4d050-109">Значения записываются или удаляются в зависимости от выбора основных действий и модификаторов.</span><span class="sxs-lookup"><span data-stu-id="4d050-109">Values are written or removed based on the selection of primary actions and modifiers.</span></span> <span data-ttu-id="4d050-110">Они описаны в следующем разделе Актиондата messages.</span><span class="sxs-lookup"><span data-stu-id="4d050-110">These are described in the following ActionData Messages section.</span></span> <span data-ttu-id="4d050-111">Обратите внимание, что в зависимости от указанного действия Вритинвиронментстрингс может удалить переменные, и Ремовинвиронментстрингс может добавить их на основе создания [таблицы среды](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="4d050-111">Note that depending upon the action specified, WriteEnvironmentStrings may remove variables, and RemoveEnvironmentStrings may add them based on the authoring of the [Environment table](environment-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4d050-112">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="4d050-112">Sequence Restrictions</span></span>

<span data-ttu-id="4d050-113">[Действие инсталлвалидате](installvalidate-action.md) должно быть выполнено перед действием ремовинвиронментстрингс.</span><span class="sxs-lookup"><span data-stu-id="4d050-113">The [InstallValidate action](installvalidate-action.md) must be executed before the RemoveEnvironmentStrings action.</span></span> <span data-ttu-id="4d050-114">Поскольку действие Вритинвиронментстрингс и действие Ремовинвиронментстрингс никогда не применяются во время установки или удаления компонента, их относительная последовательность не ограничена.</span><span class="sxs-lookup"><span data-stu-id="4d050-114">Because the WriteEnvironmentStrings action and RemoveEnvironmentStrings action are never both applied during the installation or removal of a component, their relative sequence is not restricted.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4d050-115">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="4d050-115">ActionData Messages</span></span>



| <span data-ttu-id="4d050-116">Поле</span><span class="sxs-lookup"><span data-stu-id="4d050-116">Field</span></span> | <span data-ttu-id="4d050-117">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="4d050-117">Description of action data</span></span>                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d050-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4d050-118">\[1\]</span></span> | <span data-ttu-id="4d050-119">Имя изменяемой переменной среды.</span><span class="sxs-lookup"><span data-stu-id="4d050-119">Name of the environment variable to modify.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="4d050-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="4d050-120">\[2\]</span></span> | <span data-ttu-id="4d050-121">Значение переменной среды.</span><span class="sxs-lookup"><span data-stu-id="4d050-121">The environment variable value.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="4d050-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="4d050-122">\[3\]</span></span> | <span data-ttu-id="4d050-123">Это поле битовых флагов, определяющих выполняемое действие.</span><span class="sxs-lookup"><span data-stu-id="4d050-123">This is a field of bit flags that specify the action to be performed.</span></span> <span data-ttu-id="4d050-124">Включайте только один бит для первичного действия.</span><span class="sxs-lookup"><span data-stu-id="4d050-124">Include only one bit for a primary action.</span></span> <span data-ttu-id="4d050-125">В это поле может быть включена более одного бита модификатора.</span><span class="sxs-lookup"><span data-stu-id="4d050-125">There may be more than one modifier bit included in this field.</span></span> <span data-ttu-id="4d050-126">См. следующие описания битовых флагов.</span><span class="sxs-lookup"><span data-stu-id="4d050-126">See the following bit flag descriptions.</span></span> |



 



| <span data-ttu-id="4d050-127">Битовое значение</span><span class="sxs-lookup"><span data-stu-id="4d050-127">Bit value</span></span> | <span data-ttu-id="4d050-128">Описание основных действий</span><span class="sxs-lookup"><span data-stu-id="4d050-128">Description of primary actions</span></span>                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d050-129">0x1</span><span class="sxs-lookup"><span data-stu-id="4d050-129">0x1</span></span>       | <span data-ttu-id="4d050-130">Задано.</span><span class="sxs-lookup"><span data-stu-id="4d050-130">Set.</span></span> <span data-ttu-id="4d050-131">Задает значение переменной среды во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="4d050-131">Sets the value of the environment variable in all cases.</span></span><br/> <span data-ttu-id="4d050-132">Если этот бит сочетается с битом модификатора Append или prefix, действие добавляет значение к любому существующему значению в переменной.</span><span class="sxs-lookup"><span data-stu-id="4d050-132">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/> |
| <span data-ttu-id="4d050-133">0x2</span><span class="sxs-lookup"><span data-stu-id="4d050-133">0x2</span></span>       | <span data-ttu-id="4d050-134">Задано.</span><span class="sxs-lookup"><span data-stu-id="4d050-134">Set.</span></span> <span data-ttu-id="4d050-135">Задает значение, если переменная отсутствует.</span><span class="sxs-lookup"><span data-stu-id="4d050-135">Sets the value if the variable is absent.</span></span><br/> <span data-ttu-id="4d050-136">Если этот бит сочетается с битом модификатора Append или prefix, действие добавляет значение к любому существующему значению в переменной.</span><span class="sxs-lookup"><span data-stu-id="4d050-136">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/>                |
| <span data-ttu-id="4d050-137">0x4</span><span class="sxs-lookup"><span data-stu-id="4d050-137">0x4</span></span>       | <span data-ttu-id="4d050-138">Удалить.</span><span class="sxs-lookup"><span data-stu-id="4d050-138">Remove.</span></span> <span data-ttu-id="4d050-139">Удаляет значение из переменной.</span><span class="sxs-lookup"><span data-stu-id="4d050-139">Removes the value from the variable.</span></span><br/> <span data-ttu-id="4d050-140">Если этот бит сочетается с битом модификатора Append или prefix, значение удаляется из существующей строки, если значение существует.</span><span class="sxs-lookup"><span data-stu-id="4d050-140">If this bit is combined with an Append or Prefix modifier bit, the value is removed from the existing string, if the value exists.</span></span><br/>               |



 



| <span data-ttu-id="4d050-141">Битовое значение</span><span class="sxs-lookup"><span data-stu-id="4d050-141">Bit value</span></span>  | <span data-ttu-id="4d050-142">Описание модификатора</span><span class="sxs-lookup"><span data-stu-id="4d050-142">Description of modifier</span></span>                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d050-143">0x20000000</span><span class="sxs-lookup"><span data-stu-id="4d050-143">0x20000000</span></span> | <span data-ttu-id="4d050-144">Если этот бит задан, действия применяются к переменным среды компьютера.</span><span class="sxs-lookup"><span data-stu-id="4d050-144">If this bit is set, actions are applied to the machine environment variables.</span></span><br/> <span data-ttu-id="4d050-145">Если этот бит не задан, действия применяются к переменным среды пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d050-145">If this bit is not set, actions are applied to the user's environment variables.</span></span><br/> |
| <span data-ttu-id="4d050-146">0x40000000</span><span class="sxs-lookup"><span data-stu-id="4d050-146">0x40000000</span></span> | <span data-ttu-id="4d050-147">Добавить.</span><span class="sxs-lookup"><span data-stu-id="4d050-147">Append.</span></span> <span data-ttu-id="4d050-148">Этот бит является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4d050-148">This bit is optional.</span></span> <span data-ttu-id="4d050-149">Не задавайте модификаторы Append и prefix.</span><span class="sxs-lookup"><span data-stu-id="4d050-149">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |
| <span data-ttu-id="4d050-150">0x80000000</span><span class="sxs-lookup"><span data-stu-id="4d050-150">0x80000000</span></span> | <span data-ttu-id="4d050-151">Prefix.</span><span class="sxs-lookup"><span data-stu-id="4d050-151">Prefix.</span></span> <span data-ttu-id="4d050-152">Этот бит является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4d050-152">This bit is optional.</span></span> <span data-ttu-id="4d050-153">Не задавайте модификаторы Append и prefix.</span><span class="sxs-lookup"><span data-stu-id="4d050-153">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |



 

 

 




