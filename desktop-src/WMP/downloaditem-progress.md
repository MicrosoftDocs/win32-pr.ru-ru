---
title: Довнлоадитем. ход выполнения
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Progress получает сведения о ходе загрузки в байтах.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- Проигрыватель Windows Media Довнлоадитем. Progress
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694823"
---
# <a name="downloaditemprogress"></a><span data-ttu-id="72f5e-106">Довнлоадитем. ход выполнения</span><span class="sxs-lookup"><span data-stu-id="72f5e-106">DownloadItem.progress</span></span>

> [!Note]  
> <span data-ttu-id="72f5e-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="72f5e-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="72f5e-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="72f5e-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="72f5e-109">Свойство **Progress** получает сведения о ходе загрузки в байтах.</span><span class="sxs-lookup"><span data-stu-id="72f5e-109">The **progress** property retrieves the progress of the download in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f5e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72f5e-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a><span data-ttu-id="72f5e-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="72f5e-111">Possible Values</span></span>

<span data-ttu-id="72f5e-112">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="72f5e-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="72f5e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="72f5e-113">Requirements</span></span>



| <span data-ttu-id="72f5e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="72f5e-114">Requirement</span></span> | <span data-ttu-id="72f5e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="72f5e-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="72f5e-116">Версия</span><span class="sxs-lookup"><span data-stu-id="72f5e-116">Version</span></span><br/> | <span data-ttu-id="72f5e-117">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="72f5e-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="72f5e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="72f5e-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="72f5e-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f5e-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f5e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72f5e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f5e-121">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="72f5e-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="72f5e-122">**Довнлоадитем. size**</span><span class="sxs-lookup"><span data-stu-id="72f5e-122">**DownloadItem.size**</span></span>](downloaditem-size.md)
</dt> </dl>

 

 





