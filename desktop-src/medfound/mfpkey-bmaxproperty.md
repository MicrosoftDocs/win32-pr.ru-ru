---
description: Указывает окно буфера (в миллисекундах) для потока с переменным ограничением переменной скорости (VBR) с пиковой скоростью (заданный параметром МФПКЭЙ \_ рмакс).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: Свойство MFPKEY_BMAX (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693605"
---
# <a name="mfpkey_bmax-property"></a><span data-ttu-id="ea3e2-103">МФПКЭЙ \_ бмакс, свойство</span><span class="sxs-lookup"><span data-stu-id="ea3e2-103">MFPKEY\_BMAX Property</span></span>

<span data-ttu-id="ea3e2-104">Указывает окно буфера (в миллисекундах) для потока с переменным ограничением переменной скорости (VBR) с пиковой скоростью (заданный параметром [мфпкэй \_ рмакс](mfpkey-rmaxproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="ea3e2-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by [MFPKEY\_RMAX](mfpkey-rmaxproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ea3e2-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="ea3e2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ea3e2-106">g \_ всзвмвкбмакс</span><span class="sxs-lookup"><span data-stu-id="ea3e2-106">g\_wszWMVCBMax</span></span>

## <a name="data-type"></a><span data-ttu-id="ea3e2-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ea3e2-107">Data Type</span></span>

<span data-ttu-id="ea3e2-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ea3e2-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ea3e2-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ea3e2-109">Default Value</span></span>

<span data-ttu-id="ea3e2-110">Значение по умолчанию отсутствует.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea3e2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea3e2-111">Remarks</span></span>

<span data-ttu-id="ea3e2-112">Необходимо задать это значение для кодирования с пиковой интенсивностью VBR.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-112">You must set this value for peak-constrained VBR encoding.</span></span> <span data-ttu-id="ea3e2-113">После начала обработки образцов вы не должны запрашивать это значение до завершения кодирования потока.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-113">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="ea3e2-114">Кодек интерпретирует запрос этого значения как сигнал, над которым находится сеанс кодирования. Следующий образец, который вы обрабатываете, рассматривается как начало нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea3e2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ea3e2-115">Requirements</span></span>



| <span data-ttu-id="ea3e2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ea3e2-116">Requirement</span></span> | <span data-ttu-id="ea3e2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ea3e2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3e2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea3e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ea3e2-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ea3e2-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ea3e2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea3e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ea3e2-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea3e2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ea3e2-122">Header</span><span class="sxs-lookup"><span data-stu-id="ea3e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea3e2-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea3e2-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea3e2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea3e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea3e2-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea3e2-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




