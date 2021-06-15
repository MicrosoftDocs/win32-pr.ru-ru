---
title: Свойство Height (объект characters)
description: Сведения о свойстве Height объекта Characters. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068519"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="10de9-104">Свойство Height (объект characters)</span><span class="sxs-lookup"><span data-stu-id="10de9-104">Height Property (Characters Object)</span></span>

<span data-ttu-id="10de9-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="10de9-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="10de9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="10de9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="10de9-107">Возвращает или задает высоту рамки указанного символа.</span><span class="sxs-lookup"><span data-stu-id="10de9-107">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="10de9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="10de9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="10de9-109">\*Агент \***. Символы ("**_чарактерид_\*_")._ \*  \[ =  *Значение* высоты\]</span><span class="sxs-lookup"><span data-stu-id="10de9-109">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="10de9-110">Часть</span><span class="sxs-lookup"><span data-stu-id="10de9-110">Part</span></span>    | <span data-ttu-id="10de9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="10de9-111">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="10de9-112">*value*</span><span class="sxs-lookup"><span data-stu-id="10de9-112">*value*</span></span> | <span data-ttu-id="10de9-113">Длинное целое число, указывающее высоту рамки символа.</span><span class="sxs-lookup"><span data-stu-id="10de9-113">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10de9-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="10de9-114">Remarks</span></span>

<span data-ttu-id="10de9-115">Свойство **Height** всегда выражается в пикселях относительно экранных координат (в верхнем левом углу).</span><span class="sxs-lookup"><span data-stu-id="10de9-115">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="10de9-116">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="10de9-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="10de9-117">Несмотря на то, что символ отображается в окне области неправильной формы, высота символа основана на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="10de9-117">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




