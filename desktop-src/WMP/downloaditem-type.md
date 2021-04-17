---
title: Довнлоадитем. тип
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Type Извлекает тип загружаемого файла.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- Довнлоадитем. Введите Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694759"
---
# <a name="downloaditemtype"></a><span data-ttu-id="355c2-106">Довнлоадитем. тип</span><span class="sxs-lookup"><span data-stu-id="355c2-106">DownloadItem.type</span></span>

> [!Note]  
> <span data-ttu-id="355c2-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="355c2-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="355c2-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="355c2-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="355c2-109">Свойство **Type** Извлекает тип загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="355c2-109">The **type** property retrieves the type of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="355c2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="355c2-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a><span data-ttu-id="355c2-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="355c2-111">Possible Values</span></span>

<span data-ttu-id="355c2-112">Это свойство является **строкой** только для чтения, содержащей одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="355c2-112">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="355c2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="355c2-113">Value</span></span>      | <span data-ttu-id="355c2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="355c2-114">Description</span></span>                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="355c2-115">background</span><span class="sxs-lookup"><span data-stu-id="355c2-115">background</span></span> | <span data-ttu-id="355c2-116">(Только для Windows XP.) Загрузка выполняется в фоновом режиме, как только процессорное время станет доступным.</span><span class="sxs-lookup"><span data-stu-id="355c2-116">(Windows XP only.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="355c2-117">Состояния загрузки сохраняются даже при завершении работы проигрывателя Windows Media или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="355c2-117">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="355c2-118">реальное время</span><span class="sxs-lookup"><span data-stu-id="355c2-118">real time</span></span>  | <span data-ttu-id="355c2-119">(Все поддерживаемые операционные системы.) Загрузка выполняется всего один раз.</span><span class="sxs-lookup"><span data-stu-id="355c2-119">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="355c2-120">Между сеансами не сохраняются состояния загрузки.</span><span class="sxs-lookup"><span data-stu-id="355c2-120">No download states persist between sessions.</span></span>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="355c2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="355c2-121">Remarks</span></span>

<span data-ttu-id="355c2-122">Каждый тип загрузки имеет свои преимущества и недостатки.</span><span class="sxs-lookup"><span data-stu-id="355c2-122">Each type of download has advantages and disadvantages.</span></span> <span data-ttu-id="355c2-123">Фоновая загрузка позволяет пользователю переходить к другим задачам и даже перезапускать Windows без отмены загрузки, но занимает больше времени для завершения загрузки и поддерживается только для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="355c2-123">Background downloading allows the user to proceed to other tasks and even restart Windows without cancelling the download, but takes more time overall to complete the download and is only supported for Windows XP.</span></span> <span data-ttu-id="355c2-124">Загрузка в режиме реального времени занимает меньше времени, но требует от пользователя завершить все загрузки перед закрытием проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="355c2-124">Real-time downloading takes less time to complete, but requires the user to finish all downloading before closing Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="355c2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="355c2-125">Requirements</span></span>



| <span data-ttu-id="355c2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="355c2-126">Requirement</span></span> | <span data-ttu-id="355c2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="355c2-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="355c2-128">Версия</span><span class="sxs-lookup"><span data-stu-id="355c2-128">Version</span></span><br/> | <span data-ttu-id="355c2-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="355c2-129">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="355c2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="355c2-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="355c2-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="355c2-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="355c2-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="355c2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="355c2-133">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="355c2-133">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





