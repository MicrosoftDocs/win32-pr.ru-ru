---
description: Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с средней скоростью (заданным параметром МФПКЭЙ \_ равг).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: Свойство MFPKEY_BAVG (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693050"
---
# <a name="mfpkey_bavg-property"></a><span data-ttu-id="ecbfa-103">МФПКЭЙ \_ бавг, свойство</span><span class="sxs-lookup"><span data-stu-id="ecbfa-103">MFPKEY\_BAVG Property</span></span>

<span data-ttu-id="ecbfa-104">Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с средней скоростью (заданным параметром [мфпкэй \_ равг](mfpkey-ravgproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="ecbfa-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by [MFPKEY\_RAVG](mfpkey-ravgproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ecbfa-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="ecbfa-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ecbfa-106">g \_ всзвмвкбавг</span><span class="sxs-lookup"><span data-stu-id="ecbfa-106">g\_wszWMVCBAvg</span></span>

## <a name="data-type"></a><span data-ttu-id="ecbfa-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ecbfa-107">Data Type</span></span>

<span data-ttu-id="ecbfa-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ecbfa-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ecbfa-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ecbfa-109">Default Value</span></span>

<span data-ttu-id="ecbfa-110">Значение по умолчанию отсутствует, но кодек вычислит соответствующее значение на основе других параметров с ограничением VBR.</span><span class="sxs-lookup"><span data-stu-id="ecbfa-110">No default value, but the codec will compute an appropriate value based on the other constrained VBR settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecbfa-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecbfa-111">Remarks</span></span>

<span data-ttu-id="ecbfa-112">Это значение высчитывается кодеком после окончательного прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="ecbfa-112">This value is computed by the codec after the final encoding pass.</span></span> <span data-ttu-id="ecbfa-113">Не запрашивать это значение до завершения кодирования.</span><span class="sxs-lookup"><span data-stu-id="ecbfa-113">You should not query for this value until after encoding is complete.</span></span> <span data-ttu-id="ecbfa-114">Кодек интерпретирует запрос этого значения как сигнал, над которым находится сеанс кодирования. Следующий образец, который вы обрабатываете, рассматривается как начало нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="ecbfa-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbfa-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ecbfa-115">Requirements</span></span>



| <span data-ttu-id="ecbfa-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ecbfa-116">Requirement</span></span> | <span data-ttu-id="ecbfa-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ecbfa-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbfa-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecbfa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ecbfa-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ecbfa-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ecbfa-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecbfa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ecbfa-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ecbfa-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ecbfa-122">Header</span><span class="sxs-lookup"><span data-stu-id="ecbfa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecbfa-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecbfa-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbfa-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecbfa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbfa-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ecbfa-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




