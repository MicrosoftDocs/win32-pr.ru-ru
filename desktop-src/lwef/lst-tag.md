---
title: Тег LST
description: Тег LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532132"
---
# <a name="lst-tag"></a><span data-ttu-id="10027-103">Тег LST</span><span class="sxs-lookup"><span data-stu-id="10027-103">Lst Tag</span></span>

<span data-ttu-id="10027-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="10027-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="10027-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="10027-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="10027-106">Повторяет последнюю произнесенную инструкцию для символа.</span><span class="sxs-lookup"><span data-stu-id="10027-106">Repeats last spoken statement for the character.</span></span>

</dd> <dt>

<span data-ttu-id="10027-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="10027-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="10027-108">\\**LST**</span><span class="sxs-lookup"><span data-stu-id="10027-108">\\**Lst**</span></span>\\

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="10027-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10027-109">Remarks</span></span>

<span data-ttu-id="10027-110">Этот тег позволяет символу повторять последнюю произнесенную инструкцию.</span><span class="sxs-lookup"><span data-stu-id="10027-110">This tag enables a character to repeat its last spoken statement.</span></span> <span data-ttu-id="10027-111">Этот тег должен располагаться в методе [**говорите**](speak-method.md) . никакой другой текст или параметры не могут быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="10027-111">This tag must appear by itself in the [**Speak**](speak-method.md) method; no other text or parameters can be included.</span></span> <span data-ttu-id="10027-112">При повторении речевого текста все остальные теги, включенные в исходный текст, повторяются, за исключением закладок.</span><span class="sxs-lookup"><span data-stu-id="10027-112">When the spoken text is repeated, any other tags included in the original text are repeated, except for bookmarks.</span></span> <span data-ttu-id="10027-113">Всеми. WAV и. Файлы ЛВВ, содержащиеся в тексте, также повторяются.</span><span class="sxs-lookup"><span data-stu-id="10027-113">Any .WAV and .LWV files included in the text are also repeated.</span></span>

 

 




