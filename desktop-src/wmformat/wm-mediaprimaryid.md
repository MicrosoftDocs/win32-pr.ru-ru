---
title: WM/Медиакласспримарид
description: Атрибут WM/Медиакласспримарид содержит идентификатор GUID основного класса мультимедиа.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Формат Windows Media WM/Медиакласспримарид
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889815"
---
# <a name="wmmediaclassprimaryid"></a><span data-ttu-id="ec8c4-104">WM/Медиакласспримарид</span><span class="sxs-lookup"><span data-stu-id="ec8c4-104">WM/MediaClassPrimaryID</span></span>

<span data-ttu-id="ec8c4-105">Атрибут **WM/медиакласспримарид** содержит идентификатор GUID основного класса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ec8c4-105">The **WM/MediaClassPrimaryID** attribute contains the GUID of the primary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ec8c4-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="ec8c4-106">Global Constant</span></span>

<span data-ttu-id="ec8c4-107">g \_ всзвммедиакласспримарид</span><span class="sxs-lookup"><span data-stu-id="ec8c4-107">g\_wszWMMediaClassPrimaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="ec8c4-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ec8c4-108">Data Type</span></span>

<span data-ttu-id="ec8c4-109">**\_GUID типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="ec8c4-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="ec8c4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec8c4-110">Remarks</span></span>

<span data-ttu-id="ec8c4-111">Для этого атрибута следует задать одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ec8c4-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="ec8c4-112">GUID первичного класса</span><span class="sxs-lookup"><span data-stu-id="ec8c4-112">Primary class GUID</span></span>                     | <span data-ttu-id="ec8c4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ec8c4-113">Description</span></span>                                                  |
|----------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ec8c4-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span><span class="sxs-lookup"><span data-stu-id="ec8c4-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span></span> | <span data-ttu-id="ec8c4-115">Используется для музыкальных файлов.</span><span class="sxs-lookup"><span data-stu-id="ec8c4-115">Use for music files.</span></span> <span data-ttu-id="ec8c4-116">Не используйте для звука, который не является музыкальным.</span><span class="sxs-lookup"><span data-stu-id="ec8c4-116">Do not use for audio that is not music.</span></span> |
| <span data-ttu-id="ec8c4-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span><span class="sxs-lookup"><span data-stu-id="ec8c4-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span></span> | <span data-ttu-id="ec8c4-118">Используется для видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="ec8c4-118">Use for video files.</span></span>                                         |
| <span data-ttu-id="ec8c4-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span><span class="sxs-lookup"><span data-stu-id="ec8c4-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span></span> | <span data-ttu-id="ec8c4-120">Используется для звуковых файлов, которые не являются музыкой.</span><span class="sxs-lookup"><span data-stu-id="ec8c4-120">Use for audio files that are not music.</span></span>                      |
| <span data-ttu-id="ec8c4-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span><span class="sxs-lookup"><span data-stu-id="ec8c4-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span></span> | <span data-ttu-id="ec8c4-122">Используется для файлов, не являющихся ни аудио, ни видео.</span><span class="sxs-lookup"><span data-stu-id="ec8c4-122">Use for files that are neither audio or video.</span></span>               |



 

<span data-ttu-id="ec8c4-123">При указании идентификатора первичного класса необходимо также задать идентификатор дополнительного класса, чтобы уточнить тип содержимого в файле.</span><span class="sxs-lookup"><span data-stu-id="ec8c4-123">When you specify a primary class identifier, you should also set a secondary class identifier to clarify the type of content in the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec8c4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec8c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec8c4-125">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="ec8c4-125">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="ec8c4-126">**WM/Медиакласссекондарид**</span><span class="sxs-lookup"><span data-stu-id="ec8c4-126">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
</dt> </dl>

 

 




