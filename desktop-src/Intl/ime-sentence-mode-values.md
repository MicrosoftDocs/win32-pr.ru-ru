---
description: Эти значения используются с функциями Иммжетконверсионстатус и Иммсетконверсионстатус.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Значения режима предложений IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264716"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="e7b57-103">Значения режима предложений IME</span><span class="sxs-lookup"><span data-stu-id="e7b57-103">IME Sentence Mode Values</span></span>

<span data-ttu-id="e7b57-104">Эти значения используются с функциями [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) и [**иммсетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="e7b57-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="e7b57-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e7b57-105">Constant</span></span>                  | <span data-ttu-id="e7b57-106">Определение</span><span class="sxs-lookup"><span data-stu-id="e7b57-106">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="e7b57-107">редактор IME \_ смоде \_ автоматически</span><span class="sxs-lookup"><span data-stu-id="e7b57-107">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="e7b57-108">Редактор IME выполняет обработку преобразования в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="e7b57-108">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="e7b57-109">IME \_ смоде \_ None</span><span class="sxs-lookup"><span data-stu-id="e7b57-109">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="e7b57-110">Нет сведений о предложении.</span><span class="sxs-lookup"><span data-stu-id="e7b57-110">No information for sentence.</span></span>                                               |
| <span data-ttu-id="e7b57-111">редактор IME \_ смоде \_ фрасепредикт</span><span class="sxs-lookup"><span data-stu-id="e7b57-111">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="e7b57-112">Редактор IME использует сведения о фразах для прогнозирования следующего символа.</span><span class="sxs-lookup"><span data-stu-id="e7b57-112">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="e7b57-113">редактор IME \_ смоде \_ плуралклаусе</span><span class="sxs-lookup"><span data-stu-id="e7b57-113">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="e7b57-114">Редактор IME использует сведения о предложении plural для выполнения обработки преобразования.</span><span class="sxs-lookup"><span data-stu-id="e7b57-114">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="e7b57-115">редактор IME \_ смоде \_ синглеконверт</span><span class="sxs-lookup"><span data-stu-id="e7b57-115">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="e7b57-116">Редактор IME выполняет обработку преобразования в односимвольном режиме.</span><span class="sxs-lookup"><span data-stu-id="e7b57-116">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="e7b57-117">\_диалог СМОДЕ \_ IME</span><span class="sxs-lookup"><span data-stu-id="e7b57-117">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="e7b57-118">Редактор IME использует режим диалога.</span><span class="sxs-lookup"><span data-stu-id="e7b57-118">The IME uses conversation mode.</span></span> <span data-ttu-id="e7b57-119">Это полезно для приложений разговора.</span><span class="sxs-lookup"><span data-stu-id="e7b57-119">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="e7b57-120">Биты с 16 по 31 зарезервированы для использования IME.</span><span class="sxs-lookup"><span data-stu-id="e7b57-120">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



