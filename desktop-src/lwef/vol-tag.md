---
title: Тег Vol
description: Тег Vol
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979278b2eb89c352b9e53f6141cb585fb0ed134
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067528"
---
# <a name="vol-tag"></a><span data-ttu-id="6a574-103">Тег Vol</span><span class="sxs-lookup"><span data-stu-id="6a574-103">Vol Tag</span></span>

<span data-ttu-id="6a574-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6a574-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6a574-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="6a574-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6a574-106">Задает уровень громкости, на котором наводится речь.</span><span class="sxs-lookup"><span data-stu-id="6a574-106">Sets the baseline speaking volume of the speech output.</span></span>

</dd> <dt>

<span data-ttu-id="6a574-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6a574-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6a574-108">**\\Vol =***номер***\\**</span><span class="sxs-lookup"><span data-stu-id="6a574-108">**\\Vol=***number***\\**</span></span>



| <span data-ttu-id="6a574-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="6a574-109">Part</span></span>     | <span data-ttu-id="6a574-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6a574-110">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="6a574-111">*number*</span><span class="sxs-lookup"><span data-stu-id="6a574-111">*number*</span></span> | <span data-ttu-id="6a574-112">Том с базовой назначением: 0 — это тишина, а 65535 — максимальный том.</span><span class="sxs-lookup"><span data-stu-id="6a574-112">Baseline speaking volume: 0 is silence and 65535 is maximum volume.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="6a574-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a574-113">Remarks</span></span>

<span data-ttu-id="6a574-114">Параметр Volume влияет как на левый, так и на правый канал.</span><span class="sxs-lookup"><span data-stu-id="6a574-114">The volume setting affects both left and right channels.</span></span> <span data-ttu-id="6a574-115">Вы не можете задать громкость каждого канала отдельно.</span><span class="sxs-lookup"><span data-stu-id="6a574-115">You cannot set the volume of each channel separately.</span></span> <span data-ttu-id="6a574-116">Этот тег поддерживается только для выходных данных, созданных системой TTS.</span><span class="sxs-lookup"><span data-stu-id="6a574-116">This tag is supported only for TTS-generated output.</span></span>

 

 




