---
description: Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: Свойство MFPKEY_FOURCC (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991605"
---
# <a name="mfpkey_fourcc-property"></a><span data-ttu-id="8516f-103">МФПКЭЙ \_ FourCC, свойство</span><span class="sxs-lookup"><span data-stu-id="8516f-103">MFPKEY\_FOURCC Property</span></span>

<span data-ttu-id="8516f-104">Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="8516f-104">Specifies the FOURCC that identifies the encoder you want to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8516f-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="8516f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8516f-106">g \_ всзвмвкфауркк</span><span class="sxs-lookup"><span data-stu-id="8516f-106">g\_wszWMVCFOURCC</span></span>

## <a name="data-type"></a><span data-ttu-id="8516f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8516f-107">Data Type</span></span>

<span data-ttu-id="8516f-108">VT \_ I4 (значение FOURCC)</span><span class="sxs-lookup"><span data-stu-id="8516f-108">VT\_I4 (FOURCC value)</span></span>

## <a name="remarks"></a><span data-ttu-id="8516f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8516f-109">Remarks</span></span>

<span data-ttu-id="8516f-110">Это значение необходимо задать перед получением значений для следующих свойств с помощью **ипропертибаг** или **ипропертисторе**:</span><span class="sxs-lookup"><span data-stu-id="8516f-110">You must set this value before retrieving the values for the following properties using **IPropertyBag** or **IPropertyStore**:</span></span>

-   [<span data-ttu-id="8516f-111">МФПКЭЙ \_ буфферфуллнессинфирстбите</span><span class="sxs-lookup"><span data-stu-id="8516f-111">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE</span></span>](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [<span data-ttu-id="8516f-112">МФПКЭЙ \_ пассесрекоммендед</span><span class="sxs-lookup"><span data-stu-id="8516f-112">MFPKEY\_PASSESRECOMMENDED</span></span>](mfpkey-passesrecommendedproperty.md)

<span data-ttu-id="8516f-113">Для получения значений свойств, зависящих от FOURCC, перечисленных выше, следует использовать [**ивмкодекпропс:: жеткодекпроп**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) .</span><span class="sxs-lookup"><span data-stu-id="8516f-113">You should use [**IWMCodecProps::GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) to retrieve the values of the FOURCC-dependent properties listed previously.</span></span> <span data-ttu-id="8516f-114">При использовании **жеткодекпроп** не нужно задавать **мфпкэй \_ FourCC**.</span><span class="sxs-lookup"><span data-stu-id="8516f-114">When using **GetCodecProp**, you do not need to set **MFPKEY\_FOURCC**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8516f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8516f-115">Requirements</span></span>



| <span data-ttu-id="8516f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8516f-116">Requirement</span></span> | <span data-ttu-id="8516f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8516f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8516f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8516f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8516f-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8516f-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8516f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8516f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8516f-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8516f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8516f-122">Header</span><span class="sxs-lookup"><span data-stu-id="8516f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8516f-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8516f-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8516f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8516f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8516f-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8516f-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




