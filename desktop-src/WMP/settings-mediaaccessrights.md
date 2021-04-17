---
title: Settings. Медиаакцессригхтс
description: Свойство Медиаакцессригхтс извлекает значение, указывающее права, предоставленные в настоящее время для доступа к библиотеке.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Проигрыватель Windows Media Settings. Медиаакцессригхтс
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704382"
---
# <a name="settingsmediaaccessrights"></a><span data-ttu-id="ecac3-104">Settings. Медиаакцессригхтс</span><span class="sxs-lookup"><span data-stu-id="ecac3-104">Settings.mediaAccessRights</span></span>

<span data-ttu-id="ecac3-105">Свойство **медиаакцессригхтс** извлекает значение, указывающее права, предоставленные в настоящее время для доступа к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="ecac3-105">The **mediaAccessRights** property retrieves a value indicating the rights currently granted for library access.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecac3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecac3-106">Syntax</span></span>

<span data-ttu-id="ecac3-107">Player. Settings. Медиаакцессригхтс</span><span class="sxs-lookup"><span data-stu-id="ecac3-107">player.settings.mediaAccessRights</span></span>

## <a name="possible-values"></a><span data-ttu-id="ecac3-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ecac3-108">Possible Values</span></span>

<span data-ttu-id="ecac3-109">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ecac3-109">This property is a read-only **String**.</span></span>



| <span data-ttu-id="ecac3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ecac3-110">Value</span></span> | <span data-ttu-id="ecac3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ecac3-111">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="ecac3-112">нет</span><span class="sxs-lookup"><span data-stu-id="ecac3-112">none</span></span>  | <span data-ttu-id="ecac3-113">Только права доступа к текущему элементу.</span><span class="sxs-lookup"><span data-stu-id="ecac3-113">Current item access rights only.</span></span> |
| <span data-ttu-id="ecac3-114">read</span><span class="sxs-lookup"><span data-stu-id="ecac3-114">read</span></span>  | <span data-ttu-id="ecac3-115">Права доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ecac3-115">Read access rights only.</span></span>         |
| <span data-ttu-id="ecac3-116">переполненные</span><span class="sxs-lookup"><span data-stu-id="ecac3-116">full</span></span>  | <span data-ttu-id="ecac3-117">Права доступа для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ecac3-117">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="ecac3-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecac3-118">Remarks</span></span>

<span data-ttu-id="ecac3-119">Веб-страница должна сначала запросить у пользователя разрешение на чтение информации из библиотеки или запись данных в нее.</span><span class="sxs-lookup"><span data-stu-id="ecac3-119">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="ecac3-120">Это означает, что определенные методы, свойства и события будут недоступны из кода, если соответствующие права доступа не были предоставлены.</span><span class="sxs-lookup"><span data-stu-id="ecac3-120">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="ecac3-121">Для получения прав доступа приложение вызывает *Параметры*. **рекуестмедиаакцессригхтс**, передавая параметр, указывающий требуемый уровень прав доступа.</span><span class="sxs-lookup"><span data-stu-id="ecac3-121">To obtain access rights, the application calls *Settings*.**requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="ecac3-122">**Проигрыватель Windows Media 10 Mobile**: это свойство всегда возвращает значение **Full**.</span><span class="sxs-lookup"><span data-stu-id="ecac3-122">**Windows Media Player 10 Mobile**: This property always returns **full**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecac3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ecac3-123">Requirements</span></span>



| <span data-ttu-id="ecac3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ecac3-124">Requirement</span></span> | <span data-ttu-id="ecac3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ecac3-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecac3-126">Версия</span><span class="sxs-lookup"><span data-stu-id="ecac3-126">Version</span></span><br/> | <span data-ttu-id="ecac3-127">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ecac3-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ecac3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ecac3-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="ecac3-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecac3-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecac3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecac3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecac3-131">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="ecac3-131">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="ecac3-132">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="ecac3-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





