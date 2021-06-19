---
title: Свойство Top (объект characters)
description: Сведения о свойстве Top (объект characters). Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396349"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="47b94-104">Свойство Top (объект characters)</span><span class="sxs-lookup"><span data-stu-id="47b94-104">Top Property (Characters Object)</span></span>

<span data-ttu-id="47b94-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47b94-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="47b94-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="47b94-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="47b94-107">Возвращает или задает верхний край указанного кадра символа.</span><span class="sxs-lookup"><span data-stu-id="47b94-107">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="47b94-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="47b94-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="47b94-109">\*Агент \***. Символы ("**_чарактерид_\*_"). Верхнее_ \*  \[  =  *значение*\]</span><span class="sxs-lookup"><span data-stu-id="47b94-109">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="47b94-110">Часть</span><span class="sxs-lookup"><span data-stu-id="47b94-110">Part</span></span>    | <span data-ttu-id="47b94-111">Описание</span><span class="sxs-lookup"><span data-stu-id="47b94-111">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="47b94-112">*value*</span><span class="sxs-lookup"><span data-stu-id="47b94-112">*value*</span></span> | <span data-ttu-id="47b94-113">Длинное целое число, указывающее верхнюю границу символа.</span><span class="sxs-lookup"><span data-stu-id="47b94-113">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47b94-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="47b94-114">Remarks</span></span>

<span data-ttu-id="47b94-115">Свойство **Top** всегда выражается в пикселях относительно исходного экрана (в верхнем левом углу).</span><span class="sxs-lookup"><span data-stu-id="47b94-115">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="47b94-116">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="47b94-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="47b94-117">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="47b94-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="47b94-118">Чтобы изменить расположение символа, используйте метод [**MoveTo**](moveto-method.md) .</span><span class="sxs-lookup"><span data-stu-id="47b94-118">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="47b94-119">См. также</span><span class="sxs-lookup"><span data-stu-id="47b94-119">See Also</span></span>

<span data-ttu-id="47b94-120">[**Свойство Left**](left-property.md), [ **метод moveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="47b94-120">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




