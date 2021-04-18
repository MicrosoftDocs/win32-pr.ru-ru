---
title: Вставить метод
description: Вставить метод
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681610"
---
# <a name="insert-method"></a><span data-ttu-id="e14e3-103">Вставить метод</span><span class="sxs-lookup"><span data-stu-id="e14e3-103">Insert Method</span></span>

<span data-ttu-id="e14e3-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e14e3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e14e3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="e14e3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e14e3-106">Вставляет объект **Command** в коллекцию **Commands** .</span><span class="sxs-lookup"><span data-stu-id="e14e3-106">Inserts a **Command** object in the **Commands** collection.</span></span>

</dd> <dt>

<span data-ttu-id="e14e3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e14e3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e14e3-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Commands. INSERT* \*  *имя*, *refname*, *до*\_</span><span class="sxs-lookup"><span data-stu-id="e14e3-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Insert*\* *Name*, *RefName*, *Before*\_</span></span>

<span data-ttu-id="e14e3-109">*Заголовок*, *речь, включено, видимый*</span><span class="sxs-lookup"><span data-stu-id="e14e3-109">*Caption*, *Voice, Enabled, Visible*</span></span>



| <span data-ttu-id="e14e3-110">Отделение</span><span class="sxs-lookup"><span data-stu-id="e14e3-110">Part</span></span>      | <span data-ttu-id="e14e3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e14e3-111">Description</span></span>                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e14e3-112">*Name*</span><span class="sxs-lookup"><span data-stu-id="e14e3-112">*Name*</span></span>    | <span data-ttu-id="e14e3-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e14e3-113">Required.</span></span> <span data-ttu-id="e14e3-114">Строковое значение, соответствующее ИДЕНТИФИКАТОРу, присваиваемому [**команде**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="e14e3-114">A string value corresponding to the ID you assign to the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="e14e3-115">*RefName*</span><span class="sxs-lookup"><span data-stu-id="e14e3-115">*RefName*</span></span> | <span data-ttu-id="e14e3-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e14e3-116">Required.</span></span> <span data-ttu-id="e14e3-117">Строковое значение, соответствующее имени (ID) команды, расположенной выше или ниже того места, где требуется вставить новую команду.</span><span class="sxs-lookup"><span data-stu-id="e14e3-117">A string value corresponding to the name (ID) of the command just above or below where you want to insert the new command.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="e14e3-118">*До*</span><span class="sxs-lookup"><span data-stu-id="e14e3-118">*Before*</span></span>  | <span data-ttu-id="e14e3-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e14e3-119">Optional.</span></span> <span data-ttu-id="e14e3-120">Логическое значение, указывающее, следует ли вставлять новую команду перед командой, заданной параметром *refname*.</span><span class="sxs-lookup"><span data-stu-id="e14e3-120">A Boolean value indicating whether to insert the new command before the command specified by *RefName*.</span></span> <span data-ttu-id="e14e3-121">**True** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e14e3-121">**True** (Default).</span></span> <span data-ttu-id="e14e3-122">Новая команда будет вставлена перед указанной командой.</span><span class="sxs-lookup"><span data-stu-id="e14e3-122">The new command will be inserted before the referenced command.</span></span><br/> <span data-ttu-id="e14e3-123">**Значение false** Новая команда будет вставлена после указанной команды.</span><span class="sxs-lookup"><span data-stu-id="e14e3-123">**False** The new command will be inserted after the referenced command.</span></span><br/> |
| <span data-ttu-id="e14e3-124">*Заголовок*</span><span class="sxs-lookup"><span data-stu-id="e14e3-124">*Caption*</span></span> | <span data-ttu-id="e14e3-125">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e14e3-125">Optional.</span></span> <span data-ttu-id="e14e3-126">Строковое значение, соответствующее имени, которое будет отображаться во всплывающем меню символа и в окне команд, если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="e14e3-126">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="e14e3-127">Дополнительные сведения см. в разделе свойство [**Caption**](caption-property.md)объекта [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="e14e3-127">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md)property.</span></span>    |
| <span data-ttu-id="e14e3-128">*Голосовая связь*</span><span class="sxs-lookup"><span data-stu-id="e14e3-128">*Voice*</span></span>   | <span data-ttu-id="e14e3-129">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e14e3-129">Optional.</span></span> <span data-ttu-id="e14e3-130">Строковое значение, соответствующее словам или фразе, используемым модулем распознавания речи для распознавания этой команды.</span><span class="sxs-lookup"><span data-stu-id="e14e3-130">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="e14e3-131">Дополнительные сведения о способах форматирования для строки см. в разделе свойство **Voice** объекта [**команды**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="e14e3-131">For more information on formatting alternatives for the string, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Voice** property.</span></span>                                  |
| <span data-ttu-id="e14e3-132">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="e14e3-132">*Enabled*</span></span> | <span data-ttu-id="e14e3-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e14e3-133">Optional.</span></span> <span data-ttu-id="e14e3-134">Логическое значение, указывающее, включена ли команда.</span><span class="sxs-lookup"><span data-stu-id="e14e3-134">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="e14e3-135">По умолчанию используется значение **True**.</span><span class="sxs-lookup"><span data-stu-id="e14e3-135">The default value is **True**.</span></span> <span data-ttu-id="e14e3-136">Дополнительные сведения см. в описании свойства **Enabled** объекта [**команды**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="e14e3-136">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Enabled** property.</span></span>                                                                                                  |
| <span data-ttu-id="e14e3-137">*Visible*</span><span class="sxs-lookup"><span data-stu-id="e14e3-137">*Visible*</span></span> | <span data-ttu-id="e14e3-138">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e14e3-138">Optional.</span></span> <span data-ttu-id="e14e3-139">Логическое значение, указывающее, видима ли команда в окне команд при входе в клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="e14e3-139">A Boolean value indicating whether the command is visible in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="e14e3-140">По умолчанию используется значение **True**.</span><span class="sxs-lookup"><span data-stu-id="e14e3-140">The default value is **True**.</span></span> <span data-ttu-id="e14e3-141">Дополнительные сведения см. в разделе свойство [**Visible**](visible-property.md) объекта [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="e14e3-141">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Visible**](visible-property.md) property.</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e14e3-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e14e3-142">Remarks</span></span>

<span data-ttu-id="e14e3-143">Значение свойства [**имени**](name-property.md) [**командного**](/windows/desktop/lwef/the-command-object) объекта должно быть уникальным в пределах коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e14e3-143">The value of a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Name**](name-property.md) property must be unique within its [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="e14e3-144">Перед созданием новой **команды** с тем же значением свойства **Name** необходимо удалить **команду** .</span><span class="sxs-lookup"><span data-stu-id="e14e3-144">You must remove a **Command** before you can create a new **Command** with the same **Name** property setting.</span></span> <span data-ttu-id="e14e3-145">Попытка создать **команду** с уже существующим свойством **Name** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e14e3-145">Attempting to create a **Command** with a **Name** property that already exists raises an error.</span></span>

<span data-ttu-id="e14e3-146">Этот метод также возвращает объект [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="e14e3-146">This method also returns a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="e14e3-147">Это позволяет объявить объект и назначить ему **команду** при вызове метода **INSERT** .</span><span class="sxs-lookup"><span data-stu-id="e14e3-147">This enables you to declare an object and assign a **Command** to it when you call the **Insert** method.</span></span>


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a><span data-ttu-id="e14e3-148">См. также:</span><span class="sxs-lookup"><span data-stu-id="e14e3-148">See Also</span></span>

<span data-ttu-id="e14e3-149">Метод [**Add**](add-method.md), [**метод Remove**](remove-method.md), [**метод RemoveAll**](removeall-method.md)</span><span class="sxs-lookup"><span data-stu-id="e14e3-149">[**Add method**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)</span></span>


 

