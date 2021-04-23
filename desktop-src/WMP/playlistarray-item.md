---
title: Плайлистаррай. Item, метод
description: Метод Item извлекает список воспроизведения по указанному индексу.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс Плайлистаррай
- Класс Плайлистаррай Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718040"
---
# <a name="playlistarrayitem-method"></a><span data-ttu-id="3955b-106">Плайлистаррай. Item, метод</span><span class="sxs-lookup"><span data-stu-id="3955b-106">PlaylistArray.item method</span></span>

<span data-ttu-id="3955b-107">Метод **Item** извлекает список воспроизведения по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="3955b-107">The **item** method retrieves the playlist at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3955b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3955b-108">Syntax</span></span>


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="3955b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3955b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3955b-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3955b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3955b-111">**Число** (**длинное**), содержащее индекс списка воспроизведения, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="3955b-111">**Number** (**long**) containing the index of the playlist to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3955b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3955b-112">Return value</span></span>

<span data-ttu-id="3955b-113">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="3955b-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3955b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3955b-114">Remarks</span></span>

<span data-ttu-id="3955b-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3955b-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3955b-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3955b-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3955b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3955b-117">Requirements</span></span>



| <span data-ttu-id="3955b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3955b-118">Requirement</span></span> | <span data-ttu-id="3955b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3955b-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3955b-120">Версия</span><span class="sxs-lookup"><span data-stu-id="3955b-120">Version</span></span><br/> | <span data-ttu-id="3955b-121">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3955b-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3955b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3955b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="3955b-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3955b-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3955b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3955b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3955b-125">**Объект Плайлистаррай**</span><span class="sxs-lookup"><span data-stu-id="3955b-125">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="3955b-126">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="3955b-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3955b-127">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="3955b-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





