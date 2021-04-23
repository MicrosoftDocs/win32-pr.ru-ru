---
title: Метод Play (устаревшие функции среды Windows)
description: Метод Play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691722"
---
# <a name="play-method-legacy-windows-environment-features"></a><span data-ttu-id="2aa1c-103">Метод Play (устаревшие функции среды Windows)</span><span class="sxs-lookup"><span data-stu-id="2aa1c-103">Play Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="2aa1c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2aa1c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2aa1c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="2aa1c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2aa1c-106">Воспроизводит указанную анимацию для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-106">Plays the specified animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="2aa1c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="2aa1c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2aa1c-108">\*Агент \***. Символы ("**_чарактерид_*_"). Воспроизвести_* "*аниматионнаме*"</span><span class="sxs-lookup"><span data-stu-id="2aa1c-108">*agent\***.Characters ("**_CharacterID_*_").Play_\* "*AnimationName*"</span></span>

</dd> </dl> 

| <span data-ttu-id="2aa1c-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="2aa1c-109">Part</span></span>            | <span data-ttu-id="2aa1c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2aa1c-110">Description</span></span>                                                          |
|-----------------|----------------------------------------------------------------------|
| <span data-ttu-id="2aa1c-111">*аниматионнаме*</span><span class="sxs-lookup"><span data-stu-id="2aa1c-111">*AnimationName*</span></span> | <span data-ttu-id="2aa1c-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-112">Required.</span></span> <span data-ttu-id="2aa1c-113">Строка, указывающая имя последовательности анимации.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-113">A string that specifies the name of an animation sequence.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2aa1c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2aa1c-114">Remarks</span></span>

<span data-ttu-id="2aa1c-115">Имя анимации определяется при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-115">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="2aa1c-116">Прежде чем воспроизводить указанную анимацию, сервер пытается воспроизвести анимацию **возврата** для предыдущей анимации, если она была назначена.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-116">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation, if one has been assigned.</span></span>

<span data-ttu-id="2aa1c-117">При доступе к анимации символа с помощью обычного файлового протокола можно просто использовать метод **Play** , указывающий имя анимации.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-117">When accessing a character's animations using a conventional file protocol, you can simply use the **Play** method specifying the name of the animation.</span></span> <span data-ttu-id="2aa1c-118">Однако при использовании протокола HTTP для доступа к данным анимации символов используйте метод **Get** для загрузки анимации перед вызовом метода **Play** .</span><span class="sxs-lookup"><span data-stu-id="2aa1c-118">However, if you are using the HTTP protocol to access character animation data, use the **Get** method to load the animation before calling the **Play** method.</span></span>

<span data-ttu-id="2aa1c-119">Дополнительные сведения см. в описании метода **Get** .</span><span class="sxs-lookup"><span data-stu-id="2aa1c-119">For more information, see the **Get** method.</span></span>

<span data-ttu-id="2aa1c-120">Чтобы упростить синтаксис, можно объявить ссылку на объект и задать для него ссылку на [**символьный**](/windows/desktop/lwef/the-characters-object) объект в коллекции [**символов**](/windows/desktop/lwef/the-characters-object) и использовать ссылку как часть операторов **Play** :</span><span class="sxs-lookup"><span data-stu-id="2aa1c-120">To simplify your syntax, you can declare an object reference and set it to reference the [**Character**](/windows/desktop/lwef/the-characters-object) object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection and use the reference as part of your **Play** statements:</span></span>


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



<span data-ttu-id="2aa1c-121">Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="2aa1c-121">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="2aa1c-122">Кроме того, если вы укажете незагруженную анимацию или не удалось загрузить символ, сервер устанавливает свойство [**Status**](status-property.md) объекта **запроса** в значение "Failed" с соответствующим номером ошибки.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-122">In addition, if you specify an animation that is not loaded or if the character has not been successfully loaded, the server sets the [**Status**](status-property.md) property of **Request** object to "failed" with an appropriate error number.</span></span> <span data-ttu-id="2aa1c-123">Однако если анимация не существует и данные этого символа уже были успешно загружены, сервер вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-123">However, if the animation does not exist and the character's data has already been successfully loaded, the server raises an error.</span></span>

<span data-ttu-id="2aa1c-124">Метод **Play** не делает символ видимым.</span><span class="sxs-lookup"><span data-stu-id="2aa1c-124">The **Play** method does not make the character visible.</span></span> <span data-ttu-id="2aa1c-125">Если символ не виден, сервер воспроизводит анимацию незаметно и задает свойство [**Status**](status-property.md) объекта [**request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="2aa1c-125">If the character is not visible, the server plays the animation invisibly, and sets the [**Status**](status-property.md) property of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 
