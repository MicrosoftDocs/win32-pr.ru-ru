---
title: Свойство "шаг"
description: Свойство "шаг"
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411403"
---
# <a name="pitch-property"></a><span data-ttu-id="8c9b9-103">Свойство "шаг"</span><span class="sxs-lookup"><span data-stu-id="8c9b9-103">Pitch Property</span></span>

<span data-ttu-id="8c9b9-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c9b9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8c9b9-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="8c9b9-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Description**</span></span> 
</dt> <dd>

<span data-ttu-id="8c9b9-106">Возвращает длинное целое число для заданного параметра продачи речевого вывода символа (TTS).</span><span class="sxs-lookup"><span data-stu-id="8c9b9-106">Returns a Long integer for the specified character's speech output (TTS) pitch setting.</span></span>

</dd> <dt>

<span data-ttu-id="8c9b9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="8c9b9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8c9b9-108">*Агент ***. Символы ("*** чарактерид \* \* *"). Тон**</span><span class="sxs-lookup"><span data-stu-id="8c9b9-108">*agent ***.Characters ("*** CharacterID\*\*\*").Pitch*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c9b9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c9b9-109">Remarks</span></span>

<span data-ttu-id="8c9b9-110">Это свойство применяется только к символам, настроенным для вывода TTS.</span><span class="sxs-lookup"><span data-stu-id="8c9b9-110">This property applies only to characters configured for TTS output.</span></span> <span data-ttu-id="8c9b9-111">Если символ не поддерживает вывод TTS, это свойство возвращает ноль (0).</span><span class="sxs-lookup"><span data-stu-id="8c9b9-111">If the character does not support TTS output, this property returns zero (0).</span></span>

<span data-ttu-id="8c9b9-112">Несмотря на то, что приложение не может записать это значение, можно включить в выходной текст Теги « **смолой** » (высота), которые будут временно увеличивать шаг для конкретного utterance.</span><span class="sxs-lookup"><span data-stu-id="8c9b9-112">Although your application cannot write this value, you can include **Pit** (pitch) tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="8c9b9-113">Однако использование тега **смолой** для изменения высоты не приведет к изменению значения свойства **шаг** .</span><span class="sxs-lookup"><span data-stu-id="8c9b9-113">However, using the **Pit** tag to change the pitch will not change the **Pitch** property setting.</span></span> <span data-ttu-id="8c9b9-114">Дополнительные сведения см. в разделе [теги вывода речи](pit-tag.md).</span><span class="sxs-lookup"><span data-stu-id="8c9b9-114">For further information, see [Speech Output Tags](pit-tag.md).</span></span>

 

 




