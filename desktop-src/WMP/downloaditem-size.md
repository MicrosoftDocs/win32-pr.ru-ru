---
title: Довнлоадитем. size
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Size Извлекает размер загружаемого файла.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- Проигрыватель Windows Media Довнлоадитем. size
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ebb1ce15d34ad04095f1ef1ed84ad2df008c7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695083"
---
# <a name="downloaditemsize"></a><span data-ttu-id="1d707-106">Довнлоадитем. size</span><span class="sxs-lookup"><span data-stu-id="1d707-106">DownloadItem.size</span></span>

> [!Note]  
> <span data-ttu-id="1d707-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="1d707-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1d707-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d707-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1d707-109">Свойство **size** Извлекает размер загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="1d707-109">The **size** property retrieves the size of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d707-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d707-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a><span data-ttu-id="1d707-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1d707-111">Possible Values</span></span>

<span data-ttu-id="1d707-112">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="1d707-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d707-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1d707-113">Requirements</span></span>



| <span data-ttu-id="1d707-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1d707-114">Requirement</span></span> | <span data-ttu-id="1d707-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1d707-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d707-116">Версия</span><span class="sxs-lookup"><span data-stu-id="1d707-116">Version</span></span><br/> | <span data-ttu-id="1d707-117">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1d707-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="1d707-118">DLL</span><span class="sxs-lookup"><span data-stu-id="1d707-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="1d707-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d707-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d707-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d707-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d707-121">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="1d707-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="1d707-122">**Довнлоадитем. ход выполнения**</span><span class="sxs-lookup"><span data-stu-id="1d707-122">**DownloadItem.progress**</span></span>](downloaditem-progress.md)
</dt> </dl>

 

 





