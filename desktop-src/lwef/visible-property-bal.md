---
title: Свойство Visible (объект всплывающего объекта)
description: Свойство Visible
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070925"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="3d666-103">Свойство Visible (объект всплывающего объекта)</span><span class="sxs-lookup"><span data-stu-id="3d666-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="3d666-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3d666-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3d666-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="3d666-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3d666-106">Возвращает или задает видимый параметр для всплывающего окна для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="3d666-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="3d666-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3d666-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="3d666-108">\*Агент \***. Символы (**"\* чарактерид \*" \* *). Повсплывающее. видимое* \*  \[  =  *логическое значение*\]</span><span class="sxs-lookup"><span data-stu-id="3d666-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="3d666-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="3d666-109">Part</span></span>      | <span data-ttu-id="3d666-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3d666-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d666-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="3d666-111">*boolean*</span></span> | <span data-ttu-id="3d666-112">Логическое выражение, указывающее, отображается ли всплывающее сообщение в слове.</span><span class="sxs-lookup"><span data-stu-id="3d666-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="3d666-113">**Значение true** Всплывающее сообщение отображается.</span><span class="sxs-lookup"><span data-stu-id="3d666-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="3d666-114">**Значение false** Всплывающее сообщение скрыто.</span><span class="sxs-lookup"><span data-stu-id="3d666-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d666-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d666-115">Remarks</span></span>

<span data-ttu-id="3d666-116">Если [**следовать за вызовом**](speak-method.md) или [**подумать**](think-method.md) с оператором, который пытается изменить свойство всплывающего окна, это может не повлиять на видимое состояние всплывающего окна из-за того, что вызов **говорите** или **считает** в очереди, но параметр вызова видимого состояния всплывающего окна не имеет.</span><span class="sxs-lookup"><span data-stu-id="3d666-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="3d666-117">Таким образом, это значение задается только в том случае, если в очереди символов нет вызовов **говорите** или **обработки** .</span><span class="sxs-lookup"><span data-stu-id="3d666-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="3d666-118">Если вы попытаетесь установить это свойство в то время, когда символ говорит, перемещается или перетаскивается, Настройка свойства не вступит в силу до завершения предыдущей операции.</span><span class="sxs-lookup"><span data-stu-id="3d666-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="3d666-119">Вызов метода [**говорите**](speak-method.md) и [**мышления**](think-method.md) автоматически делает видимым всплывающее сообщение, устанавливая для свойства [**Visible**](visible-property.md) значение **true**.</span><span class="sxs-lookup"><span data-stu-id="3d666-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="3d666-120">Если свойство автоскрытия текста символа включено, то после выхода из него всплывающее сообщение автоматически скрывается.</span><span class="sxs-lookup"><span data-stu-id="3d666-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="3d666-121">При щелчке или перетаскивании символа, который в настоящий момент не говорит, автоматически скрывается, даже если параметр автоскрытия отключен.</span><span class="sxs-lookup"><span data-stu-id="3d666-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="3d666-122">Параметр автоскрытия символа можно изменить с помощью свойства [**стиля**](style-property.md) всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="3d666-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="3d666-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="3d666-123">See Also</span></span>

[<span data-ttu-id="3d666-124">**Свойство Style**</span><span class="sxs-lookup"><span data-stu-id="3d666-124">**Style property**</span></span>](style-property.md)


 

 





