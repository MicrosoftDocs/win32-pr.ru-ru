---
description: Указывает, будет ли приемник мультимедиа ASF автоматически корректировать скорость потока.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: Свойство MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693880"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a><span data-ttu-id="34b8e-103">\_Свойство мфпкэй асфмедиасинк \_ АВТОнастройки скорости \_</span><span class="sxs-lookup"><span data-stu-id="34b8e-103">MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE property</span></span>

<span data-ttu-id="34b8e-104">Указывает, будет ли приемник мультимедиа ASF автоматически корректировать скорость потока.</span><span class="sxs-lookup"><span data-stu-id="34b8e-104">Specifies whether the ASF media sink automatically adjusts the bit rate.</span></span>



<span data-ttu-id="34b8e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="34b8e-105">Data type</span></span>

<span data-ttu-id="34b8e-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="34b8e-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="34b8e-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="34b8e-107">PROPVARIANT member</span></span>

<span data-ttu-id="34b8e-108">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="34b8e-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="34b8e-109">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="34b8e-109">VT\_BOOL</span></span>

<span data-ttu-id="34b8e-110">**булвал**</span><span class="sxs-lookup"><span data-stu-id="34b8e-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="34b8e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34b8e-111">Remarks</span></span>

<span data-ttu-id="34b8e-112">Если значение этого свойства равно \_ true, приемник мультимедиа ASF автоматически корректирует скорость передачи содержимого ASF в ответ на характеристики мультиплексированных потоков.</span><span class="sxs-lookup"><span data-stu-id="34b8e-112">If the value of this property is VARIANT\_TRUE, the ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span>

<span data-ttu-id="34b8e-113">Это свойство влияет на работу приемника мультимедиа ASF, когда поток переполняет параметры "сегмент утечки" приемника:</span><span class="sxs-lookup"><span data-stu-id="34b8e-113">This property affects how the ASF media sink behaves when a stream overflows the sink's "leaky bucket" parameters:</span></span>



| <span data-ttu-id="34b8e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="34b8e-114">Value</span></span>              | <span data-ttu-id="34b8e-115">Поведение</span><span class="sxs-lookup"><span data-stu-id="34b8e-115">Behavior</span></span>                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b8e-116">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="34b8e-116">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="34b8e-117">Приемник мультимедиа ASF автоматически корректирует скорость передачи содержимого ASF в ответ на характеристики мультиплексирования потоков.</span><span class="sxs-lookup"><span data-stu-id="34b8e-117">The ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span> |
| <span data-ttu-id="34b8e-118">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="34b8e-118">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="34b8e-119">Приемник мультимедиа ASF использует значение скорости потока, предоставленное приложением.</span><span class="sxs-lookup"><span data-stu-id="34b8e-119">The ASF media sink uses the stream bit rate value provided by the application.</span></span>                                                                |



 

<span data-ttu-id="34b8e-120">Значение по умолчанию — **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="34b8e-120">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="34b8e-121">Задайте это свойство при настройке приемника мультимедиа ASF.</span><span class="sxs-lookup"><span data-stu-id="34b8e-121">Set this property when you configure the ASF media sink.</span></span> <span data-ttu-id="34b8e-122">Использование зависит от того, какая функция вызывается для создания приемника мультимедиа ASF:</span><span class="sxs-lookup"><span data-stu-id="34b8e-122">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="34b8e-123">[**Мфкреатеасфмедиасинк**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): запросите полученный указатель [**Имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) для интерфейса **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="34b8e-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="34b8e-124">[**Мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): вызов [**Имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) в указателе [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , указанном в параметре *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="34b8e-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

<span data-ttu-id="34b8e-125">Если задать для этого свойства значение "VARIANT true", \_ приемник мультимедиа ASF должен установить флаг **\_ \_ авторегулировки \_ скорости мфасф мультиплексора** в мультиплексоре ASF.</span><span class="sxs-lookup"><span data-stu-id="34b8e-125">Setting this property to VARIANT\_TRUE causes the ASF media sink to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag on the ASF multiplexer.</span></span> <span data-ttu-id="34b8e-126">См. раздел [**имфасфмултиплексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span><span class="sxs-lookup"><span data-stu-id="34b8e-126">See [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span></span>

<span data-ttu-id="34b8e-127">Дополнительные сведения о концепции сегмента утечки см. в разделе «Модель буфера с буферным сегментом» документации по пакету SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="34b8e-127">For more information about the leaky bucket concept, see the topic "The Leaky Bucket Buffer Model" in the Windows Media Format SDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="34b8e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="34b8e-128">Requirements</span></span>



| <span data-ttu-id="34b8e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="34b8e-129">Requirement</span></span> | <span data-ttu-id="34b8e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="34b8e-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34b8e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34b8e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="34b8e-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34b8e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34b8e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34b8e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="34b8e-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34b8e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34b8e-135">Header</span><span class="sxs-lookup"><span data-stu-id="34b8e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="34b8e-136"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="34b8e-136"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b8e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34b8e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b8e-138">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34b8e-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="34b8e-139">**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="34b8e-139">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[<span data-ttu-id="34b8e-140">**MF \_ асфстреамконфиг \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="34b8e-140">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




