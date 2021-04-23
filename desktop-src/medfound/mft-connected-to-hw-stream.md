---
description: Указывает, подключено ли аппаратное преобразование Media Foundation к другому MFT на основе оборудования.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Атрибут MFT_CONNECTED_TO_HW_STREAM (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656555"
---
# <a name="mft_connected_to_hw_stream-attribute"></a><span data-ttu-id="597a2-103">MFT \_ подключено \_ к \_ \_ атрибуту потока HW</span><span class="sxs-lookup"><span data-stu-id="597a2-103">MFT\_CONNECTED\_TO\_HW\_STREAM attribute</span></span>

<span data-ttu-id="597a2-104">Указывает, подключено ли аппаратное преобразование Media Foundation к другому MFT на основе оборудования.</span><span class="sxs-lookup"><span data-stu-id="597a2-104">Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.</span></span>

## <a name="data-type"></a><span data-ttu-id="597a2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="597a2-105">Data type</span></span>

<span data-ttu-id="597a2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="597a2-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="597a2-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="597a2-107">Get/set</span></span>

<span data-ttu-id="597a2-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="597a2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="597a2-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="597a2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="597a2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="597a2-110">Remarks</span></span>

<span data-ttu-id="597a2-111">Приложения обычно не используют этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="597a2-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="597a2-112">Этот атрибут используется с МФТС на основе оборудования.</span><span class="sxs-lookup"><span data-stu-id="597a2-112">This attribute is used with hardware-based MFTs.</span></span> <span data-ttu-id="597a2-113">При подключении двух МФТС оборудования в топологии загрузчик топологии присваивает этому атрибуту **значение true** для следующих объектов:</span><span class="sxs-lookup"><span data-stu-id="597a2-113">When two hardware MFTs are connected within a topology, the topology loader sets this attribute to **TRUE** on the following objects:</span></span>

-   <span data-ttu-id="597a2-114">Выходной поток вышестоящей MFT</span><span class="sxs-lookup"><span data-stu-id="597a2-114">The output stream of the upstream MFT</span></span>
-   <span data-ttu-id="597a2-115">Входной поток нисходящих файлов MFT</span><span class="sxs-lookup"><span data-stu-id="597a2-115">The input stream of the downstream MFT</span></span>

<span data-ttu-id="597a2-116">Чтобы получить хранилище атрибутов для выходного потока, загрузчик топологии вызывает [**имфтрансформ:: жетаутпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) в вышестоящей MFT.</span><span class="sxs-lookup"><span data-stu-id="597a2-116">To get the attribute store for the output stream, the topology loader calls [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) on the upstream MFT.</span></span> <span data-ttu-id="597a2-117">Чтобы получить хранилище атрибутов для входного потока, загрузчик топологии вызывает [**имфтрансформ:: жетинпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) в ПОДЧИНЕННОЙ таблице MFT.</span><span class="sxs-lookup"><span data-stu-id="597a2-117">To get the attribute store for the input stream, the topology loader calls [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) on the downstream MFT.</span></span>

<span data-ttu-id="597a2-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="597a2-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="597a2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="597a2-119">Requirements</span></span>



| <span data-ttu-id="597a2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="597a2-120">Requirement</span></span> | <span data-ttu-id="597a2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="597a2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="597a2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="597a2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="597a2-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="597a2-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="597a2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="597a2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="597a2-125">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="597a2-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="597a2-126">Header</span><span class="sxs-lookup"><span data-stu-id="597a2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="597a2-127"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="597a2-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="597a2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="597a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="597a2-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="597a2-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="597a2-130">Оборудование МФТС</span><span class="sxs-lookup"><span data-stu-id="597a2-130">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="597a2-131">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="597a2-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




