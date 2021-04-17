---
title: Список воспроизведения. attributeName
description: Свойство attributeName извлекает имя атрибута по указанному индексу.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Проигрыватель Windows Media для списка воспроизведения. attributeName
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704450"
---
# <a name="playlistattributename"></a><span data-ttu-id="1e275-104">Список воспроизведения. attributeName</span><span class="sxs-lookup"><span data-stu-id="1e275-104">Playlist.attributeName</span></span>

<span data-ttu-id="1e275-105">Свойство **attributeName** извлекает имя атрибута по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="1e275-105">The **attributeName** property retrieves the name of an attribute at a specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e275-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e275-106">Syntax</span></span>

<span data-ttu-id="1e275-107">*проигрыватель*. *куррентплайлист*. **attributeName**( *индекс* )</span><span class="sxs-lookup"><span data-stu-id="1e275-107">*player*.*currentPlaylist*.**attributeName**( *index* )</span></span>

## <a name="parameters"></a><span data-ttu-id="1e275-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e275-108">Parameters</span></span>

<span data-ttu-id="1e275-109">*index*</span><span class="sxs-lookup"><span data-stu-id="1e275-109">*index*</span></span>

<span data-ttu-id="1e275-110">**Число** (**Long**), содержащее индекс.</span><span class="sxs-lookup"><span data-stu-id="1e275-110">**Number** (**long**) containing the index.</span></span>

## <a name="possible-values"></a><span data-ttu-id="1e275-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1e275-111">Possible Values</span></span>

<span data-ttu-id="1e275-112">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e275-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e275-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e275-113">Remarks</span></span>

<span data-ttu-id="1e275-114">Число атрибутов извлекается свойством **аттрибутекаунт** .</span><span class="sxs-lookup"><span data-stu-id="1e275-114">The number of attributes is retrieved by the **attributeCount** property.</span></span> <span data-ttu-id="1e275-115">При наличии индекса атрибут **attributeName** возвращает **строку** , которую можно использовать в сочетании с **сетитеминфо** или **getItemInfo** для указания или получения значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="1e275-115">Given an index, **attributeName** returns a **String** that can be used in conjunction with **setItemInfo** or **getItemInfo** to specify or retrieve a value for the attribute.</span></span>

<span data-ttu-id="1e275-116">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="1e275-116">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="1e275-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1e275-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1e275-118">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e275-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="1e275-119">Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](playlist-attributecount.md) .</span><span class="sxs-lookup"><span data-stu-id="1e275-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e275-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1e275-120">Requirements</span></span>



| <span data-ttu-id="1e275-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1e275-121">Requirement</span></span> | <span data-ttu-id="1e275-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1e275-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e275-123">Версия</span><span class="sxs-lookup"><span data-stu-id="1e275-123">Version</span></span><br/> | <span data-ttu-id="1e275-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1e275-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1e275-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1e275-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e275-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e275-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e275-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e275-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e275-128">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="1e275-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="1e275-129">**Список воспроизведения. Аттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="1e275-129">**Playlist.attributeCount**</span></span>](playlist-attributecount.md)
</dt> <dt>

[<span data-ttu-id="1e275-130">**Список воспроизведения. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1e275-130">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1e275-131">**Список воспроизведения. Сетитеминфо**</span><span class="sxs-lookup"><span data-stu-id="1e275-131">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1e275-132">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="1e275-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1e275-133">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="1e275-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





