---
title: Атрибут Пеаквалуе
description: Атрибут Пеаквалуе представляет собой 16-битное значение амплитуды, указывающее пиковый уровень громкости.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Пеаквалуе атрибут Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699118"
---
# <a name="peakvalue-attribute"></a><span data-ttu-id="67afc-104">Атрибут Пеаквалуе</span><span class="sxs-lookup"><span data-stu-id="67afc-104">PeakValue Attribute</span></span>

<span data-ttu-id="67afc-105">Атрибут **пеаквалуе** представляет собой 16-битное значение амплитуды, указывающее пиковый уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="67afc-105">The **PeakValue** attribute is a 16-bit amplitude value indicating the peak volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="67afc-106">Применение</span><span class="sxs-lookup"><span data-stu-id="67afc-106">Applies To</span></span>

-   [<span data-ttu-id="67afc-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="67afc-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="67afc-108">Часто используемые файлы Windows Media</span><span class="sxs-lookup"><span data-stu-id="67afc-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="67afc-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67afc-109">Remarks</span></span>

<span data-ttu-id="67afc-110">Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="67afc-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="67afc-111">Проигрыватель Windows Media задает это значение в одном из следующих экземпляров:</span><span class="sxs-lookup"><span data-stu-id="67afc-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="67afc-112">После копирования файла на скопированный файл.</span><span class="sxs-lookup"><span data-stu-id="67afc-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="67afc-113">После воспроизведения файла (при включенном улучшении автоматического выравнивания громкости).</span><span class="sxs-lookup"><span data-stu-id="67afc-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="67afc-114">Константа Windows Media Format SDK для этого атрибута — g \_ всзпеаквалуе.</span><span class="sxs-lookup"><span data-stu-id="67afc-114">The Windows Media Format SDK constant for this attribute is g\_wszPeakValue.</span></span>

<span data-ttu-id="67afc-115">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="67afc-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="67afc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="67afc-116">Requirements</span></span>



| <span data-ttu-id="67afc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="67afc-117">Requirement</span></span> | <span data-ttu-id="67afc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="67afc-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="67afc-119">Версия</span><span class="sxs-lookup"><span data-stu-id="67afc-119">Version</span></span><br/> | <span data-ttu-id="67afc-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="67afc-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67afc-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67afc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67afc-122">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="67afc-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





