---
title: Список воспроизведения. Аттрибутекаунт
description: Свойство Аттрибутекаунт извлекает количество атрибутов, связанных с списком воспроизведения.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Проигрыватель Windows Media Player. Аттрибутекаунт
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708322"
---
# <a name="playlistattributecount"></a><span data-ttu-id="2235e-104">Список воспроизведения. Аттрибутекаунт</span><span class="sxs-lookup"><span data-stu-id="2235e-104">Playlist.attributeCount</span></span>

<span data-ttu-id="2235e-105">Свойство **аттрибутекаунт** извлекает количество атрибутов, связанных с списком воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2235e-105">The **attributeCount** property retrieves the number of attributes associated with the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="2235e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2235e-106">Syntax</span></span>

<span data-ttu-id="2235e-107">*проигрыватель*. *куррентплайлист*. **аттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="2235e-107">*player*.*currentPlaylist*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="2235e-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="2235e-108">Possible Values</span></span>

<span data-ttu-id="2235e-109">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="2235e-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2235e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2235e-110">Remarks</span></span>

<span data-ttu-id="2235e-111">Так как списки воспроизведения могут поступать из множества различных источников, они могут иметь несколько разных наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="2235e-111">Because playlists can come from many different sources, they can have several different sets of properties.</span></span> <span data-ttu-id="2235e-112">Этот метод извлекает общее число доступных свойств, чтобы другие методы объекта **списка воспроизведения** могли получить к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="2235e-112">This method retrieves the total number of properties available so that the other methods of the **Playlist** object can access them.</span></span>

<span data-ttu-id="2235e-113">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2235e-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="2235e-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2235e-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2235e-115">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2235e-115">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2235e-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="2235e-116">Examples</span></span>

<span data-ttu-id="2235e-117">В следующем примере JScript показано, как используются различные свойства и методы **списка воспроизведения** и объектов **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="2235e-117">The following JScript example illustrates how various properties and methods of the **Playlist** and **Media** objects are used.</span></span>


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a><span data-ttu-id="2235e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2235e-118">Requirements</span></span>



| <span data-ttu-id="2235e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2235e-119">Requirement</span></span> | <span data-ttu-id="2235e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2235e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2235e-121">Версия</span><span class="sxs-lookup"><span data-stu-id="2235e-121">Version</span></span><br/> | <span data-ttu-id="2235e-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2235e-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2235e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2235e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="2235e-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2235e-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2235e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2235e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2235e-126">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="2235e-126">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="2235e-127">**Список воспроизведения. attributeName**</span><span class="sxs-lookup"><span data-stu-id="2235e-127">**Playlist.attributeName**</span></span>](playlist-attributename.md)
</dt> <dt>

[<span data-ttu-id="2235e-128">**Список воспроизведения. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2235e-128">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2235e-129">**Список воспроизведения. Сетитеминфо**</span><span class="sxs-lookup"><span data-stu-id="2235e-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2235e-130">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="2235e-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2235e-131">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="2235e-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





