---
description: Указывает идентификатор потоковой передачи ядра (KS) для потока на устройстве видеозаписи.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: Атрибут MF_DEVICESTREAM_STREAM_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080489"
---
# <a name="mf_devicestream_stream_id-attribute"></a><span data-ttu-id="97db0-103">\_ \_ Атрибут идентификатора потока MF девицестреам \_</span><span class="sxs-lookup"><span data-stu-id="97db0-103">MF\_DEVICESTREAM\_STREAM\_ID attribute</span></span>

<span data-ttu-id="97db0-104">Указывает идентификатор потоковой передачи ядра (KS) для потока на устройстве видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="97db0-104">Specifies the kernel streaming (KS) identifier for a stream on a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="97db0-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="97db0-105">Data type</span></span>

<span data-ttu-id="97db0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="97db0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="97db0-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97db0-107">Remarks</span></span>

<span data-ttu-id="97db0-108">Чтобы получить этот атрибут, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="97db0-108">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="97db0-109">Запросите источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="97db0-109">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="97db0-110">Вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для потока.</span><span class="sxs-lookup"><span data-stu-id="97db0-110">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="97db0-111">Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="97db0-111">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="97db0-112">Требования</span><span class="sxs-lookup"><span data-stu-id="97db0-112">Requirements</span></span>



| <span data-ttu-id="97db0-113">Требование</span><span class="sxs-lookup"><span data-stu-id="97db0-113">Requirement</span></span> | <span data-ttu-id="97db0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="97db0-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97db0-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97db0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="97db0-116">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="97db0-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="97db0-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97db0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="97db0-118">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="97db0-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="97db0-119">Header</span><span class="sxs-lookup"><span data-stu-id="97db0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="97db0-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="97db0-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97db0-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97db0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97db0-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97db0-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




