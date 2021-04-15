---
title: Метод списка воспроизведения. getItemInfo
description: Метод getItemInfo извлекает значение атрибута списка воспроизведения.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647949"
---
# <a name="playlistgetiteminfo-method"></a><span data-ttu-id="fc88a-106">Метод списка воспроизведения. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="fc88a-106">Playlist.getItemInfo method</span></span>

<span data-ttu-id="fc88a-107">Метод **getItemInfo** извлекает значение атрибута списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fc88a-107">The **getItemInfo** method retrieves the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc88a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc88a-108">Syntax</span></span>


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="fc88a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc88a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc88a-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc88a-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc88a-111">**Строка** , содержащая имя извлекаемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="fc88a-111">**String** containing the name of the attribute to be retrieved.</span></span> <span data-ttu-id="fc88a-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fc88a-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc88a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc88a-113">Return value</span></span>

<span data-ttu-id="fc88a-114">Этот метод возвращает **строку**.</span><span class="sxs-lookup"><span data-stu-id="fc88a-114">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc88a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc88a-115">Remarks</span></span>

<span data-ttu-id="fc88a-116">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="fc88a-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="fc88a-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fc88a-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fc88a-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="fc88a-118">Examples</span></span>

<span data-ttu-id="fc88a-119">Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](playlist-attributecount.md) .</span><span class="sxs-lookup"><span data-stu-id="fc88a-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc88a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fc88a-120">Requirements</span></span>



| <span data-ttu-id="fc88a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fc88a-121">Requirement</span></span> | <span data-ttu-id="fc88a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fc88a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc88a-123">Версия</span><span class="sxs-lookup"><span data-stu-id="fc88a-123">Version</span></span><br/> | <span data-ttu-id="fc88a-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="fc88a-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fc88a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fc88a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc88a-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc88a-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc88a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc88a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc88a-128">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="fc88a-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="fc88a-129">**Список воспроизведения. Сетитеминфо**</span><span class="sxs-lookup"><span data-stu-id="fc88a-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="fc88a-130">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="fc88a-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fc88a-131">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="fc88a-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





