---
description: Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: Свойство MFPKEY_BUFFERFULLNESSINFIRSTBYTE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693604"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a><span data-ttu-id="4df14-103">МФПКЭЙ \_ буфферфуллнессинфирстбите, свойство</span><span class="sxs-lookup"><span data-stu-id="4df14-103">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE Property</span></span>

<span data-ttu-id="4df14-104">Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.</span><span class="sxs-lookup"><span data-stu-id="4df14-104">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4df14-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="4df14-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4df14-106">g \_ всзвмвкбуфферфуллнессинфирстбите</span><span class="sxs-lookup"><span data-stu-id="4df14-106">g\_wszWMVCBufferFullnessInFirstByte</span></span>

## <a name="data-type"></a><span data-ttu-id="4df14-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4df14-107">Data Type</span></span>

<span data-ttu-id="4df14-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="4df14-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="4df14-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4df14-109">Remarks</span></span>

<span data-ttu-id="4df14-110">Перед получением этого значения необходимо задать выходной тип.</span><span class="sxs-lookup"><span data-stu-id="4df14-110">You must set an output type before getting this value.</span></span>

<span data-ttu-id="4df14-111">Значение этого свойства можно получить с помощью [ивмкодекпропс:: жеткодекпроп](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="4df14-111">You can get the value of this property using [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="4df14-112">При использовании **ипропертибаг** необходимо сначала задать значение FOURCC нужного сжатого формата с помощью свойства [мфпкэй \_ FourCC](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="4df14-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format with the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

<span data-ttu-id="4df14-113">Заполнение буфера в первом байте всех ключевых кадров позволяет определить размер буфера, необходимый при объединении сжатых потоков видео.</span><span class="sxs-lookup"><span data-stu-id="4df14-113">Having the buffer fullness in the first byte of all key frames enables you to determine the buffer size required when concatenating compressed video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df14-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4df14-114">Requirements</span></span>



| <span data-ttu-id="4df14-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4df14-115">Requirement</span></span> | <span data-ttu-id="4df14-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4df14-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df14-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4df14-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4df14-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4df14-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4df14-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4df14-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4df14-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4df14-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4df14-121">Header</span><span class="sxs-lookup"><span data-stu-id="4df14-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df14-122"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df14-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df14-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4df14-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df14-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4df14-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




