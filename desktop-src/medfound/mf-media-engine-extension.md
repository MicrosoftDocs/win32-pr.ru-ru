---
description: Содержит указатель на интерфейс Имфмедиаенгиникстенсион.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: Атрибут MF_MEDIA_ENGINE_EXTENSION (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104424130"
---
# <a name="mf_media_engine_extension-attribute"></a><span data-ttu-id="608f4-103">\_ \_ Атрибут расширения обработчика мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="608f4-103">MF\_MEDIA\_ENGINE\_EXTENSION attribute</span></span>

<span data-ttu-id="608f4-104">Содержит указатель на интерфейс [**имфмедиаенгиникстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="608f4-104">Contains a pointer to the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="608f4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="608f4-105">Data type</span></span>

<span data-ttu-id="608f4-106">**Имфмедиаенгиникстенсион \* *_ хранится как _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="608f4-106">**IMFMediaEngineExtension\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="608f4-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="608f4-107">Get/set</span></span>

<span data-ttu-id="608f4-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="608f4-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="608f4-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="608f4-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="608f4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="608f4-110">Remarks</span></span>

<span data-ttu-id="608f4-111">Этот атрибут используется с методом [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) для инициализации механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="608f4-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="608f4-112">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="608f4-112">This attribute is optional.</span></span> <span data-ttu-id="608f4-113">Используйте его для предоставления объекта, реализующего интерфейс [**имфмедиаенгиникстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="608f4-113">Use it to provide an object that implements the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span> <span data-ttu-id="608f4-114">Этот интерфейс позволяет приложению загружать пользовательские ресурсы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="608f4-114">This interface enables the application to load custom media resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="608f4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="608f4-115">Requirements</span></span>



| <span data-ttu-id="608f4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="608f4-116">Requirement</span></span> | <span data-ttu-id="608f4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="608f4-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="608f4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="608f4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="608f4-119">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="608f4-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="608f4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="608f4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="608f4-121">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="608f4-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="608f4-122">Header</span><span class="sxs-lookup"><span data-stu-id="608f4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="608f4-123"><dt>Мфмедиаенгине. h</dt></span><span class="sxs-lookup"><span data-stu-id="608f4-123"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="608f4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="608f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="608f4-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="608f4-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




