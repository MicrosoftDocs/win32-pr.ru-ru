---
description: Указывает пиковую скорость потока (в битах в секунду), используемую для воспроизведения с ограничением в 2 прохода с переменной скоростью (VBR).
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: Свойство MFPKEY_RMAX (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263962"
---
# <a name="mfpkey_rmax-property"></a><span data-ttu-id="1f7f6-103">МФПКЭЙ \_ рмакс, свойство</span><span class="sxs-lookup"><span data-stu-id="1f7f6-103">MFPKEY\_RMAX Property</span></span>

<span data-ttu-id="1f7f6-104">Указывает пиковую скорость потока (в битах в секунду), используемую для воспроизведения с ограничением в 2 прохода с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="1f7f6-104">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) playback.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1f7f6-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1f7f6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1f7f6-106">g \_ всзвмвкмаксбитрате</span><span class="sxs-lookup"><span data-stu-id="1f7f6-106">g\_wszWMVCMaxBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="1f7f6-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1f7f6-107">Data Type</span></span>

<span data-ttu-id="1f7f6-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1f7f6-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1f7f6-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1f7f6-109">Default Value</span></span>

<span data-ttu-id="1f7f6-110">Значение по умолчанию отсутствует.</span><span class="sxs-lookup"><span data-stu-id="1f7f6-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f7f6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f7f6-111">Remarks</span></span>

<span data-ttu-id="1f7f6-112">Это значение представляет пиковую скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1f7f6-112">This value represents the peak bit rate for playback.</span></span> <span data-ttu-id="1f7f6-113">Значение параметра [мфпкэй \_ бмакс](mfpkey-bmaxproperty.md) используется для описания буфера с точки зрения этой скорости. фактически, ограниченная скорость действия аналогична постоянной скорости потока (CBR) с использованием этого значения в качестве скорости.</span><span class="sxs-lookup"><span data-stu-id="1f7f6-113">The value of [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is used to describe the buffer in terms of this bit rate; in effect, constrained VBR is similar to constant bit rate (CBR) using this value as the bit rate.</span></span> <span data-ttu-id="1f7f6-114">Однако поток с ограничением VBR можно воспроизводить с более низкой скоростью, пока буфер увеличивается.</span><span class="sxs-lookup"><span data-stu-id="1f7f6-114">However, a constrained VBR stream can be played back at a lower bit rate, as long as the buffer is increased.</span></span>

<span data-ttu-id="1f7f6-115">Это значение необходимо задать для многоэтапной кодировки VBR с ограничением в максимальной нагрузке.</span><span class="sxs-lookup"><span data-stu-id="1f7f6-115">You must set this value for peak-constrained two-pass VBR encoding.</span></span> <span data-ttu-id="1f7f6-116">После начала обработки образцов вы не должны запрашивать это значение до завершения кодирования потока.</span><span class="sxs-lookup"><span data-stu-id="1f7f6-116">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="1f7f6-117">Кодировщик интерпретирует запрос этого значения как сигнал, над которым находится сеанс кодирования. Следующий образец, который вы обрабатываете, рассматривается как начало нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="1f7f6-117">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="1f7f6-118">Обычно это значение составляет от двух до трех раз больше значения параметра [мфпкэй \_ равг](mfpkey-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1f7f6-118">Typically, this value is two to three times greater than the value of [MFPKEY\_RAVG](mfpkey-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f7f6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1f7f6-119">Requirements</span></span>



| <span data-ttu-id="1f7f6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1f7f6-120">Requirement</span></span> | <span data-ttu-id="1f7f6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1f7f6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7f6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f7f6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7f6-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1f7f6-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f7f6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f7f6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7f6-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f7f6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f7f6-126">Header</span><span class="sxs-lookup"><span data-stu-id="1f7f6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f7f6-127"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f6-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f7f6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f7f6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7f6-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f7f6-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




