---
title: Свойство Top (объект characters)
description: Свойство Top
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710421"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="ba507-103">Свойство Top (объект characters)</span><span class="sxs-lookup"><span data-stu-id="ba507-103">Top Property (Characters Object)</span></span>

<span data-ttu-id="ba507-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ba507-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ba507-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="ba507-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ba507-106">Возвращает или задает верхний край указанного кадра символа.</span><span class="sxs-lookup"><span data-stu-id="ba507-106">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="ba507-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ba507-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ba507-108">\*Агент \***. Символы ("**_чарактерид_\*_"). Верхнее_ \*  \[  =  *значение*\]</span><span class="sxs-lookup"><span data-stu-id="ba507-108">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="ba507-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="ba507-109">Part</span></span>    | <span data-ttu-id="ba507-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ba507-110">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="ba507-111">*value*</span><span class="sxs-lookup"><span data-stu-id="ba507-111">*value*</span></span> | <span data-ttu-id="ba507-112">Длинное целое число, указывающее верхнюю границу символа.</span><span class="sxs-lookup"><span data-stu-id="ba507-112">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba507-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba507-113">Remarks</span></span>

<span data-ttu-id="ba507-114">Свойство **Top** всегда выражается в пикселях относительно исходного экрана (в верхнем левом углу).</span><span class="sxs-lookup"><span data-stu-id="ba507-114">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="ba507-115">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="ba507-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="ba507-116">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ba507-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="ba507-117">Чтобы изменить расположение символа, используйте метод [**MoveTo**](moveto-method.md) .</span><span class="sxs-lookup"><span data-stu-id="ba507-117">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba507-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="ba507-118">See Also</span></span>

<span data-ttu-id="ba507-119">[**Свойство Left**](left-property.md), [ **метод moveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="ba507-119">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




