---
description: Указывает, следует ли загружать в топологии Microsoft Media Foundation преобразования на основе оборудования (МФТС).
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: Атрибут MF_TOPOLOGY_HARDWARE_MODE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701307"
---
# <a name="mf_topology_hardware_mode-attribute"></a><span data-ttu-id="b626b-103">\_ \_ Атрибут режима оборудования топологии MF \_</span><span class="sxs-lookup"><span data-stu-id="b626b-103">MF\_TOPOLOGY\_HARDWARE\_MODE attribute</span></span>

<span data-ttu-id="b626b-104">Указывает, следует ли загружать в топологии Microsoft Media Foundation преобразования на основе оборудования (МФТС).</span><span class="sxs-lookup"><span data-stu-id="b626b-104">Specifies whether to load hardware-based Microsoft Media Foundation transforms (MFTs) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="b626b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b626b-105">Data type</span></span>

<span data-ttu-id="b626b-106">**[**Мфтопологи \_ \_Режим оборудования**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b626b-106">**[**MFTOPOLOGY\_HARDWARE\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b626b-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="b626b-107">Get/set</span></span>

<span data-ttu-id="b626b-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b626b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b626b-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b626b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b626b-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="b626b-110">Applies to</span></span>

[<span data-ttu-id="b626b-111">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="b626b-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="b626b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b626b-112">Remarks</span></span>

<span data-ttu-id="b626b-113">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b626b-113">This attribute is optional.</span></span> <span data-ttu-id="b626b-114">Задайте атрибут перед разрешением топологии.</span><span class="sxs-lookup"><span data-stu-id="b626b-114">Set the attribute before resolving the topology.</span></span>



| <span data-ttu-id="b626b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b626b-115">Value</span></span>                                  | <span data-ttu-id="b626b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b626b-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b626b-117">**МФТОПОЛОГИ \_ хвмоде \_ использование \_ оборудования**</span><span class="sxs-lookup"><span data-stu-id="b626b-117">**MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**</span></span>  | <span data-ttu-id="b626b-118">Загрузчик топологии будет загружать аппаратные МФТС, такие как аппаратные декодеры, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="b626b-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="b626b-119">Загрузчик топологии автоматически возвращается к программному декодированию, если аппаратный декодер не найден или если аппаратный декодер не может подключиться по какой-либо причине.</span><span class="sxs-lookup"><span data-stu-id="b626b-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="b626b-120">**\_ \_ только программное обеспечение мфтопологи хвмоде \_**</span><span class="sxs-lookup"><span data-stu-id="b626b-120">**MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**</span></span> | <span data-ttu-id="b626b-121">Загрузчик топологии будет загружать только МФТС программного обеспечения, включая программные декодеры.</span><span class="sxs-lookup"><span data-stu-id="b626b-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="b626b-122">Значение по умолчанию — **мфтопологи \_ хвмоде \_ Software \_ только** для совместимости с существующими приложениями.</span><span class="sxs-lookup"><span data-stu-id="b626b-122">The default value is **MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**, for compatibility with existing applications.</span></span> <span data-ttu-id="b626b-123">Рекомендуемое значение — **мфтопологи \_ хвмоде \_ использовать \_ оборудование**.</span><span class="sxs-lookup"><span data-stu-id="b626b-123">The recommended value is **MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**.</span></span>

<span data-ttu-id="b626b-124">Если загрузчик топологии вставляет в топологию основную таблицу оборудования, в узле Topology задается атрибут [ \_ \_ \_ \_ атрибута «URL-адрес перечисления MFT](mft-enum-hardware-url-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="b626b-124">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="b626b-125">Чтобы проверить наличие в файле MFT оборудования, перечислите узлы в разрешенной топологии и проверьте наличие этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="b626b-125">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="b626b-126">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b626b-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b626b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b626b-127">Requirements</span></span>



| <span data-ttu-id="b626b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b626b-128">Requirement</span></span> | <span data-ttu-id="b626b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b626b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b626b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b626b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b626b-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b626b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b626b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b626b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b626b-133">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b626b-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b626b-134">Header</span><span class="sxs-lookup"><span data-stu-id="b626b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b626b-135"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b626b-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b626b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b626b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b626b-137">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b626b-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b626b-138">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="b626b-138">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




