---
title: Атрибут Синконли
description: Атрибут Синконли представляет собой строковое представление логического значения, используемого проигрывателем Windows Media для определения того, доступен ли список воспроизведения только для синхронизации.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Синконли атрибут Windows Media Player
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717831"
---
# <a name="synconly-attribute"></a><span data-ttu-id="9eec4-104">Атрибут Синконли</span><span class="sxs-lookup"><span data-stu-id="9eec4-104">SyncOnly Attribute</span></span>

<span data-ttu-id="9eec4-105">Атрибут **синконли** представляет собой строковое представление **логического** значения, используемого проигрывателем Windows Media для определения того, доступен ли список воспроизведения только для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9eec4-105">The **SyncOnly** attribute is a string representation of a **Boolean** value that Windows Media Player uses to determine whether a playlist is available only for synchronization.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9eec4-106">Применение</span><span class="sxs-lookup"><span data-stu-id="9eec4-106">Applies To</span></span>

-   [<span data-ttu-id="9eec4-107">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="9eec4-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="9eec4-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9eec4-108">Remarks</span></span>

<span data-ttu-id="9eec4-109">Значение 1 указывает, что список воспроизведения доступен только для синхронизации и не может отображаться в узле **автосписок воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="9eec4-109">A value of 1 indicates that the playlist is available only for synchronization and cannot appear in the **Auto Playlist** node.</span></span> <span data-ttu-id="9eec4-110">Нулевое значение указывает, что список воспроизведения может отображаться в узле **автосписок воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="9eec4-110">A value of zero indicates that the playlist can appear in the **Auto Playlist** node.</span></span>

<span data-ttu-id="9eec4-111">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="9eec4-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eec4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9eec4-112">Requirements</span></span>



| <span data-ttu-id="9eec4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9eec4-113">Requirement</span></span> | <span data-ttu-id="9eec4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9eec4-114">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="9eec4-115">Версия</span><span class="sxs-lookup"><span data-stu-id="9eec4-115">Version</span></span><br/> | <span data-ttu-id="9eec4-116">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9eec4-116">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9eec4-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9eec4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eec4-118">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="9eec4-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





