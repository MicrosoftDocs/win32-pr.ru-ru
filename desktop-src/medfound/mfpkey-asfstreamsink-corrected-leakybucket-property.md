---
description: Указывает &\# 0034, сегмент утечки&\# 0034; параметры для потока в приемнике ASF Media.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: Свойство MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897722"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a><span data-ttu-id="ac999-103">МФПКЭЙ \_ асфстреамсинк, \_ исправленное \_ свойство леакибуккет</span><span class="sxs-lookup"><span data-stu-id="ac999-103">MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET property</span></span>

<span data-ttu-id="ac999-104">Задает параметры "сегмент утечки" (см. примечания) для потока в приемнике ASF Media.</span><span class="sxs-lookup"><span data-stu-id="ac999-104">Specifies the "leaky bucket" parameters (see Remarks) for a stream on an ASF media sink.</span></span>



<span data-ttu-id="ac999-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ac999-105">Data type</span></span>

<span data-ttu-id="ac999-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="ac999-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ac999-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="ac999-107">PROPVARIANT member</span></span>

<span data-ttu-id="ac999-108">Массив значений **типа DWORD** (**Каул**)</span><span class="sxs-lookup"><span data-stu-id="ac999-108">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="ac999-109">VT \_ вектор \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ac999-109">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="ac999-110">**каул**</span><span class="sxs-lookup"><span data-stu-id="ac999-110">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="ac999-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac999-111">Remarks</span></span>

<span data-ttu-id="ac999-112">Приложение может задать это свойство в потоке приемника мультимедиа ASF после согласования типа носителя для потока.</span><span class="sxs-lookup"><span data-stu-id="ac999-112">An application can set this property on a stream of the ASF media sink after the media type for the stream is negotiated.</span></span> <span data-ttu-id="ac999-113">Используйте это свойство, чтобы указать фактическое окно буфера, которое будет использоваться кодеком Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ac999-113">Use this property to specify the actual buffer window that the Windows Media codec will use.</span></span> <span data-ttu-id="ac999-114">Эти сведения можно получить из кодека с помощью интерфейса **ивмкодеклеакибуккет** , который описан в пакете SDK для формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ac999-114">You can obtain this information from the codec by using the **IWMCodecLeakyBucket** interface, which is documented in the Windows Media Format SDK.</span></span>

<span data-ttu-id="ac999-115">Значение этого свойства представляет собой массив из трех значений **типа DWORD** в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="ac999-115">The value of this property is an array of three **DWORD** values in the following order:</span></span>

-   <span data-ttu-id="ac999-116">Скорость в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="ac999-116">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="ac999-117">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="ac999-117">Buffer size, in bytes.</span></span>
-   <span data-ttu-id="ac999-118">Заполнение начальной буферизации в байтах.</span><span class="sxs-lookup"><span data-stu-id="ac999-118">Initial buffer fullness, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac999-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ac999-119">Requirements</span></span>



| <span data-ttu-id="ac999-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ac999-120">Requirement</span></span> | <span data-ttu-id="ac999-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ac999-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac999-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac999-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac999-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac999-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ac999-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac999-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac999-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac999-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ac999-126">Header</span><span class="sxs-lookup"><span data-stu-id="ac999-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac999-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac999-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac999-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac999-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac999-129">**имфстреамсинк**</span><span class="sxs-lookup"><span data-stu-id="ac999-129">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[<span data-ttu-id="ac999-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac999-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




