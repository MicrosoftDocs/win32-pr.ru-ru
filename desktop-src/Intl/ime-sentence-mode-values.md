---
description: Проверьте список значений режима предложений редактора методов ввода IME. Эти значения используются с функциями Иммжетконверсионстатус и Иммсетконверсионстатус.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Значения режима предложений IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406767"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="290aa-104">Значения режима предложений IME</span><span class="sxs-lookup"><span data-stu-id="290aa-104">IME Sentence Mode Values</span></span>

<span data-ttu-id="290aa-105">Эти значения используются с функциями [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) и [**иммсетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="290aa-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="290aa-106">Константа</span><span class="sxs-lookup"><span data-stu-id="290aa-106">Constant</span></span>                  | <span data-ttu-id="290aa-107">Определение</span><span class="sxs-lookup"><span data-stu-id="290aa-107">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="290aa-108">редактор IME \_ смоде \_ автоматически</span><span class="sxs-lookup"><span data-stu-id="290aa-108">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="290aa-109">Редактор IME выполняет обработку преобразования в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="290aa-109">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="290aa-110">IME \_ смоде \_ None</span><span class="sxs-lookup"><span data-stu-id="290aa-110">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="290aa-111">Нет сведений о предложении.</span><span class="sxs-lookup"><span data-stu-id="290aa-111">No information for sentence.</span></span>                                               |
| <span data-ttu-id="290aa-112">редактор IME \_ смоде \_ фрасепредикт</span><span class="sxs-lookup"><span data-stu-id="290aa-112">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="290aa-113">Редактор IME использует сведения о фразах для прогнозирования следующего символа.</span><span class="sxs-lookup"><span data-stu-id="290aa-113">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="290aa-114">редактор IME \_ смоде \_ плуралклаусе</span><span class="sxs-lookup"><span data-stu-id="290aa-114">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="290aa-115">Редактор IME использует сведения о предложении plural для выполнения обработки преобразования.</span><span class="sxs-lookup"><span data-stu-id="290aa-115">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="290aa-116">редактор IME \_ смоде \_ синглеконверт</span><span class="sxs-lookup"><span data-stu-id="290aa-116">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="290aa-117">Редактор IME выполняет обработку преобразования в односимвольном режиме.</span><span class="sxs-lookup"><span data-stu-id="290aa-117">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="290aa-118">\_диалог СМОДЕ \_ IME</span><span class="sxs-lookup"><span data-stu-id="290aa-118">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="290aa-119">Редактор IME использует режим диалога.</span><span class="sxs-lookup"><span data-stu-id="290aa-119">The IME uses conversation mode.</span></span> <span data-ttu-id="290aa-120">Это полезно для приложений разговора.</span><span class="sxs-lookup"><span data-stu-id="290aa-120">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="290aa-121">Биты с 16 по 31 зарезервированы для использования IME.</span><span class="sxs-lookup"><span data-stu-id="290aa-121">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



