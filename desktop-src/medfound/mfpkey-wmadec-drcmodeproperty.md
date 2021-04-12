---
description: Задает динамический режим управления диапазоном, который будет использоваться декодером аудио.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: Свойство MFPKEY_WMADEC_DRCMODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263524"
---
# <a name="mfpkey_wmadec_drcmode-property"></a><span data-ttu-id="4eb39-103">МФПКЭЙ \_ вмадек \_ Дркмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="4eb39-103">MFPKEY\_WMADEC\_DRCMODE Property</span></span>

<span data-ttu-id="4eb39-104">Задает динамический режим управления диапазоном, который будет использоваться декодером аудио.</span><span class="sxs-lookup"><span data-stu-id="4eb39-104">Specifies the dynamic range control mode that the audio decoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4eb39-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="4eb39-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4eb39-106">g \_ всзвмакдрксеттинг</span><span class="sxs-lookup"><span data-stu-id="4eb39-106">g\_wszWMACDRCSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="4eb39-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4eb39-107">Data Type</span></span>

<span data-ttu-id="4eb39-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4eb39-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4eb39-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4eb39-109">Default Value</span></span>

<span data-ttu-id="4eb39-110">0</span><span class="sxs-lookup"><span data-stu-id="4eb39-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb39-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4eb39-111">Remarks</span></span>

<span data-ttu-id="4eb39-112">Это целое число в диапазоне от 0 до 2.</span><span class="sxs-lookup"><span data-stu-id="4eb39-112">This integer value ranges from 0 to 2.</span></span> <span data-ttu-id="4eb39-113">Чем выше значение, тем меньше динамический диапазон распакованных звуковых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4eb39-113">The greater the value, the smaller the dynamic range of the uncompressed audio output.</span></span> <span data-ttu-id="4eb39-114">Значение 0 означает, что кодек не должен выполнять динамический контроль диапазонов, то есть кодек не изменит собственный динамический диапазон закодированного содержимого.</span><span class="sxs-lookup"><span data-stu-id="4eb39-114">A value of 0 signals the codec to perform no dynamic range control, that is, the codec will not alter the inherent dynamic range of the encoded content.</span></span>

<span data-ttu-id="4eb39-115">Если это значение равно 1 или 2, то кодек будет использовать следующие свойства для определения необходимого динамического элемента управления диапазоном:</span><span class="sxs-lookup"><span data-stu-id="4eb39-115">If this value is set to 1 or 2, the codec will use the following properties to determine the needed dynamic range control:</span></span>

-   [<span data-ttu-id="4eb39-116">МФПКЭЙ \_ вмадрк \_ авгреф</span><span class="sxs-lookup"><span data-stu-id="4eb39-116">MFPKEY\_WMADRC\_AVGREF</span></span>](mfpkey-wmadrc-avgrefproperty.md)
-   [<span data-ttu-id="4eb39-117">МФПКЭЙ \_ вмадрк \_ пеакреф</span><span class="sxs-lookup"><span data-stu-id="4eb39-117">MFPKEY\_WMADRC\_PEAKREF</span></span>](mfpkey-wmadrc-peakrefproperty.md)
-   [<span data-ttu-id="4eb39-118">МФПКЭЙ \_ вмадрк \_ авгтаржет</span><span class="sxs-lookup"><span data-stu-id="4eb39-118">MFPKEY\_WMADRC\_AVGTARGET</span></span>](mfpkey-wmadrc-avgtargetproperty.md)
-   [<span data-ttu-id="4eb39-119">МФПКЭЙ \_ вмадрк \_ пеактаржет</span><span class="sxs-lookup"><span data-stu-id="4eb39-119">MFPKEY\_WMADRC\_PEAKTARGET</span></span>](mfpkey-wmadrc-peaktargetproperty.md)

<span data-ttu-id="4eb39-120">Если целевые значения не предоставлены, кодек предоставит свой собственный.</span><span class="sxs-lookup"><span data-stu-id="4eb39-120">If you do not provide target values, the codec will provide its own.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb39-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4eb39-121">Requirements</span></span>



| <span data-ttu-id="4eb39-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4eb39-122">Requirement</span></span> | <span data-ttu-id="4eb39-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4eb39-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb39-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4eb39-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb39-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4eb39-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4eb39-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4eb39-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb39-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4eb39-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4eb39-128">Header</span><span class="sxs-lookup"><span data-stu-id="4eb39-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb39-129"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb39-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb39-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4eb39-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb39-131">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4eb39-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




