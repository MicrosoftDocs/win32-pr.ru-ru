---
title: Свойство Height (объект characters)
description: Height, свойство
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800641"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="35059-103">Свойство Height (объект characters)</span><span class="sxs-lookup"><span data-stu-id="35059-103">Height Property (Characters Object)</span></span>

<span data-ttu-id="35059-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="35059-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="35059-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="35059-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="35059-106">Возвращает или задает высоту рамки указанного символа.</span><span class="sxs-lookup"><span data-stu-id="35059-106">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="35059-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="35059-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="35059-108">\*Агент \***. Символы ("**_чарактерид_\*_")._ \*  \[ =  *Значение* высоты\]</span><span class="sxs-lookup"><span data-stu-id="35059-108">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="35059-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="35059-109">Part</span></span>    | <span data-ttu-id="35059-110">Описание</span><span class="sxs-lookup"><span data-stu-id="35059-110">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="35059-111">*value*</span><span class="sxs-lookup"><span data-stu-id="35059-111">*value*</span></span> | <span data-ttu-id="35059-112">Длинное целое число, указывающее высоту рамки символа.</span><span class="sxs-lookup"><span data-stu-id="35059-112">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35059-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35059-113">Remarks</span></span>

<span data-ttu-id="35059-114">Свойство **Height** всегда выражается в пикселях относительно экранных координат (в верхнем левом углу).</span><span class="sxs-lookup"><span data-stu-id="35059-114">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="35059-115">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="35059-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="35059-116">Несмотря на то, что символ отображается в окне области неправильной формы, высота символа основана на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="35059-116">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




