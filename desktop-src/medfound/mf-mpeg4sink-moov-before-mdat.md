---
description: Указывает, что Moov будет записано перед полем mdat в созданном файле.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Атрибут MF_MPEG4SINK_MOOV_BEFORE_MDAT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702337"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a><span data-ttu-id="d87c2-103">MF \_ MPEG4SINK \_ Moov \_ перед \_ атрибутом MDAT</span><span class="sxs-lookup"><span data-stu-id="d87c2-103">MF\_MPEG4SINK\_MOOV\_BEFORE\_MDAT attribute</span></span>

<span data-ttu-id="d87c2-104">Указывает, что "Moov" будет записан перед полем "mdat" в создаваемом файле.</span><span class="sxs-lookup"><span data-stu-id="d87c2-104">Indicates that 'moov' will be written before 'mdat' box in the generated file.</span></span>

## <a name="data-type"></a><span data-ttu-id="d87c2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d87c2-105">Data type</span></span>

<span data-ttu-id="d87c2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d87c2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d87c2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d87c2-107">Remarks</span></span>

<span data-ttu-id="d87c2-108">Поведением приемника мультимедиа MPEG4 по умолчанию является запись "Moov" после поля "mdat".</span><span class="sxs-lookup"><span data-stu-id="d87c2-108">The default behavior of the mpeg4 media sink is to write 'moov' after 'mdat' box.</span></span> <span data-ttu-id="d87c2-109">Установка этого атрибута приводит к тому, что созданный файл будет записывать "Moov" перед полем "mdat".</span><span class="sxs-lookup"><span data-stu-id="d87c2-109">Setting this attribute causes the generated file to write 'moov' before 'mdat' box.</span></span>

<span data-ttu-id="d87c2-110">Чтобы приемник MPEG4 мог использовать этот атрибут, переданный поток байтов не должен относиться к низкому или удаленному.</span><span class="sxs-lookup"><span data-stu-id="d87c2-110">In order for the mpeg4 sink to use this attribute, the byte stream passed in must not be slow seek or remote for .</span></span>

<span data-ttu-id="d87c2-111">Эта функция включает в себя дополнительное копирование и ремуксинг файлов.</span><span class="sxs-lookup"><span data-stu-id="d87c2-111">This feature involves an additional file copying/remuxing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d87c2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d87c2-112">Requirements</span></span>



| <span data-ttu-id="d87c2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d87c2-113">Requirement</span></span> | <span data-ttu-id="d87c2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d87c2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d87c2-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d87c2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d87c2-116">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="d87c2-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d87c2-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d87c2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d87c2-118">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d87c2-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d87c2-119">Header</span><span class="sxs-lookup"><span data-stu-id="d87c2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d87c2-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d87c2-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d87c2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d87c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87c2-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d87c2-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d87c2-123">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d87c2-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




