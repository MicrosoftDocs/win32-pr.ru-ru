---
title: Тег МРК
description: Тег МРК
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776046"
---
# <a name="mrk-tag"></a><span data-ttu-id="75432-103">Тег МРК</span><span class="sxs-lookup"><span data-stu-id="75432-103">Mrk Tag</span></span>

<span data-ttu-id="75432-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75432-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="75432-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="75432-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="75432-106">Определяет закладку в речевом тексте.</span><span class="sxs-lookup"><span data-stu-id="75432-106">Defines a bookmark in the spoken text.</span></span>

</dd> <dt>

<span data-ttu-id="75432-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="75432-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="75432-108">**\\МРК =***число***\\**</span><span class="sxs-lookup"><span data-stu-id="75432-108">**\\Mrk=***number***\\**</span></span>



| <span data-ttu-id="75432-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="75432-109">Part</span></span>     | <span data-ttu-id="75432-110">Описание</span><span class="sxs-lookup"><span data-stu-id="75432-110">Description</span></span>                                        |
|----------|----------------------------------------------------|
| <span data-ttu-id="75432-111">*number*</span><span class="sxs-lookup"><span data-stu-id="75432-111">*number*</span></span> | <span data-ttu-id="75432-112">Длинное целочисленное значение, идентифицирующее закладку.</span><span class="sxs-lookup"><span data-stu-id="75432-112">A Long integer value that identifies the bookmark.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="75432-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75432-113">Remarks</span></span>

<span data-ttu-id="75432-114">Когда сервер обрабатывает закладку, он создает событие закладки.</span><span class="sxs-lookup"><span data-stu-id="75432-114">When the server processes a bookmark, it generates a bookmark event.</span></span> <span data-ttu-id="75432-115">Необходимо указать число больше нуля (0) и не равно 2147483647 или 2147483646.</span><span class="sxs-lookup"><span data-stu-id="75432-115">You must specify a number greater than zero (0) and not equal to 2147483647 or 2147483646.</span></span>

 

 




