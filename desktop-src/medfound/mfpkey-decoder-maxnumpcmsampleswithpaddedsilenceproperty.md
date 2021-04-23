---
description: Указывает максимальное количество дополнительных выборок PCM, которые могут быть возвращены в конце после декодирования файла.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: Свойство MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711785"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a><span data-ttu-id="5bfa3-103">\_Свойство макснумпкмсамплесвиспаддедсиленце декодера мфпкэй \_</span><span class="sxs-lookup"><span data-stu-id="5bfa3-103">MFPKEY\_Decoder\_MaxNumPCMSamplesWithPaddedSilence Property</span></span>

<span data-ttu-id="5bfa3-104">Указывает максимальное количество дополнительных выборок PCM, которые могут быть возвращены в конце после декодирования файла.</span><span class="sxs-lookup"><span data-stu-id="5bfa3-104">Specifies the maximum number of additional PCM samples that might be returned at the end of after decoding a file.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5bfa3-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="5bfa3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5bfa3-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="5bfa3-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5bfa3-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5bfa3-107">Data Type</span></span>

<span data-ttu-id="5bfa3-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5bfa3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5bfa3-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5bfa3-109">Default Value</span></span>

<span data-ttu-id="5bfa3-110">2048</span><span class="sxs-lookup"><span data-stu-id="5bfa3-110">2048</span></span>

## <a name="remarks"></a><span data-ttu-id="5bfa3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bfa3-111">Remarks</span></span>

<span data-ttu-id="5bfa3-112">Это свойство можно использовать для оценки искусственного тишина, который вставляется между песнями по мере того, как они помещаются в декодер один за другим.</span><span class="sxs-lookup"><span data-stu-id="5bfa3-112">This property can be used to estimate artificial silence that gets is inserted between songs as they are fed to the decoder one after another.</span></span>

<span data-ttu-id="5bfa3-113">Для декодеров Windows Media Audio 10 Professional и Windows Media Audio 9 без потерь это свойство всегда равно 0.</span><span class="sxs-lookup"><span data-stu-id="5bfa3-113">For the Windows Media Audio 10 Professional and Windows Media Audio 9 Lossless decoders, this property is always equal to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bfa3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5bfa3-114">Requirements</span></span>



| <span data-ttu-id="5bfa3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5bfa3-115">Requirement</span></span> | <span data-ttu-id="5bfa3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5bfa3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bfa3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5bfa3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5bfa3-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5bfa3-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5bfa3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5bfa3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5bfa3-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5bfa3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5bfa3-121">Header</span><span class="sxs-lookup"><span data-stu-id="5bfa3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bfa3-122"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bfa3-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bfa3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bfa3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bfa3-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5bfa3-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
