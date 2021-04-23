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
ms.openlocfilehash: 8844c084802313c246aeb17924fc811d3915816a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889456"
---
# <a name="d1009-unexpected-hardware-creation-error"></a><span data-ttu-id="0a126-104">D1009: непредвиденная ошибка создания оборудования</span><span class="sxs-lookup"><span data-stu-id="0a126-104">D1009: Unexpected Hardware Creation Error</span></span>

<span data-ttu-id="0a126-105">\[  \] При попытке создать целевой объект Direct3D произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="0a126-105">An unexpected error \[*error*\] was encountered while trying to create a Direct3D target.</span></span>

## <a name="placeholders"></a><span data-ttu-id="0a126-106">Заполнители</span><span class="sxs-lookup"><span data-stu-id="0a126-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="0a126-107"><span id="error"></span><span id="ERROR"></span>*план*</span><span class="sxs-lookup"><span data-stu-id="0a126-107"><span id="error"></span><span id="ERROR"></span>*error*</span></span>
</dt> <dd>

<span data-ttu-id="0a126-108">Номер ошибки.</span><span class="sxs-lookup"><span data-stu-id="0a126-108">An error number.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="0a126-109">Уровень ошибки</span><span class="sxs-lookup"><span data-stu-id="0a126-109">Error Level</span></span> | <span data-ttu-id="0a126-110">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="0a126-110">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="0a126-111">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="0a126-111">Possible Causes</span></span>

-   <span data-ttu-id="0a126-112">Целевой объект был больше максимального размера битовой карты.</span><span class="sxs-lookup"><span data-stu-id="0a126-112">The target was larger than the maximum bitmap size.</span></span>
-   <span data-ttu-id="0a126-113">Недостаточно видеопамяти при создании целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="0a126-113">Out of video memory as the render target is created.</span></span>
-   <span data-ttu-id="0a126-114">Не удалось создать устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0a126-114">No Direct3D device could be created.</span></span>
-   <span data-ttu-id="0a126-115">Приложение работает на платформе IA64.</span><span class="sxs-lookup"><span data-stu-id="0a126-115">The application is running on IA64.</span></span>

 

 




