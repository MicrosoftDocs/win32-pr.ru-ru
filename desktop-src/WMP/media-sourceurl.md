---
title: Media. Саурцеурл
description: Свойство Саурцеурл извлекает URL-адрес элемента мультимедиа.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media. Саурцеурл проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698815"
---
# <a name="mediasourceurl"></a><span data-ttu-id="8fa67-104">Media. Саурцеурл</span><span class="sxs-lookup"><span data-stu-id="8fa67-104">Media.sourceURL</span></span>

<span data-ttu-id="8fa67-105">Свойство **саурцеурл** извлекает URL-адрес элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8fa67-105">The **sourceURL** property retrieves the URL of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa67-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fa67-106">Syntax</span></span>

<span data-ttu-id="8fa67-107">*проигрыватель*. *куррентмедиа*. саурцеурл</span><span class="sxs-lookup"><span data-stu-id="8fa67-107">*player*.*currentMedia*.sourceURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="8fa67-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="8fa67-108">Possible Values</span></span>

<span data-ttu-id="8fa67-109">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8fa67-109">This property is a read-only **String**.</span></span>

## <a name="examples"></a><span data-ttu-id="8fa67-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="8fa67-110">Examples</span></span>

<span data-ttu-id="8fa67-111">В следующем примере JScript используется *носитель*. **саурцеурл** для получения URL-адреса первого элемента мультимедиа в образце списка воспроизведения; затем URL-адрес элемента мультимедиа присваивается свойству **URL-адрес** объекта Player.</span><span class="sxs-lookup"><span data-stu-id="8fa67-111">The following JScript example uses *Media*.**sourceURL** to retrieve the URL of the first media item in the sample playlist; the URL of the media item is then assigned to the player object **URL** property.</span></span> <span data-ttu-id="8fa67-112">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="8fa67-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="8fa67-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8fa67-113">Requirements</span></span>



| <span data-ttu-id="8fa67-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8fa67-114">Requirement</span></span> | <span data-ttu-id="8fa67-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8fa67-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa67-116">Версия</span><span class="sxs-lookup"><span data-stu-id="8fa67-116">Version</span></span><br/> | <span data-ttu-id="8fa67-117">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="8fa67-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8fa67-118">DLL</span><span class="sxs-lookup"><span data-stu-id="8fa67-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="8fa67-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fa67-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fa67-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fa67-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa67-121">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="8fa67-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





