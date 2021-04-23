---
description: Указывает максимальное число проходов, поддерживаемое кодировщиком.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Свойство MFPKEY_PASSESRECOMMENDED (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263984"
---
# <a name="mfpkey_passesrecommended-property"></a><span data-ttu-id="3c989-103">МФПКЭЙ \_ пассесрекоммендед, свойство</span><span class="sxs-lookup"><span data-stu-id="3c989-103">MFPKEY\_PASSESRECOMMENDED Property</span></span>

<span data-ttu-id="3c989-104">Указывает максимальное число проходов, поддерживаемое кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="3c989-104">Specifies the maximum number of passes supported by the encoder.</span></span> <span data-ttu-id="3c989-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3c989-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3c989-106">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="3c989-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="3c989-107">g \_ всзвмвкпассесрекоммендед, g \_ всзвмкпмакспассес</span><span class="sxs-lookup"><span data-stu-id="3c989-107">g\_wszWMVCPassesRecommended, g\_wszWMCPMaxPasses</span></span>

## <a name="data-type"></a><span data-ttu-id="3c989-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3c989-108">Data Type</span></span>

<span data-ttu-id="3c989-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3c989-109">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="3c989-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c989-110">Remarks</span></span>

<span data-ttu-id="3c989-111">Можно получить значение этого свойства, вызвав [ивмкодекпропс:: жеткодекпроп](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="3c989-111">You can get the value of this property calling [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="3c989-112">При использовании **ипропертибаг** необходимо сначала задать значение FOURCC нужного сжатого формата с помощью свойства [мфпкэй \_ FourCC](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="3c989-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format by using the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c989-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3c989-113">Requirements</span></span>



| <span data-ttu-id="3c989-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3c989-114">Requirement</span></span> | <span data-ttu-id="3c989-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3c989-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c989-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c989-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c989-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3c989-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3c989-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c989-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c989-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c989-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c989-120">Header</span><span class="sxs-lookup"><span data-stu-id="3c989-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c989-121"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c989-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c989-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c989-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c989-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3c989-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




