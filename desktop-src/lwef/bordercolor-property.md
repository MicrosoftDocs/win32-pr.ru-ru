---
title: Свойство BorderColor
description: Свойство BorderColor
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981d3ac280669f64219961b74d05c6ba73f1008
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486765"
---
# <a name="bordercolor-property"></a><span data-ttu-id="3db94-103">Свойство BorderColor</span><span class="sxs-lookup"><span data-stu-id="3db94-103">BorderColor Property</span></span>

<span data-ttu-id="3db94-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3db94-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3db94-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="3db94-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3db94-106">Возвращает цвет границы, отображаемый в данный момент для всплывающего окна Word для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="3db94-106">Returns the border color currently displayed for the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="3db94-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3db94-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3db94-108">\* Агент ***. Символы ("*** чарактерид \***").** Выноска. BorderColor</span><span class="sxs-lookup"><span data-stu-id="3db94-108">*agent ***.Characters ("*** CharacterID\*\*\*").*\* Balloon.BorderColor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3db94-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3db94-109">Remarks</span></span>

<span data-ttu-id="3db94-110">Допустимый диапазон для обычного цвета RGB — от 0 до 16 777 215 (&ХФФФФФФ).</span><span class="sxs-lookup"><span data-stu-id="3db94-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="3db94-111">Старший байт числа в этом диапазоне равен 0; 3 младших байта, от минимума до наиболее значимого байта, определяют величину красного, зеленого и синего соответственно.</span><span class="sxs-lookup"><span data-stu-id="3db94-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="3db94-112">Интенсивность красного, зеленого и синего компонентов выражается числом от 0 до 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="3db94-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




