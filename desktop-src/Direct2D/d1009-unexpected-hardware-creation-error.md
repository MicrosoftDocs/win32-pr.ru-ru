---
title: D1009 непредвиденная ошибка создания оборудования
description: При попытке создать целевой объект Direct3D произошла непредвиденная ошибка \ "Ошибка \".
ms.assetid: 1ff34b1f-0ab3-4821-97f5-a4e67831383a
keywords:
- D1009 непредвиденная ошибка создания оборудования Direct2D
topic_type:
- apiref
api_name:
- D1009 Unexpected Hardware Creation Error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa51d2536995feb51081134e412d94617f34d069
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548719"
---
# <a name="d1009-unexpected-hardware-creation-error"></a><span data-ttu-id="b1c09-104">D1009: непредвиденная ошибка создания оборудования</span><span class="sxs-lookup"><span data-stu-id="b1c09-104">D1009: Unexpected Hardware Creation Error</span></span>

<span data-ttu-id="b1c09-105">\[  \] При попытке создать целевой объект Direct3D произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b1c09-105">An unexpected error \[*error*\] was encountered while trying to create a Direct3D target.</span></span>

## <a name="placeholders"></a><span data-ttu-id="b1c09-106">Заполнители</span><span class="sxs-lookup"><span data-stu-id="b1c09-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="b1c09-107"><span id="error"></span><span id="ERROR"></span>*план*</span><span class="sxs-lookup"><span data-stu-id="b1c09-107"><span id="error"></span><span id="ERROR"></span>*error*</span></span>
</dt> <dd>

<span data-ttu-id="b1c09-108">Номер ошибки.</span><span class="sxs-lookup"><span data-stu-id="b1c09-108">An error number.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="b1c09-109">Уровень ошибки</span><span class="sxs-lookup"><span data-stu-id="b1c09-109">Error Level</span></span> | <span data-ttu-id="b1c09-110">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="b1c09-110">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="b1c09-111">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="b1c09-111">Possible Causes</span></span>

-   <span data-ttu-id="b1c09-112">Целевой объект был больше максимального размера битовой карты.</span><span class="sxs-lookup"><span data-stu-id="b1c09-112">The target was larger than the maximum bitmap size.</span></span>
-   <span data-ttu-id="b1c09-113">Недостаточно видеопамяти при создании целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="b1c09-113">Out of video memory as the render target is created.</span></span>
-   <span data-ttu-id="b1c09-114">Не удалось создать устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b1c09-114">No Direct3D device could be created.</span></span>
-   <span data-ttu-id="b1c09-115">Приложение работает на платформе IA64.</span><span class="sxs-lookup"><span data-stu-id="b1c09-115">The application is running on IA64.</span></span>

 

 




