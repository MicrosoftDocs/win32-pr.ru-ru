---
description: Указывает, поддерживает ли преобразование Media Foundation (MFT) динамическое изменение формата.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: Атрибут MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702031"
---
# <a name="mft_support_dynamic_format_change-attribute"></a><span data-ttu-id="0f7b0-103">Основная таблица MFT \_ поддерживает \_ \_ \_ атрибут изменения динамического формата</span><span class="sxs-lookup"><span data-stu-id="0f7b0-103">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE attribute</span></span>

<span data-ttu-id="0f7b0-104">Указывает, поддерживает ли преобразование Media Foundation (MFT) динамическое изменение формата.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-104">Specifies whether a Media Foundation transform (MFT) supports dynamic format changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="0f7b0-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0f7b0-105">Data type</span></span>

<span data-ttu-id="0f7b0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-106">**UINT32**</span></span>

<span data-ttu-id="0f7b0-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f7b0-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f7b0-108">Remarks</span></span>

<span data-ttu-id="0f7b0-109">Этот атрибут может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-109">This attribute can have the following values.</span></span>



| <span data-ttu-id="0f7b0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="0f7b0-110">Value</span></span>     | <span data-ttu-id="0f7b0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0f7b0-111">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="0f7b0-112">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-112">**TRUE**</span></span>  | <span data-ttu-id="0f7b0-113">Клиент может изменить входной формат во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-113">The client can change the input format during streaming.</span></span>               |
| <span data-ttu-id="0f7b0-114">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-114">**FALSE**</span></span> | <span data-ttu-id="0f7b0-115">Таблица MFT должна быть остановлена, прежде чем клиент сможет изменить входной формат.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-115">The MFT must be drained before the client can change the input format.</span></span> |



 

<span data-ttu-id="0f7b0-116">Чтобы получить этот атрибут, сначала вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище АТРИБУТОВ для MFT.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-116">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store for the MFT.</span></span> <span data-ttu-id="0f7b0-117">Затем вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-117">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span>

<span data-ttu-id="0f7b0-118">Если [**произошел сбой или атрибут не**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) задан, по умолчанию используется значение **false**.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-118">If [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fails or the attribute is not present, the default value if **FALSE**.</span></span>

<span data-ttu-id="0f7b0-119">[Асинхронный МФТС](asynchronous-mfts.md) должен возвращать значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-119">[Asynchronous MFTs](asynchronous-mfts.md) must return the value **TRUE**.</span></span>

<span data-ttu-id="0f7b0-120">Дополнительные сведения см. в разделе [Обработка изменений в потоковой передаче](handling-stream-changes.md).</span><span class="sxs-lookup"><span data-stu-id="0f7b0-120">For more information, see [Handling Stream Changes](handling-stream-changes.md).</span></span>

<span data-ttu-id="0f7b0-121">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="0f7b0-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f7b0-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0f7b0-122">Requirements</span></span>



| <span data-ttu-id="0f7b0-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0f7b0-123">Requirement</span></span> | <span data-ttu-id="0f7b0-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0f7b0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7b0-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f7b0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0f7b0-126">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="0f7b0-126">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0f7b0-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f7b0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0f7b0-128">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="0f7b0-128">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0f7b0-129">Header</span><span class="sxs-lookup"><span data-stu-id="0f7b0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f7b0-130"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f7b0-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f7b0-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f7b0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f7b0-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f7b0-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0f7b0-133">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="0f7b0-133">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="0f7b0-134">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="0f7b0-134">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="0f7b0-135">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-135">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0f7b0-136">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-136">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0f7b0-137">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="0f7b0-137">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




