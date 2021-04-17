---
title: Довнлоадитем. Саурцеурл
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Саурцеурл извлекает URL-адрес источника для скачивания.
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- Проигрыватель Windows Media Довнлоадитем. Саурцеурл
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694931"
---
# <a name="downloaditemsourceurl"></a><span data-ttu-id="0f696-106">Довнлоадитем. Саурцеурл</span><span class="sxs-lookup"><span data-stu-id="0f696-106">DownloadItem.sourceURL</span></span>

> [!Note]  
> <span data-ttu-id="0f696-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="0f696-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0f696-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0f696-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0f696-109">Свойство **саурцеурл** извлекает URL-адрес источника для скачивания.</span><span class="sxs-lookup"><span data-stu-id="0f696-109">The **sourceURL** property retrieves the source URL of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f696-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f696-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a><span data-ttu-id="0f696-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0f696-111">Possible Values</span></span>

<span data-ttu-id="0f696-112">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0f696-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f696-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f696-113">Remarks</span></span>

<span data-ttu-id="0f696-114">Можно скачать только следующие форматы мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="0f696-114">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="0f696-115">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="0f696-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="0f696-116">MP3</span><span class="sxs-lookup"><span data-stu-id="0f696-116">MP3</span></span>
-   <span data-ttu-id="0f696-117">Звуковые файлы в формате WMA</span><span class="sxs-lookup"><span data-stu-id="0f696-117">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="0f696-118">Видеофайлы в формате WMV</span><span class="sxs-lookup"><span data-stu-id="0f696-118">Windows Media Video (WMV)</span></span>

## <a name="requirements"></a><span data-ttu-id="0f696-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0f696-119">Requirements</span></span>



| <span data-ttu-id="0f696-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0f696-120">Requirement</span></span> | <span data-ttu-id="0f696-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0f696-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f696-122">Версия</span><span class="sxs-lookup"><span data-stu-id="0f696-122">Version</span></span><br/> | <span data-ttu-id="0f696-123">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0f696-123">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0f696-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0f696-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f696-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f696-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f696-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f696-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f696-127">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="0f696-127">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





