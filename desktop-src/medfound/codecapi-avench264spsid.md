---
description: Задает идентификатор набора параметров последовательности (SPS) в единице уровня абстракции сети SPS (NAL) потока битов H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Свойство CODECAPI_AVEncH264SPSID (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143249"
---
# <a name="codecapi_avench264spsid-property"></a><span data-ttu-id="915db-103">КОДЕКАПИ \_ AVEncH264SPSID, свойство</span><span class="sxs-lookup"><span data-stu-id="915db-103">CODECAPI\_AVEncH264SPSID property</span></span>

<span data-ttu-id="915db-104">Задает идентификатор набора параметров последовательности (SPS) в единице уровня абстракции сети SPS (NAL) потока битов H. 264.</span><span class="sxs-lookup"><span data-stu-id="915db-104">Sets the sequence parameter set (SPS) identifier in the SPS network abstraction layer (NAL) unit of the H.264 bit stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="915db-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="915db-105">Data type</span></span>

<span data-ttu-id="915db-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="915db-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="915db-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="915db-107">Property GUID</span></span>

<span data-ttu-id="915db-108">**КОДЕКАПИ \_ AVEncH264SPSID**</span><span class="sxs-lookup"><span data-stu-id="915db-108">**CODECAPI\_AVEncH264SPSID**</span></span>

## <a name="property-value"></a><span data-ttu-id="915db-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="915db-109">Property value</span></span>

<span data-ttu-id="915db-110">Указывает значение **\_ \_ \_ идентификатора набора параметров seq** в единице SPS NAL.</span><span class="sxs-lookup"><span data-stu-id="915db-110">Specifies the value of **seq\_parameter\_set\_id** in the SPS NAL unit.</span></span> <span data-ttu-id="915db-111">Элемент синтаксиса **\_ \_ Set \_ параметра seq** определяет набор параметров последовательности.</span><span class="sxs-lookup"><span data-stu-id="915db-111">The **seq\_parameter\_set\_id** syntax element identifies the sequence parameter set.</span></span> <span data-ttu-id="915db-112">Полученный бит потока можно объединить с другими потоками-потоками для создания более длинного потока, содержащего несколько наборов параметров последовательности с разными идентификаторами SPS.</span><span class="sxs-lookup"><span data-stu-id="915db-112">The resulting bit stream can be concatenated with other bit streams, to produce a longer bit stream that contains multiple sequence parameter sets with different SPS identifiers.</span></span>

<span data-ttu-id="915db-113">Допустимый диапазон — 0 31, как указано в спецификации H. 264/AVC.</span><span class="sxs-lookup"><span data-stu-id="915db-113">The valid range is 0 31, as specified in the H.264/AVC specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="915db-114">Требования</span><span class="sxs-lookup"><span data-stu-id="915db-114">Requirements</span></span>



| <span data-ttu-id="915db-115">Требование</span><span class="sxs-lookup"><span data-stu-id="915db-115">Requirement</span></span> | <span data-ttu-id="915db-116">Значение</span><span class="sxs-lookup"><span data-stu-id="915db-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="915db-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="915db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="915db-118">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="915db-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="915db-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="915db-119">Minimum supported server</span></span><br/> | <span data-ttu-id="915db-120">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="915db-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="915db-121">Header</span><span class="sxs-lookup"><span data-stu-id="915db-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="915db-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="915db-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="915db-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="915db-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915db-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="915db-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="915db-125">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="915db-125">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

