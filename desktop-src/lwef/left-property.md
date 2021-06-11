---
title: Свойство Left (объект characters)
description: Сведения о свойстве объекта "левые символы". Microsoft Agent является устаревшим в Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988940"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="4107d-104">Свойство Left (объект characters)</span><span class="sxs-lookup"><span data-stu-id="4107d-104">Left Property (Characters Object)</span></span>

<span data-ttu-id="4107d-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4107d-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4107d-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="4107d-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4107d-107">Возвращает или задает левую границу указанного кадра символа.</span><span class="sxs-lookup"><span data-stu-id="4107d-107">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="4107d-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="4107d-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4107d-109">\*Агент \***. Символы ("**_чарактерид_\*_"). Левое_ \*  \[  =  *значение*\]</span><span class="sxs-lookup"><span data-stu-id="4107d-109">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="4107d-110">Часть</span><span class="sxs-lookup"><span data-stu-id="4107d-110">Part</span></span>    | <span data-ttu-id="4107d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4107d-111">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="4107d-112">*value*</span><span class="sxs-lookup"><span data-stu-id="4107d-112">*value*</span></span> | <span data-ttu-id="4107d-113">Длинное целое число, указывающее левую границу рамки символа.</span><span class="sxs-lookup"><span data-stu-id="4107d-113">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4107d-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="4107d-114">Remarks</span></span>

<span data-ttu-id="4107d-115">Свойство **Left** всегда выражается в пикселях относительно исходного экрана (в верхнем левом углу).</span><span class="sxs-lookup"><span data-stu-id="4107d-115">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="4107d-116">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="4107d-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="4107d-117">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4107d-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




