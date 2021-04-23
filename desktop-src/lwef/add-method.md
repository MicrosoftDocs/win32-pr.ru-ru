---
title: Добавить метод.
description: Добавить метод.
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067862"
---
# <a name="add-method"></a><span data-ttu-id="3a0b0-103">Добавить метод.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-103">Add Method</span></span>

<span data-ttu-id="3a0b0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3a0b0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3a0b0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="3a0b0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b0-106">Добавляет объект [Command](the-command-object.md) в коллекцию [Commands](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0b0-106">Adds a [Command](the-command-object.md) object to the [Commands](the-commands-collection-object.md) collection.</span></span>

</dd> <dt>

<span data-ttu-id="3a0b0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3a0b0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b0-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Команды. Добавление* \*  *имени*, *заголовка*, *голоса*, *включенного*, *видимого*</span><span class="sxs-lookup"><span data-stu-id="3a0b0-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Add*\* *Name*, *Caption*, *Voice*, *Enabled*, *Visible*</span></span>



| <span data-ttu-id="3a0b0-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="3a0b0-109">Part</span></span>      | <span data-ttu-id="3a0b0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3a0b0-110">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0b0-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="3a0b0-111">*Name*</span></span>    | <span data-ttu-id="3a0b0-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-112">Required.</span></span> <span data-ttu-id="3a0b0-113">Строковое значение, соответствующее ИДЕНТИФИКАТОРу, присваиваемому команде.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-113">A string value corresponding to the ID you assign for the command.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="3a0b0-114">*Заголовок*</span><span class="sxs-lookup"><span data-stu-id="3a0b0-114">*Caption*</span></span> | <span data-ttu-id="3a0b0-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-115">Optional.</span></span> <span data-ttu-id="3a0b0-116">Строковое значение, соответствующее имени, которое будет отображаться во всплывающем меню символа и в окне команд, если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-116">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="3a0b0-117">Дополнительные сведения см. в разделе свойство [Caption](caption-property.md) объекта [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0b0-117">For more information, see the [Command](the-command-object.md) object's [Caption](caption-property.md) property.</span></span>                       |
| <span data-ttu-id="3a0b0-118">*Голосовая связь*</span><span class="sxs-lookup"><span data-stu-id="3a0b0-118">*Voice*</span></span>   | <span data-ttu-id="3a0b0-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-119">Optional.</span></span> <span data-ttu-id="3a0b0-120">Строковое значение, соответствующее словам или фразе, используемым модулем распознавания речи для распознавания этой команды.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-120">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="3a0b0-121">Дополнительные сведения о способах форматирования для строки см. в разделе свойство [Voice](voice-property.md) объекта [команды](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0b0-121">For more information on formatting alternatives for the string, see the [Command](the-command-object.md) object's [Voice](voice-property.md) property.</span></span>                                |
| <span data-ttu-id="3a0b0-122">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="3a0b0-122">*Enabled*</span></span> | <span data-ttu-id="3a0b0-123">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-123">Optional.</span></span> <span data-ttu-id="3a0b0-124">Логическое значение, указывающее, включена ли команда.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-124">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="3a0b0-125">По умолчанию используется значение **True**.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-125">The default value is **True**.</span></span> <span data-ttu-id="3a0b0-126">Дополнительные сведения см. в описании свойства [Enabled](enabled-property.md) объекта [команды](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0b0-126">For more information, see the [Command](the-command-object.md) object's [Enabled](enabled-property.md) property.</span></span>                                                                                              |
| <span data-ttu-id="3a0b0-127">*Visible*</span><span class="sxs-lookup"><span data-stu-id="3a0b0-127">*Visible*</span></span> | <span data-ttu-id="3a0b0-128">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-128">Optional.</span></span> <span data-ttu-id="3a0b0-129">Логическое значение, указывающее, отображается ли команда во всплывающем меню символа, если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-129">A Boolean value indicating whether the command is visible in the character's pop-up menu for the character when the client application is input-active.</span></span> <span data-ttu-id="3a0b0-130">По умолчанию используется значение **True**.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-130">The default value is **True**.</span></span> <span data-ttu-id="3a0b0-131">Дополнительные сведения см. в разделе свойство [Visible](visible-property.md) объекта [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0b0-131">For more information, see the [Command](the-command-object.md) object's [Visible](visible-property.md) property.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a0b0-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a0b0-132">Remarks</span></span>

<span data-ttu-id="3a0b0-133">Значение свойства [имени](name-property.md) [командного](the-command-object.md) объекта должно быть уникальным в пределах коллекции [Commands](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0b0-133">The value of a [Command](the-command-object.md) object's [Name](name-property.md) property must be unique within its [Commands](the-commands-collection-object.md) collection.</span></span> <span data-ttu-id="3a0b0-134">Перед созданием новой команды с тем же значением свойства Name необходимо удалить команду.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-134">You must remove a Command before you can create a new Command with the same Name property setting.</span></span> <span data-ttu-id="3a0b0-135">Попытка создать команду с уже существующим свойством Name вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-135">Attempting to create a Command with a Name property that already exists raises an error.</span></span>

<span data-ttu-id="3a0b0-136">Этот метод также возвращает объект [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0b0-136">This method also returns a [Command](the-command-object.md) object.</span></span> <span data-ttu-id="3a0b0-137">Это позволяет объявить объект и назначить ему команду при вызове addMethod.</span><span class="sxs-lookup"><span data-stu-id="3a0b0-137">This enables you to declare an object and assign a Command to it when you call the Addmethod.</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a><span data-ttu-id="3a0b0-138">См. также</span><span class="sxs-lookup"><span data-stu-id="3a0b0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a0b0-139">**Вставить метод**</span><span class="sxs-lookup"><span data-stu-id="3a0b0-139">**Insert method**</span></span>](insert-method.md)
</dt> <dt>

[<span data-ttu-id="3a0b0-140">**RemoveAll, метод**</span><span class="sxs-lookup"><span data-stu-id="3a0b0-140">**RemoveAll method**</span></span>](removeall-method.md)
</dt> <dt>

[<span data-ttu-id="3a0b0-141">**Remove - метод**</span><span class="sxs-lookup"><span data-stu-id="3a0b0-141">**Remove method**</span></span>](remove-method.md)
</dt> </dl>

 

 




