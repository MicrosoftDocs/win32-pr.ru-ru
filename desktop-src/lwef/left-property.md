---
title: Свойство Left (объект characters)
description: Свойство Left
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105661817"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="eb295-103">Свойство Left (объект characters)</span><span class="sxs-lookup"><span data-stu-id="eb295-103">Left Property (Characters Object)</span></span>

<span data-ttu-id="eb295-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb295-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eb295-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="eb295-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eb295-106">Возвращает или задает левую границу указанного кадра символа.</span><span class="sxs-lookup"><span data-stu-id="eb295-106">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="eb295-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="eb295-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="eb295-108">\*Агент \***. Символы ("**_чарактерид_\*_"). Левое_ \*  \[  =  *значение*\]</span><span class="sxs-lookup"><span data-stu-id="eb295-108">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="eb295-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="eb295-109">Part</span></span>    | <span data-ttu-id="eb295-110">Описание</span><span class="sxs-lookup"><span data-stu-id="eb295-110">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="eb295-111">*value*</span><span class="sxs-lookup"><span data-stu-id="eb295-111">*value*</span></span> | <span data-ttu-id="eb295-112">Длинное целое число, указывающее левую границу рамки символа.</span><span class="sxs-lookup"><span data-stu-id="eb295-112">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb295-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb295-113">Remarks</span></span>

<span data-ttu-id="eb295-114">Свойство **Left** всегда выражается в пикселях относительно исходного экрана (в верхнем левом углу).</span><span class="sxs-lookup"><span data-stu-id="eb295-114">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="eb295-115">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="eb295-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="eb295-116">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="eb295-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




