---
title: Атрибут Аверажелевел
description: Атрибут Аверажелевел представляет собой 16-битное значение амплитуды, указывающее средний уровень громкости.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Аверажелевел атрибут Windows Media Player
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694762"
---
# <a name="averagelevel-attribute"></a><span data-ttu-id="df82e-104">Атрибут Аверажелевел</span><span class="sxs-lookup"><span data-stu-id="df82e-104">AverageLevel Attribute</span></span>

<span data-ttu-id="df82e-105">Атрибут **аверажелевел** представляет собой 16-битное значение амплитуды, указывающее средний уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="df82e-105">The **AverageLevel** attribute is a 16-bit amplitude value indicating the average volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="df82e-106">Применение</span><span class="sxs-lookup"><span data-stu-id="df82e-106">Applies To</span></span>

-   [<span data-ttu-id="df82e-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="df82e-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="df82e-108">Часто используемые файлы Windows Media</span><span class="sxs-lookup"><span data-stu-id="df82e-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="df82e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df82e-109">Remarks</span></span>

<span data-ttu-id="df82e-110">Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="df82e-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="df82e-111">Проигрыватель Windows Media задает это значение в одном из следующих экземпляров:</span><span class="sxs-lookup"><span data-stu-id="df82e-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="df82e-112">После копирования файла на скопированный файл.</span><span class="sxs-lookup"><span data-stu-id="df82e-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="df82e-113">После воспроизведения файла (при включенном улучшении автоматического выравнивания громкости).</span><span class="sxs-lookup"><span data-stu-id="df82e-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="df82e-114">Константа Windows Media Format SDK для этого атрибута — g \_ всзаверажелевел.</span><span class="sxs-lookup"><span data-stu-id="df82e-114">The Windows Media Format SDK constant for this attribute is g\_wszAverageLevel.</span></span>

<span data-ttu-id="df82e-115">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="df82e-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="df82e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="df82e-116">Requirements</span></span>



| <span data-ttu-id="df82e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="df82e-117">Requirement</span></span> | <span data-ttu-id="df82e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="df82e-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="df82e-119">Версия</span><span class="sxs-lookup"><span data-stu-id="df82e-119">Version</span></span><br/> | <span data-ttu-id="df82e-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="df82e-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df82e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df82e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df82e-122">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="df82e-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





