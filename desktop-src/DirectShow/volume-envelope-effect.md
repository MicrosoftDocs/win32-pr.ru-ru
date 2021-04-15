---
description: Эффекты конверта тома
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Эффекты конверта тома
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683768"
---
# <a name="volume-envelope-effect"></a><span data-ttu-id="04898-103">Эффекты конверта тома</span><span class="sxs-lookup"><span data-stu-id="04898-103">Volume Envelope Effect</span></span>

> [!Note]  
> <span data-ttu-id="04898-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="04898-104">\[Deprecated.</span></span> <span data-ttu-id="04898-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04898-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04898-106">Действие конверта тома задает громкость аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="04898-106">The Volume Envelope effect sets the volume on an audio stream.</span></span>

<span data-ttu-id="04898-107">Идентификатор класса (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="04898-107">Class ID (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span></span>

<span data-ttu-id="04898-108">Имя переменной CLSID: CLSID \_ аудмиксер</span><span class="sxs-lookup"><span data-stu-id="04898-108">CLSID Variable Name: CLSID\_AudMixer</span></span>

<span data-ttu-id="04898-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="04898-109">Properties</span></span>



| <span data-ttu-id="04898-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="04898-110">Property</span></span> | <span data-ttu-id="04898-111">Тип</span><span class="sxs-lookup"><span data-stu-id="04898-111">Type</span></span>   | <span data-ttu-id="04898-112">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="04898-112">Default</span></span> | <span data-ttu-id="04898-113">Описание</span><span class="sxs-lookup"><span data-stu-id="04898-113">Description</span></span>                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04898-114">Т</span><span class="sxs-lookup"><span data-stu-id="04898-114">Vol</span></span>      | <span data-ttu-id="04898-115">double</span><span class="sxs-lookup"><span data-stu-id="04898-115">double</span></span> | <span data-ttu-id="04898-116">1.0</span><span class="sxs-lookup"><span data-stu-id="04898-116">1.0</span></span>     | <span data-ttu-id="04898-117">Том в процентах от созданного тома.</span><span class="sxs-lookup"><span data-stu-id="04898-117">Volume, as a percentage of the authored volume.</span></span> <span data-ttu-id="04898-118">Вы можете создавать звуковые затухания, изменяя значение этого свойства с течением времени.</span><span class="sxs-lookup"><span data-stu-id="04898-118">You can produce audio fades by varying this property value over time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="04898-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04898-119">Remarks</span></span>

<span data-ttu-id="04898-120">Каждый объект на временной шкале может иметь не более одного воздействия на конверт.</span><span class="sxs-lookup"><span data-stu-id="04898-120">Each object in a timeline can have at most one volume envelope effect.</span></span> <span data-ttu-id="04898-121">В композиции или группе перед любыми звуковыми эффектами применяется конверт тома, который не зависит от его приоритета.</span><span class="sxs-lookup"><span data-stu-id="04898-121">In a composition or a group, the volume envelope is applied first, before any other audio effects, regardless of its priority.</span></span> <span data-ttu-id="04898-122">В источнике или дорожке воздействие на том применяется в соответствии с приоритетом.</span><span class="sxs-lookup"><span data-stu-id="04898-122">In a source or a track, the volume effect is applied according to its priority.</span></span>

 

 



