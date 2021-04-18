---
title: Свойство Speed
description: Свойство Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700529"
---
# <a name="speed-property"></a><span data-ttu-id="d0b76-103">Свойство Speed</span><span class="sxs-lookup"><span data-stu-id="d0b76-103">Speed Property</span></span>

<span data-ttu-id="d0b76-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0b76-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d0b76-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="d0b76-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d0b76-106">Возвращает длинное целое число, определяющее текущую скорость речевого вывода символа.</span><span class="sxs-lookup"><span data-stu-id="d0b76-106">Returns a Long integer that specifies the current speed of the character's speech output.</span></span>

</dd> <dt>

<span data-ttu-id="d0b76-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="d0b76-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d0b76-108">*Агент ***. Символы ("*** чарактерид \* \* *"). Установлен**</span><span class="sxs-lookup"><span data-stu-id="d0b76-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speed*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0b76-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0b76-109">Remarks</span></span>

<span data-ttu-id="d0b76-110">Это свойство возвращает значение текущего параметра скорости вывода речи для символа.</span><span class="sxs-lookup"><span data-stu-id="d0b76-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="d0b76-111">Для символов, использующих выходные данные TTS, свойство возвращает фактический параметр вывода TTS для символа.</span><span class="sxs-lookup"><span data-stu-id="d0b76-111">For characters using TTS output, the property returns the actual TTS output setting for the character.</span></span> <span data-ttu-id="d0b76-112">Если режим TTS не включен или символ не поддерживает вывод TTS, параметр отражает скорость вывода.</span><span class="sxs-lookup"><span data-stu-id="d0b76-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

<span data-ttu-id="d0b76-113">Несмотря на то, что приложение не может записать это значение, можно включить в выходной текст Теги **SPD** (Speed), которые будут временно ускорить вывод для определенного utterance.</span><span class="sxs-lookup"><span data-stu-id="d0b76-113">Although your application cannot write this value, you can include **Spd** (speed) tags in your output text that will temporarily speed up the output for a particular utterance.</span></span> <span data-ttu-id="d0b76-114">Однако использование тега **SPD** для изменения речевого вывода символа не влияет на значение свойства **Speed** .</span><span class="sxs-lookup"><span data-stu-id="d0b76-114">However, using the **Spd** tag to change the character's spoken output does not affect the **Speed** property setting.</span></span> <span data-ttu-id="d0b76-115">Дополнительные сведения см. в разделе [теги вывода речи](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="d0b76-115">For further information, see [Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




