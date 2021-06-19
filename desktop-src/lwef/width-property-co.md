---
title: Свойство Width (объект characters)
description: Сведения о свойстве Width объекта Characters, который возвращает или задает ширину кадра для указанного символа.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395130"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="f8eb0-103">Свойство Width (объект characters)</span><span class="sxs-lookup"><span data-stu-id="f8eb0-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="f8eb0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f8eb0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f8eb0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f8eb0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f8eb0-106">Возвращает или задает ширину кадра для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="f8eb0-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="f8eb0-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f8eb0-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="f8eb0-108">\*Агент \***. Символы ("**_чарактерид_\*_")._ \*  \[ =  *Значение* ширины\]</span><span class="sxs-lookup"><span data-stu-id="f8eb0-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="f8eb0-109">Часть</span><span class="sxs-lookup"><span data-stu-id="f8eb0-109">Part</span></span>    | <span data-ttu-id="f8eb0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f8eb0-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="f8eb0-111">*value*</span><span class="sxs-lookup"><span data-stu-id="f8eb0-111">*value*</span></span> | <span data-ttu-id="f8eb0-112">Длинное целое число, указывающее ширину кадра символа.</span><span class="sxs-lookup"><span data-stu-id="f8eb0-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8eb0-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="f8eb0-113">Remarks</span></span>

<span data-ttu-id="f8eb0-114">Свойство [**Width**](width-property.md) всегда выражается в пикселях.</span><span class="sxs-lookup"><span data-stu-id="f8eb0-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="f8eb0-115">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="f8eb0-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="f8eb0-116">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f8eb0-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




