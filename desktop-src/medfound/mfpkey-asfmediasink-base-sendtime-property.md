---
description: Базовое время отправки для приемника мультимедиа ASF в миллисекундах.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: Свойство MFPKEY_ASFMEDIASINK_BASE_SENDTIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693879"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a><span data-ttu-id="420cc-103">МФПКЭЙ \_ асфмедиасинк \_ базовое \_ свойство сендтиме</span><span class="sxs-lookup"><span data-stu-id="420cc-103">MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME property</span></span>

<span data-ttu-id="420cc-104">Базовое время отправки для приемника мультимедиа ASF в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="420cc-104">Base send time for the ASF media sink, in milliseconds.</span></span>



<span data-ttu-id="420cc-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="420cc-105">Data type</span></span>

<span data-ttu-id="420cc-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="420cc-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="420cc-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="420cc-107">PROPVARIANT member</span></span>

<span data-ttu-id="420cc-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="420cc-108">**ULONG**</span></span>

<span data-ttu-id="420cc-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="420cc-109">VT\_UI4</span></span>

<span data-ttu-id="420cc-110">**улвал**</span><span class="sxs-lookup"><span data-stu-id="420cc-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="420cc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="420cc-111">Remarks</span></span>

<span data-ttu-id="420cc-112">Время отправки — это время, когда пакет ASF отправляется по сети.</span><span class="sxs-lookup"><span data-stu-id="420cc-112">The send time is the time at which an ASF packet is sent across the network.</span></span> <span data-ttu-id="420cc-113">Он не соответствует непосредственно времени презентации данных в пакете.</span><span class="sxs-lookup"><span data-stu-id="420cc-113">It does not correspond directly to the presentation time of the data in the packet.</span></span>

<span data-ttu-id="420cc-114">Это свойство можно использовать для настройки приемника мультимедиа ASF.</span><span class="sxs-lookup"><span data-stu-id="420cc-114">You can use this property to configure the ASF media sink.</span></span> <span data-ttu-id="420cc-115">Использование зависит от того, какая функция вызывается для создания приемника мультимедиа ASF:</span><span class="sxs-lookup"><span data-stu-id="420cc-115">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="420cc-116">[**Мфкреатеасфмедиасинк**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): запросите полученный указатель [**Имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) для интерфейса **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="420cc-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="420cc-117">[**Мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): вызов [**Имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) в указателе [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , указанном в параметре *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="420cc-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="420cc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="420cc-118">Requirements</span></span>



| <span data-ttu-id="420cc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="420cc-119">Requirement</span></span> | <span data-ttu-id="420cc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="420cc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="420cc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="420cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="420cc-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="420cc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="420cc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="420cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="420cc-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="420cc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="420cc-125">Header</span><span class="sxs-lookup"><span data-stu-id="420cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="420cc-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="420cc-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="420cc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="420cc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="420cc-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="420cc-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




