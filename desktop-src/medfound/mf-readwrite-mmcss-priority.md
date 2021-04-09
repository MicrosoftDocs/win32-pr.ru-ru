---
description: Задает приоритет базового потока для модуля чтения исходного кода или средства записи приемника.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: Атрибут MF_READWRITE_MMCSS_PRIORITY (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081467"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a><span data-ttu-id="3205a-103">\_ \_ \_ Атрибут приоритета MMCSS для MF ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3205a-103">MF\_READWRITE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="3205a-104">Задает приоритет базового потока для модуля чтения исходного кода или средства записи приемника.</span><span class="sxs-lookup"><span data-stu-id="3205a-104">Sets the base thread priority for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="3205a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3205a-105">Data type</span></span>

<span data-ttu-id="3205a-106">**Int32** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3205a-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3205a-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="3205a-107">Get/set</span></span>

<span data-ttu-id="3205a-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3205a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3205a-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3205a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="3205a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3205a-110">Remarks</span></span>

<span data-ttu-id="3205a-111">При необходимости задайте этот атрибут при создании экземпляра модуля [чтения источника](source-reader.md) или [средства записи приемника](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="3205a-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="3205a-112">Если этот атрибут задан, также необходимо задать атрибут [ \_ \_ \_ класса MMCSS MF ReadWrite](mf-readwrite-mmcss-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3205a-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute.</span></span> <span data-ttu-id="3205a-113">В противном случае этот атрибут игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3205a-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="3205a-114">Когда модуль чтения источника или модуль записи приемника регистрирует потоки с помощью [службы планировщика классов мультимедиа](../procthread/multimedia-class-scheduler-service.md), значение этого атрибута указывает базовый приоритет потока.</span><span class="sxs-lookup"><span data-stu-id="3205a-114">When the Source Reader or Sink Writer registers threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="3205a-115">Если этот атрибут не задан, значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3205a-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3205a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3205a-116">Requirements</span></span>



| <span data-ttu-id="3205a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3205a-117">Requirement</span></span> | <span data-ttu-id="3205a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3205a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3205a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3205a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3205a-120">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="3205a-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="3205a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3205a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3205a-122">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="3205a-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="3205a-123">Header</span><span class="sxs-lookup"><span data-stu-id="3205a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3205a-124"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="3205a-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3205a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3205a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3205a-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3205a-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
