---
title: Свойство достоверности
description: Свойство достоверности
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412823"
---
# <a name="confidence-property"></a><span data-ttu-id="9285c-103">Свойство достоверности</span><span class="sxs-lookup"><span data-stu-id="9285c-103">Confidence Property</span></span>

<span data-ttu-id="9285c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9285c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9285c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9285c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9285c-106">Возвращает или задает значение, указывающее, отображается ли **достоверность** клиента в Tip прослушивания.</span><span class="sxs-lookup"><span data-stu-id="9285c-106">Returns or sets whether the client's **Confidence** appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="9285c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9285c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9285c-108">\*Агент ***. Символы ("*** чарактерид ***"). Команды ("*** имя \***")**. \* \* достоверное\* \*  \[  =  *число*\]</span><span class="sxs-lookup"><span data-stu-id="9285c-108">*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.\*\*Confidence*\* \[ = *Number*\]</span></span>



| <span data-ttu-id="9285c-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="9285c-109">Part</span></span>     | <span data-ttu-id="9285c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9285c-110">Description</span></span>                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9285c-111">*Число*</span><span class="sxs-lookup"><span data-stu-id="9285c-111">*Number*</span></span> | <span data-ttu-id="9285c-112">Числовое выражение, результатом которого является длинное целое число, идентифицирующее значение достоверности для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="9285c-112">A numeric expression that evaluates to a Long integer that identifies confidence value for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9285c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9285c-113">Remarks</span></span>

<span data-ttu-id="9285c-114">Если возвращенное значение достоверности наилучшего соответствия (UserInput. достоверность) не превышает значение, заданное для свойства **достоверности** , то текст, указанный в [**конфиденцетекст**](confidencetext-property.md) , отображается в подсказке прослушивания.</span><span class="sxs-lookup"><span data-stu-id="9285c-114">If the returned confidence value of the best match (UserInput.Confidence) does not exceed value you set for the **Confidence** property, the text supplied in [**ConfidenceText**](confidencetext-property.md) is displayed in the Listening Tip.</span></span>

 

 