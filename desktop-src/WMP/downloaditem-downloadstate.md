---
title: Довнлоадитем. Довнлоадстате
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Довнлоадстате Извлекает состояние загрузки.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- Проигрыватель Windows Media Довнлоадитем. Довнлоадстате
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699208"
---
# <a name="downloaditemdownloadstate"></a><span data-ttu-id="16172-106">Довнлоадитем. Довнлоадстате</span><span class="sxs-lookup"><span data-stu-id="16172-106">DownloadItem.downloadState</span></span>

> [!Note]  
> <span data-ttu-id="16172-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="16172-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="16172-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="16172-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="16172-109">Свойство **довнлоадстате** Извлекает состояние загрузки.</span><span class="sxs-lookup"><span data-stu-id="16172-109">The **downloadState** property retrieves the state of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="16172-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16172-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a><span data-ttu-id="16172-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="16172-111">Possible Values</span></span>

<span data-ttu-id="16172-112">Это свойство **доступно только для** чтения и содержит одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="16172-112">This property is a read-only **Number** containing one of the following values.</span></span>



| <span data-ttu-id="16172-113">Значение</span><span class="sxs-lookup"><span data-stu-id="16172-113">Value</span></span> | <span data-ttu-id="16172-114">Описание</span><span class="sxs-lookup"><span data-stu-id="16172-114">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="16172-115">0</span><span class="sxs-lookup"><span data-stu-id="16172-115">0</span></span>     | <span data-ttu-id="16172-116">Загрузка</span><span class="sxs-lookup"><span data-stu-id="16172-116">Downloading</span></span> |
| <span data-ttu-id="16172-117">1</span><span class="sxs-lookup"><span data-stu-id="16172-117">1</span></span>     | <span data-ttu-id="16172-118">Пауза</span><span class="sxs-lookup"><span data-stu-id="16172-118">Paused</span></span>      |
| <span data-ttu-id="16172-119">2</span><span class="sxs-lookup"><span data-stu-id="16172-119">2</span></span>     | <span data-ttu-id="16172-120">Обработка</span><span class="sxs-lookup"><span data-stu-id="16172-120">Processing</span></span>  |
| <span data-ttu-id="16172-121">3</span><span class="sxs-lookup"><span data-stu-id="16172-121">3</span></span>     | <span data-ttu-id="16172-122">Завершено</span><span class="sxs-lookup"><span data-stu-id="16172-122">Completed</span></span>   |
| <span data-ttu-id="16172-123">4</span><span class="sxs-lookup"><span data-stu-id="16172-123">4</span></span>     | <span data-ttu-id="16172-124">Отменено</span><span class="sxs-lookup"><span data-stu-id="16172-124">Canceled</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="16172-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16172-125">Remarks</span></span>

<span data-ttu-id="16172-126">Состояния загрузки могут происходить в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="16172-126">Download states can occur in any order.</span></span> <span data-ttu-id="16172-127">Не следует писать код, который зависит от вхождения любого определенного состояния загрузки.</span><span class="sxs-lookup"><span data-stu-id="16172-127">Do not write code that depends on the occurrence of any particular download state.</span></span>

## <a name="requirements"></a><span data-ttu-id="16172-128">Требования</span><span class="sxs-lookup"><span data-stu-id="16172-128">Requirements</span></span>



| <span data-ttu-id="16172-129">Требование</span><span class="sxs-lookup"><span data-stu-id="16172-129">Requirement</span></span> | <span data-ttu-id="16172-130">Значение</span><span class="sxs-lookup"><span data-stu-id="16172-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16172-131">Версия</span><span class="sxs-lookup"><span data-stu-id="16172-131">Version</span></span><br/> | <span data-ttu-id="16172-132">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="16172-132">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="16172-133">DLL</span><span class="sxs-lookup"><span data-stu-id="16172-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="16172-134"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16172-134"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16172-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16172-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16172-136">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="16172-136">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





