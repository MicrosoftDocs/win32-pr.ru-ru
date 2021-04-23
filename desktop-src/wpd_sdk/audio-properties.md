---
description: Портативные устройства Windows поддерживают следующие свойства аудио.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Свойства аудио (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694743"
---
# <a name="audio-properties"></a><span data-ttu-id="9526f-103">Свойства звука</span><span class="sxs-lookup"><span data-stu-id="9526f-103">Audio Properties</span></span>

<span data-ttu-id="9526f-104">Портативные устройства Windows поддерживают следующие свойства аудио.</span><span class="sxs-lookup"><span data-stu-id="9526f-104">Windows Portable Devices supports the following audio properties.</span></span>



| <span data-ttu-id="9526f-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="9526f-105">Property</span></span>                         | <span data-ttu-id="9526f-106">VarType</span><span class="sxs-lookup"><span data-stu-id="9526f-106">VarType</span></span>     | <span data-ttu-id="9526f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9526f-107">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9526f-108">**\_ \_ Битовая глубина звука \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="9526f-108">**WPD\_AUDIO\_BIT\_DEPTH**</span></span>       | <span data-ttu-id="9526f-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="9526f-109">**VT\_UI4**</span></span> | <span data-ttu-id="9526f-110">Битовая глубина звука.</span><span class="sxs-lookup"><span data-stu-id="9526f-110">The bit-depth of the audio.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="9526f-111">**\_звуковая \_ скорость WPD**</span><span class="sxs-lookup"><span data-stu-id="9526f-111">**WPD\_AUDIO\_BITRATE**</span></span>          | <span data-ttu-id="9526f-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="9526f-112">**VT\_UI4**</span></span> | <span data-ttu-id="9526f-113">Битовая скорость звука в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="9526f-113">The bit rate of the audio, in bits per second.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="9526f-114">**\_Выравнивание аудио \_ блока \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="9526f-114">**WPD\_AUDIO\_BLOCK\_ALIGNMENT**</span></span> | <span data-ttu-id="9526f-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="9526f-115">**VT\_UI4**</span></span> | <span data-ttu-id="9526f-116">Выравнивание блока для звукового файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="9526f-116">The block alignment of the audio file, in bytes.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="9526f-117">**\_число звуковых \_ каналов WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9526f-117">**WPD\_AUDIO\_CHANNEL\_COUNT**</span></span>   | <span data-ttu-id="9526f-118">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="9526f-118">**VT\_R4**</span></span>  | <span data-ttu-id="9526f-119">Число каналов в этом звуковом файле, например 1, 2 или 5,1.</span><span class="sxs-lookup"><span data-stu-id="9526f-119">The number of channels in this audio file, for example, 1, 2, or 5.1.</span></span>                                                                                                                                              |
| <span data-ttu-id="9526f-120">**\_код звукового \_ формата WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9526f-120">**WPD\_AUDIO\_FORMAT\_CODE**</span></span>     | <span data-ttu-id="9526f-121">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="9526f-121">**VT\_UI4**</span></span> | <span data-ttu-id="9526f-122">Номер зарегистрированного кода формата WAVE.</span><span class="sxs-lookup"><span data-stu-id="9526f-122">The registered WAVE format code number.</span></span> <span data-ttu-id="9526f-123">Список зарегистрированных форматов WAVE см. в статье [зарегистрированные коды FourCC и форматы Wave](https://msdn2.microsoft.com/library/ms867195.aspx) на веб-сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="9526f-123">For a listing of registered WAVE formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9526f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9526f-124">Requirements</span></span>



| <span data-ttu-id="9526f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9526f-125">Requirement</span></span> | <span data-ttu-id="9526f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9526f-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9526f-127">Header</span><span class="sxs-lookup"><span data-stu-id="9526f-127">Header</span></span><br/> | <dl> <span data-ttu-id="9526f-128"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="9526f-128"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9526f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9526f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9526f-130">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="9526f-130">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




