---
title: Довнлоадитем. getItemInfo, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод getItemInfo извлекает значение атрибута для элемента загрузки.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод Windows Media Player, класс Довнлоадитем
- Класс Довнлоадитем Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694830"
---
# <a name="downloaditemgetiteminfo-method"></a><span data-ttu-id="ba080-108">Довнлоадитем. getItemInfo, метод</span><span class="sxs-lookup"><span data-stu-id="ba080-108">DownloadItem.getItemInfo method</span></span>

> [!Note]  
> <span data-ttu-id="ba080-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="ba080-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ba080-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ba080-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ba080-111">Метод **getItemInfo** извлекает значение атрибута для элемента загрузки.</span><span class="sxs-lookup"><span data-stu-id="ba080-111">The **getItemInfo** method retrieves the value of an attribute for the download item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba080-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba080-112">Syntax</span></span>


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a><span data-ttu-id="ba080-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba080-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba080-114">*ItemName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba080-114">*itemname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba080-115">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="ba080-115">**String** containing the attribute name.</span></span> <span data-ttu-id="ba080-116">Поддерживаемые значения: Албумартист, альбом, длительность, WM/provider, Title, Усерратинг и WM/Траккнумбер.</span><span class="sxs-lookup"><span data-stu-id="ba080-116">Supported values are AlbumArtist, Album, Duration, WM/Provider, Title, UserRating, and WM/TrackNumber.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba080-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba080-117">Return value</span></span>

<span data-ttu-id="ba080-118">Этот метод возвращает **строку** , содержащую значение атрибута, заданного параметром *ItemName*.</span><span class="sxs-lookup"><span data-stu-id="ba080-118">This method returns a **String** containing the value of the attribute specified by *itemname*.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba080-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba080-119">Remarks</span></span>

<span data-ttu-id="ba080-120">Этот метод извлекает атрибуты, указанные с помощью строки описания BITS.</span><span class="sxs-lookup"><span data-stu-id="ba080-120">This method retrieves attributes specified using the BITS description string.</span></span> <span data-ttu-id="ba080-121">См. раздел [соглашение о задании BITS в проигрывателе Windows Media](windows-media-player-bits-job-convention.md).</span><span class="sxs-lookup"><span data-stu-id="ba080-121">See [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md).</span></span>

<span data-ttu-id="ba080-122">Этот метод поддерживается для фонового скачивания.</span><span class="sxs-lookup"><span data-stu-id="ba080-122">This method is supported for background downloading.</span></span> <span data-ttu-id="ba080-123">Код не должен вызывать этот метод при использовании загрузки в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="ba080-123">Your code should not call this method when using real-time downloading.</span></span>

<span data-ttu-id="ba080-124">Этот метод может получать сведения о заданиях BITS, добавленных только в текущем сеансе проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ba080-124">This method can retrieve information for BITS jobs added during the current Windows Media Player session only.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba080-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ba080-125">Requirements</span></span>



| <span data-ttu-id="ba080-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ba080-126">Requirement</span></span> | <span data-ttu-id="ba080-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ba080-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba080-128">Версия</span><span class="sxs-lookup"><span data-stu-id="ba080-128">Version</span></span><br/> | <span data-ttu-id="ba080-129">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ba080-129">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="ba080-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ba080-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba080-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba080-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba080-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba080-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba080-133">**Довнлоадитем. тип**</span><span class="sxs-lookup"><span data-stu-id="ba080-133">**DownloadItem.type**</span></span>](downloaditem-type.md)
</dt> <dt>

[<span data-ttu-id="ba080-134">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="ba080-134">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





