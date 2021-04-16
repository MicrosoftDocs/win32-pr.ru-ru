---
description: Задает среднее &\# 0034;&\# 0034; параметров (см. примечания) для кодирования файла Windows Media. Задайте этот атрибут с помощью интерфейса Имфасфстреамконфиг.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: Атрибут MF_ASFSTREAMCONFIG_LEAKYBUCKET1 (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692670"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a><span data-ttu-id="cb921-104">\_Атрибут MF асфстреамконфиг \_ LEAKYBUCKET1</span><span class="sxs-lookup"><span data-stu-id="cb921-104">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1 attribute</span></span>

<span data-ttu-id="cb921-105">Задает среднее значение параметра "сегмент утечки" (см. примечания) для кодирования файла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cb921-105">Sets the average "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="cb921-106">Задайте этот атрибут с помощью интерфейса [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="cb921-106">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb921-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cb921-107">Data type</span></span>

<span data-ttu-id="cb921-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="cb921-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="cb921-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb921-109">Remarks</span></span>

<span data-ttu-id="cb921-110">Значение этого атрибута представляет собой массив из трех **DWORD** в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="cb921-110">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="cb921-111">Скорость в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="cb921-111">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="cb921-112">Окно буфера в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="cb921-112">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="cb921-113">Заполнение начальной буферизации в байтах.</span><span class="sxs-lookup"><span data-stu-id="cb921-113">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="cb921-114">Дополнительные сведения о концепции сегмента утечки см. в разделе [модель буферного контейнера с утечкой](the-leaky-bucket-buffer-model.md) данных в документации пакета Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cb921-114">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="cb921-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="cb921-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb921-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cb921-116">Requirements</span></span>



| <span data-ttu-id="cb921-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cb921-117">Requirement</span></span> | <span data-ttu-id="cb921-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cb921-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb921-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb921-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb921-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb921-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cb921-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb921-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb921-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb921-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cb921-123">Header</span><span class="sxs-lookup"><span data-stu-id="cb921-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb921-124"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb921-124"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb921-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb921-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb921-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb921-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb921-127">Атрибуты ASF</span><span class="sxs-lookup"><span data-stu-id="cb921-127">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb921-128">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="cb921-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="cb921-129">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="cb921-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="cb921-130">**MF \_ асфстреамконфиг \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="cb921-130">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




