---
description: Указывает среднюю скорость потока в битах в секунду, используемую для кодирования 2-прохода с переменной скоростью (VBR).
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: Свойство MFPKEY_RAVG (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702115"
---
# <a name="mfpkey_ravg-property"></a><span data-ttu-id="a4a9c-103">МФПКЭЙ \_ равг, свойство</span><span class="sxs-lookup"><span data-stu-id="a4a9c-103">MFPKEY\_RAVG Property</span></span>

<span data-ttu-id="a4a9c-104">Указывает среднюю скорость потока в битах в секунду, используемую для кодирования 2-прохода с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="a4a9c-104">Specifies the average bit rate, in bits per second, used for 2-pass, variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a4a9c-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="a4a9c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a4a9c-106">g \_ всзвмвкавгбитрате</span><span class="sxs-lookup"><span data-stu-id="a4a9c-106">g\_wszWMVCAvgBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="a4a9c-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a4a9c-107">Data Type</span></span>

<span data-ttu-id="a4a9c-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a4a9c-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a9c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4a9c-109">Remarks</span></span>

<span data-ttu-id="a4a9c-110">Как с ограничением, так и с неограниченным числом VBR это значение представляет собой среднюю скорость потока в течение всего содержимого.</span><span class="sxs-lookup"><span data-stu-id="a4a9c-110">In both constrained and unconstrained VBR, this value is the average bit rate across the duration of the content.</span></span>

<span data-ttu-id="a4a9c-111">Это значение необходимо задать для обоих режимов кодирования VBR с двумя проходами.</span><span class="sxs-lookup"><span data-stu-id="a4a9c-111">You must set this value for both modes of two-pass VBR encoding.</span></span> <span data-ttu-id="a4a9c-112">После начала обработки образцов вы не должны запрашивать это значение до завершения кодирования потока.</span><span class="sxs-lookup"><span data-stu-id="a4a9c-112">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="a4a9c-113">Кодировщик интерпретирует запрос этого значения как сигнал, над которым находится сеанс кодирования. Следующий образец, который вы обрабатываете, рассматривается как начало нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4a9c-113">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="a4a9c-114">Это свойство также может быть считано в конце сеанса кодирования с 1 проходом VBR.</span><span class="sxs-lookup"><span data-stu-id="a4a9c-114">This property can also be read at the end of a 1-pass VBR encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a9c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a4a9c-115">Requirements</span></span>



| <span data-ttu-id="a4a9c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a4a9c-116">Requirement</span></span> | <span data-ttu-id="a4a9c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a4a9c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a9c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4a9c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a9c-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a4a9c-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a4a9c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4a9c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a9c-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4a9c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a4a9c-122">Header</span><span class="sxs-lookup"><span data-stu-id="a4a9c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4a9c-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4a9c-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4a9c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4a9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a9c-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4a9c-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




