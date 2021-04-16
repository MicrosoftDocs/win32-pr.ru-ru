---
title: DownloadCollection.id
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство ID извлекает идентификатор коллекции загрузки.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699212"
---
# <a name="downloadcollectionid"></a><span data-ttu-id="1a18e-106">DownloadCollection.id</span><span class="sxs-lookup"><span data-stu-id="1a18e-106">DownloadCollection.id</span></span>

> [!Note]  
> <span data-ttu-id="1a18e-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="1a18e-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1a18e-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1a18e-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1a18e-109">Свойство **ID** извлекает идентификатор коллекции загрузки.</span><span class="sxs-lookup"><span data-stu-id="1a18e-109">The **id** property retrieves the ID of the download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a18e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a18e-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a><span data-ttu-id="1a18e-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1a18e-111">Possible Values</span></span>

<span data-ttu-id="1a18e-112">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="1a18e-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a18e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a18e-113">Remarks</span></span>

<span data-ttu-id="1a18e-114">Когда диспетчер загрузки создает новую коллекцию загрузки, он присваивает коллекции ИДЕНТИФИКАЦИОНный номер.</span><span class="sxs-lookup"><span data-stu-id="1a18e-114">When the Download Manager creates a new download collection, it assigns the collection an ID number.</span></span> <span data-ttu-id="1a18e-115">Номера ИДЕНТИФИКАТОРов сохраняются между сеансами проигрывателя Windows Media и сеансами операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1a18e-115">ID numbers persist between Windows Media Player sessions and operating system sessions.</span></span>

<span data-ttu-id="1a18e-116">ИДЕНТИФИКАЦИОНные номера не являются уникальными.</span><span class="sxs-lookup"><span data-stu-id="1a18e-116">ID numbers are not unique.</span></span> <span data-ttu-id="1a18e-117">Однако в 32-разрядном значении достаточно номеров ИДЕНТИФИКАТОРов, что чрезвычайно маловероятно, что существующий идентификатор будет перезаписан новым.</span><span class="sxs-lookup"><span data-stu-id="1a18e-117">However, there are enough ID numbers available in the 32-bit value that it is extremely unlikely that an existing ID number will ever be overwritten by a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a18e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1a18e-118">Requirements</span></span>



| <span data-ttu-id="1a18e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1a18e-119">Requirement</span></span> | <span data-ttu-id="1a18e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1a18e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a18e-121">Версия</span><span class="sxs-lookup"><span data-stu-id="1a18e-121">Version</span></span><br/> | <span data-ttu-id="1a18e-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1a18e-122">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="1a18e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1a18e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a18e-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a18e-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a18e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a18e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a18e-126">**Объект Довнлоадколлектион**</span><span class="sxs-lookup"><span data-stu-id="1a18e-126">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





