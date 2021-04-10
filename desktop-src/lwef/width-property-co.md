---
title: Свойство Width (объект characters)
description: Width, свойство
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070974"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="47711-103">Свойство Width (объект characters)</span><span class="sxs-lookup"><span data-stu-id="47711-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="47711-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47711-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="47711-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="47711-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="47711-106">Возвращает или задает ширину кадра для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="47711-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="47711-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="47711-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="47711-108">\*Агент \***. Символы ("**_чарактерид_\*_")._ \*  \[ =  *Значение* ширины\]</span><span class="sxs-lookup"><span data-stu-id="47711-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="47711-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="47711-109">Part</span></span>    | <span data-ttu-id="47711-110">Описание</span><span class="sxs-lookup"><span data-stu-id="47711-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="47711-111">*value*</span><span class="sxs-lookup"><span data-stu-id="47711-111">*value*</span></span> | <span data-ttu-id="47711-112">Длинное целое число, указывающее ширину кадра символа.</span><span class="sxs-lookup"><span data-stu-id="47711-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47711-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47711-113">Remarks</span></span>

<span data-ttu-id="47711-114">Свойство [**Width**](width-property.md) всегда выражается в пикселях.</span><span class="sxs-lookup"><span data-stu-id="47711-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="47711-115">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="47711-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="47711-116">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="47711-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




