---
description: Задает исходную метку времени устройства для образца.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: Атрибут MFSampleExtension_DeviceReferenceSystemTime (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898194"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a><span data-ttu-id="7540e-103">Мфсампликстенсион \_ девицереференцесистемтиме, атрибут</span><span class="sxs-lookup"><span data-stu-id="7540e-103">MFSampleExtension\_DeviceReferenceSystemTime attribute</span></span>

<span data-ttu-id="7540e-104">Задает исходную метку времени устройства для образца.</span><span class="sxs-lookup"><span data-stu-id="7540e-104">Specifies the original device timestamp on the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="7540e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7540e-105">Data type</span></span>

<span data-ttu-id="7540e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="7540e-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="7540e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7540e-107">Remarks</span></span>

<span data-ttu-id="7540e-108">Это метка времени ссылки на устройство примеры носителей в разрешении 100 нс.</span><span class="sxs-lookup"><span data-stu-id="7540e-108">This is the a device reference time stamp of media samples in 100ns resolution.</span></span> <span data-ttu-id="7540e-109">Эта отметка времени может не содержать фактическое значение счетчика производительности запросов (QPC) в зависимости от источника, производящего выборки.</span><span class="sxs-lookup"><span data-stu-id="7540e-109">This time stamp may or may not carry the actual value of the query performance counter (QPC), depending on the source producing the samples.</span></span> <span data-ttu-id="7540e-110">Это значение может быть изменено другими компонентами в конвейере мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7540e-110">This value may be modified by other components in the media pipeline.</span></span> <span data-ttu-id="7540e-111">Это значение недоступно для МФТС, вставленного в конвейер захвата.</span><span class="sxs-lookup"><span data-stu-id="7540e-111">This value is not available to MFTs inserted into the capture pipeline.</span></span>

## <a name="requirements"></a><span data-ttu-id="7540e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7540e-112">Requirements</span></span>



| <span data-ttu-id="7540e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7540e-113">Requirement</span></span> | <span data-ttu-id="7540e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7540e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7540e-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7540e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7540e-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7540e-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7540e-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7540e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7540e-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7540e-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7540e-119">Header</span><span class="sxs-lookup"><span data-stu-id="7540e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7540e-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="7540e-120"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="7540e-121">IDL</span><span class="sxs-lookup"><span data-stu-id="7540e-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7540e-122"><dt>Mfcaptureengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7540e-122"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7540e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7540e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7540e-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7540e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




