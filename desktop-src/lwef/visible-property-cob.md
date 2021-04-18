---
title: Свойство Visible (объект characters)
description: Свойство Visible
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691718"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="5d202-103">Свойство Visible (объект characters)</span><span class="sxs-lookup"><span data-stu-id="5d202-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="5d202-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d202-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5d202-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="5d202-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5d202-106">Возвращает логическое значение, указывающее, является ли символ видимым.</span><span class="sxs-lookup"><span data-stu-id="5d202-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="5d202-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="5d202-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="5d202-108">\*Агент \***. Символы (**"\* чарактерид *" \* *). Видимый**</span><span class="sxs-lookup"><span data-stu-id="5d202-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="5d202-109">Значение</span><span class="sxs-lookup"><span data-stu-id="5d202-109">Value</span></span> | <span data-ttu-id="5d202-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5d202-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="5d202-111">True</span><span class="sxs-lookup"><span data-stu-id="5d202-111">True</span></span>  | <span data-ttu-id="5d202-112">Отображается символ.</span><span class="sxs-lookup"><span data-stu-id="5d202-112">The character is displayed.</span></span>            |
| <span data-ttu-id="5d202-113">Неверно</span><span class="sxs-lookup"><span data-stu-id="5d202-113">False</span></span> | <span data-ttu-id="5d202-114">Символ скрыт (невидимый).</span><span class="sxs-lookup"><span data-stu-id="5d202-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d202-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d202-115">Remarks</span></span>

<span data-ttu-id="5d202-116">Это свойство указывает, отображается ли кадр символа.</span><span class="sxs-lookup"><span data-stu-id="5d202-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="5d202-117">Это не обязательно означает, что на экране есть изображение.</span><span class="sxs-lookup"><span data-stu-id="5d202-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="5d202-118">Например, это свойство возвращает **значение true** , даже если символ находится вне видимой области отображения или если текущая символьная рамка не содержит изображений.</span><span class="sxs-lookup"><span data-stu-id="5d202-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="5d202-119">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="5d202-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="5d202-120">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5d202-120">This property is read-only.</span></span> <span data-ttu-id="5d202-121">Чтобы сделать символ видимым или скрытым, используйте методы [**Показать**](show-method.md) или [**Скрыть**](https://www.bing.com/search?q=**Hide**) .</span><span class="sxs-lookup"><span data-stu-id="5d202-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




