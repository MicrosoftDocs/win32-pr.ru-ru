---
title: Медиаколлектион. Жетмедиаатом, метод
description: Метод Жетмедиаатом извлекает индекс, по которому указанный атрибут находится в наборе доступных атрибутов.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- Жетмедиаатом метод Windows Media Player
- Жетмедиаатом метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетмедиаатом
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688780"
---
# <a name="mediacollectiongetmediaatom-method"></a><span data-ttu-id="38a10-106">Медиаколлектион. Жетмедиаатом, метод</span><span class="sxs-lookup"><span data-stu-id="38a10-106">MediaCollection.getMediaAtom method</span></span>

<span data-ttu-id="38a10-107">Метод **жетмедиаатом** извлекает индекс, по которому указанный атрибут находится в наборе доступных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="38a10-107">The **getMediaAtom** method retrieves the index at which a specified attribute resides within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a10-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38a10-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="38a10-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="38a10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a10-110">*атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38a10-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38a10-111">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="38a10-111">**String** containing the attribute name.</span></span> <span data-ttu-id="38a10-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="38a10-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a10-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38a10-113">Return value</span></span>

<span data-ttu-id="38a10-114">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="38a10-114">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="38a10-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38a10-115">Remarks</span></span>

<span data-ttu-id="38a10-116">Номер индекса, полученный с помощью этого метода, может быть передан на *носитель*. метод **жетитеминфобятом** для доступа к значениям атрибутов.</span><span class="sxs-lookup"><span data-stu-id="38a10-116">The index number retrieved with this method can be passed to the *Media*.**getItemInfoByAtom** method to access attribute values.</span></span> <span data-ttu-id="38a10-117">Эта методика обычно более эффективна при работе с большими списками воспроизведения, чем доступ к значению атрибута по имени через *носитель*. **getItemInfo** или *Media*. **жетитеминфобитипе**.</span><span class="sxs-lookup"><span data-stu-id="38a10-117">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span>

<span data-ttu-id="38a10-118">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="38a10-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="38a10-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="38a10-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38a10-120">Требования</span><span class="sxs-lookup"><span data-stu-id="38a10-120">Requirements</span></span>



| <span data-ttu-id="38a10-121">Требование</span><span class="sxs-lookup"><span data-stu-id="38a10-121">Requirement</span></span> | <span data-ttu-id="38a10-122">Значение</span><span class="sxs-lookup"><span data-stu-id="38a10-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38a10-123">Версия</span><span class="sxs-lookup"><span data-stu-id="38a10-123">Version</span></span><br/> | <span data-ttu-id="38a10-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="38a10-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="38a10-125">DLL</span><span class="sxs-lookup"><span data-stu-id="38a10-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="38a10-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38a10-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a10-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38a10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a10-128">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="38a10-128">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="38a10-129">**Media. Жетитеминфобятом**</span><span class="sxs-lookup"><span data-stu-id="38a10-129">**Media.getItemInfoByAtom**</span></span>](media-getiteminfobyatom.md)
</dt> <dt>

[<span data-ttu-id="38a10-130">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="38a10-130">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="38a10-131">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="38a10-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="38a10-132">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="38a10-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="38a10-133">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="38a10-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





