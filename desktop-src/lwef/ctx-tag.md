---
title: Тег CTX
description: Тег CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068214"
---
# <a name="ctx-tag"></a><span data-ttu-id="f217e-103">Тег CTX</span><span class="sxs-lookup"><span data-stu-id="f217e-103">Ctx Tag</span></span>

<span data-ttu-id="f217e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f217e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f217e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f217e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f217e-106">Задает контекст выходного текста.</span><span class="sxs-lookup"><span data-stu-id="f217e-106">Sets the context of the output text.</span></span>

</dd> <dt>

<span data-ttu-id="f217e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f217e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f217e-108">\\**CTX** = *строка*</span><span class="sxs-lookup"><span data-stu-id="f217e-108">\\**Ctx**=*string*</span></span>\\



| <span data-ttu-id="f217e-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="f217e-109">Part</span></span>     | <span data-ttu-id="f217e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f217e-110">Description</span></span>                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f217e-111">*string*</span><span class="sxs-lookup"><span data-stu-id="f217e-111">*string*</span></span> | <span data-ttu-id="f217e-112">Строка, указывающая контекст следующего текста, который определяет, как говорят символы или сокращения.</span><span class="sxs-lookup"><span data-stu-id="f217e-112">A string specifying the context of the text that follows, which determines how symbols or abbreviations are spoken.</span></span><br/> <span data-ttu-id="f217e-113">**"Address"**    Адреса и (или) номера телефонов.</span><span class="sxs-lookup"><span data-stu-id="f217e-113">**"Address"**    Addresses and/or phone numbers.</span></span><br/> <span data-ttu-id="f217e-114">**"Электронная почта"**    Электронная почта.</span><span class="sxs-lookup"><span data-stu-id="f217e-114">**"E-mail"**    Electronic mail.</span></span><br/> <span data-ttu-id="f217e-115">Контекст **"Unknown"** (по умолчанию) неизвестен.</span><span class="sxs-lookup"><span data-stu-id="f217e-115">**"Unknown"**    (Default) Context is unknown.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="f217e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f217e-116">Remarks</span></span>

<span data-ttu-id="f217e-117">Этот тег поддерживается только для выходных данных, созданных системой TTS.</span><span class="sxs-lookup"><span data-stu-id="f217e-117">This tag is supported only for TTS-generated output.</span></span> <span data-ttu-id="f217e-118">Диапазон значений параметра может различаться в зависимости от установленного модуля TTS.</span><span class="sxs-lookup"><span data-stu-id="f217e-118">The range of values for the parameter may vary depending on the installed TTS engine.</span></span>

 

 





