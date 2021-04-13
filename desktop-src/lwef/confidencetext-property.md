---
title: Конфиденцетекст, свойство
description: Конфиденцетекст, свойство
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412886"
---
# <a name="confidencetext-property"></a><span data-ttu-id="9bc83-103">Конфиденцетекст, свойство</span><span class="sxs-lookup"><span data-stu-id="9bc83-103">ConfidenceText Property</span></span>

<span data-ttu-id="9bc83-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9bc83-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9bc83-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9bc83-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9bc83-106">Возвращает или задает **конфиденцетекст** клиента, который отображается в Tip прослушивания.</span><span class="sxs-lookup"><span data-stu-id="9bc83-106">Returns or sets the client's **ConfidenceText** that appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="9bc83-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9bc83-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9bc83-108">\* Агент ***. Символы ("*** чарактерид ***"). Команды ("*** имя \***")**.  \[ Конфиденцетекст  =  *строка*\]</span><span class="sxs-lookup"><span data-stu-id="9bc83-108">\*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.**ConfidenceText**\[ = *string*\]</span></span>



| <span data-ttu-id="9bc83-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="9bc83-109">Part</span></span>     | <span data-ttu-id="9bc83-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9bc83-110">Description</span></span>                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc83-111">*string*</span><span class="sxs-lookup"><span data-stu-id="9bc83-111">*string*</span></span> | <span data-ttu-id="9bc83-112">Строковое выражение, результатом которого является текст для **Конфиденцетекст** [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="9bc83-112">A string expression that evaluates to the text for the **ConfidenceText** for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bc83-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bc83-113">Remarks</span></span>

<span data-ttu-id="9bc83-114">Если возвращенное значение достоверности наилучшего соответствия (UserInput. достоверность) не превышает параметр [**достоверности**](confidence-property.md) , сервер отображает текст, указанный в **конфиденцетекст** , в подсказке прослушивания.</span><span class="sxs-lookup"><span data-stu-id="9bc83-114">When the returned confidence value of the best match (UserInput.Confidence) does not exceed the [**Confidence**](confidence-property.md) setting, the server displays the text supplied in **ConfidenceText** in the Listening Tip.</span></span>

 

 