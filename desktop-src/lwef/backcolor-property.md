---
title: Свойство BackColor (устаревшие функции среды Windows)
description: Свойство BackColor
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800892"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a><span data-ttu-id="a1203-103">Свойство BackColor (устаревшие функции среды Windows)</span><span class="sxs-lookup"><span data-stu-id="a1203-103">BackColor Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="a1203-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1203-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a1203-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="a1203-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a1203-106">Возвращает цвет фона, который в данный момент отображается в окне всплывающей подсказки для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="a1203-106">Returns the background color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a1203-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="a1203-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a1203-108">\*Агент \***. Символы ("**_чарактерид_*_"). Выноски. BackColor_*</span><span class="sxs-lookup"><span data-stu-id="a1203-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.BackColor_\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1203-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1203-109">Remarks</span></span>

<span data-ttu-id="a1203-110">Допустимый диапазон для обычного цвета RGB — от 0 до 16 777 215 (&ХФФФФФФ).</span><span class="sxs-lookup"><span data-stu-id="a1203-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="a1203-111">Старший байт числа в этом диапазоне равен 0; 3 младших байта, от минимума до наиболее значимого байта, определяют величину красного, зеленого и синего соответственно.</span><span class="sxs-lookup"><span data-stu-id="a1203-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="a1203-112">Интенсивность красного, зеленого и синего компонентов выражается числом от 0 до 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="a1203-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




