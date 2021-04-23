---
description: Задает пиковое &\# 0034;&\# 0034; параметров (см. примечания) для кодирования файла Windows Media. Эти параметры используются для пиковой скорости. Задайте этот атрибут с помощью интерфейса Имфасфстреамконфиг.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: Атрибут MF_ASFSTREAMCONFIG_LEAKYBUCKET2 (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674013"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a><span data-ttu-id="1106a-105">\_Атрибут MF асфстреамконфиг \_ LEAKYBUCKET2</span><span class="sxs-lookup"><span data-stu-id="1106a-105">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2 attribute</span></span>

<span data-ttu-id="1106a-106">Задает пиковые параметры "сегмент утечки" (см. примечания) для кодирования файла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1106a-106">Sets the peak "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="1106a-107">Эти параметры используются для пиковой скорости.</span><span class="sxs-lookup"><span data-stu-id="1106a-107">These parameters are used for the peak bit rate.</span></span> <span data-ttu-id="1106a-108">Задайте этот атрибут с помощью интерфейса [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="1106a-108">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="1106a-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1106a-109">Data type</span></span>

<span data-ttu-id="1106a-110">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="1106a-110">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="1106a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1106a-111">Remarks</span></span>

<span data-ttu-id="1106a-112">Значение этого атрибута представляет собой массив из трех **DWORD** в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="1106a-112">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="1106a-113">Скорость в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="1106a-113">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="1106a-114">Окно буфера в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="1106a-114">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="1106a-115">Заполнение начальной буферизации в байтах.</span><span class="sxs-lookup"><span data-stu-id="1106a-115">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="1106a-116">Дополнительные сведения о концепции сегмента утечки см. в разделе [модель буферного контейнера с утечкой](the-leaky-bucket-buffer-model.md) данных в документации пакета Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="1106a-116">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="1106a-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="1106a-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1106a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1106a-118">Requirements</span></span>



| <span data-ttu-id="1106a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1106a-119">Requirement</span></span> | <span data-ttu-id="1106a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1106a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1106a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1106a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1106a-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1106a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1106a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1106a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1106a-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1106a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1106a-125">Header</span><span class="sxs-lookup"><span data-stu-id="1106a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1106a-126"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="1106a-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1106a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1106a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1106a-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1106a-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1106a-129">Атрибуты ASF</span><span class="sxs-lookup"><span data-stu-id="1106a-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="1106a-130">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="1106a-130">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="1106a-131">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="1106a-131">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="1106a-132">**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="1106a-132">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




