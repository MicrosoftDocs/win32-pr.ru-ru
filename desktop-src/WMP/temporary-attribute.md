---
title: Временный атрибут
description: Временный атрибут указывает, является ли список воспроизведения временным.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Временный атрибут Windows Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717829"
---
# <a name="temporary-attribute"></a><span data-ttu-id="c1ee9-104">Временный атрибут</span><span class="sxs-lookup"><span data-stu-id="c1ee9-104">Temporary Attribute</span></span>

<span data-ttu-id="c1ee9-105">**Временный** атрибут указывает, является ли список воспроизведения временным.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-105">The **Temporary** attribute specifies whether a playlist is temporary.</span></span>

<span data-ttu-id="c1ee9-106">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c1ee9-106">**Remarks**</span></span>

<span data-ttu-id="c1ee9-107">Если вы получили список воспроизведения из библиотеки, изменения, внесенные в список воспроизведения, будут отражены в библиотеке пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-107">If you retrieved a playlist from the library, changes you make to the playlist will be reflected in the user's library.</span></span> <span data-ttu-id="c1ee9-108">Чтобы избежать этого, вызовите [ивмпплайлист:: сетитеминфо](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) , передав имя атрибута "Temporary" и значение "true".</span><span class="sxs-lookup"><span data-stu-id="c1ee9-108">To avoid this, call [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passing the attribute name "Temporary" and the value "true".</span></span> <span data-ttu-id="c1ee9-109">При этом экземпляр списка воспроизведения преобразуется во временный список воспроизведения, который можно изменить, не изменяя исходный список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-109">This converts your playlist instance to a temporary playlist, which is safe to edit without changing the original playlist.</span></span>

<span data-ttu-id="c1ee9-110">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c1ee9-110">**Applies To**</span></span>

-   [<span data-ttu-id="c1ee9-111">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="c1ee9-111">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="requirements"></a><span data-ttu-id="c1ee9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c1ee9-112">Requirements</span></span>



| <span data-ttu-id="c1ee9-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c1ee9-113">Requirement</span></span> | <span data-ttu-id="c1ee9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c1ee9-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="c1ee9-115">Версия</span><span class="sxs-lookup"><span data-stu-id="c1ee9-115">Version</span></span><br/> | <span data-ttu-id="c1ee9-116">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="c1ee9-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1ee9-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1ee9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ee9-118">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="c1ee9-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





