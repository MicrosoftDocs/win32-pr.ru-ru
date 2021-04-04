---
title: Свойство ForeColor
description: Свойство ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887868"
---
# <a name="forecolor-property"></a><span data-ttu-id="db31b-103">Свойство ForeColor</span><span class="sxs-lookup"><span data-stu-id="db31b-103">ForeColor Property</span></span>

<span data-ttu-id="db31b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="db31b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="db31b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="db31b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="db31b-106">Возвращает цвет переднего плана, который в данный момент отображается в окне всплывающего окна для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="db31b-106">Returns the foreground color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="db31b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="db31b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="db31b-108">*Агент ***. Символы ("*** чарактерид \* \* *"). Всплывающее сообщение. ForeColor**</span><span class="sxs-lookup"><span data-stu-id="db31b-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.ForeColor*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db31b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db31b-109">Remarks</span></span>

<span data-ttu-id="db31b-110">Свойство **ForeColor** возвращает значение, определяющее цвет текста в выноске слова.</span><span class="sxs-lookup"><span data-stu-id="db31b-110">The **ForeColor** property returns a value that specifies the color of text in the word balloon.</span></span> <span data-ttu-id="db31b-111">Допустимый диапазон для обычного цвета RGB — от 0 до 16 777 215 (&ХФФФФФФ).</span><span class="sxs-lookup"><span data-stu-id="db31b-111">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="db31b-112">Старший байт числа в этом диапазоне равен 0; 3 младших байта, от минимума до наиболее значимого байта, определяют величину красного, зеленого и синего соответственно.</span><span class="sxs-lookup"><span data-stu-id="db31b-112">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="db31b-113">Интенсивность красного, зеленого и синего компонентов выражается числом от 0 до 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="db31b-113">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




