---
description: '\_Константы побитового флага линегасертерм описывают условия, при которых сбор буферизованных цифр завершается.'
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Константы LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680031"
---
# <a name="linegatherterm_-constants"></a><span data-ttu-id="0778d-103">\_Константы линегасертерм</span><span class="sxs-lookup"><span data-stu-id="0778d-103">LINEGATHERTERM\_ Constants</span></span>

<span data-ttu-id="0778d-104">Константы побитового флага **линегасертерм \_** описывают условия, при которых сбор буферизованных цифр завершается.</span><span class="sxs-lookup"><span data-stu-id="0778d-104">The **LINEGATHERTERM\_** bit-flag constants describe the conditions under which buffered digit gathering is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="0778d-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**ЛИНЕГАСЕРТЕРМ \_ буфферфулл**</span><span class="sxs-lookup"><span data-stu-id="0778d-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM\_BUFFERFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0778d-106">Было собрано запрошенное количество цифр.</span><span class="sxs-lookup"><span data-stu-id="0778d-106">The requested number of digits has been gathered.</span></span> <span data-ttu-id="0778d-107">Буфер заполнен.</span><span class="sxs-lookup"><span data-stu-id="0778d-107">The buffer is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0778d-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**ЛИНЕГАСЕРТЕРМ \_ Отмена**</span><span class="sxs-lookup"><span data-stu-id="0778d-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0778d-109">Запрос был отменен этим приложением, другим приложением или из-за прекращения вызова.</span><span class="sxs-lookup"><span data-stu-id="0778d-109">The request was canceled by this application, by another application, or because the call terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0778d-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**ЛИНЕГАСЕРТЕРМ \_ фирсттимеаут**</span><span class="sxs-lookup"><span data-stu-id="0778d-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM\_FIRSTTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0778d-111">Истекло время ожидания первой цифры.</span><span class="sxs-lookup"><span data-stu-id="0778d-111">The first digit timeout expired.</span></span> <span data-ttu-id="0778d-112">Буфер не содержит цифр.</span><span class="sxs-lookup"><span data-stu-id="0778d-112">The buffer contains no digits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0778d-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**ЛИНЕГАСЕРТЕРМ \_**</span><span class="sxs-lookup"><span data-stu-id="0778d-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM\_INTERTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0778d-114">Время ожидания между цифрами истекло.</span><span class="sxs-lookup"><span data-stu-id="0778d-114">The inter-digit timeout expired.</span></span> <span data-ttu-id="0778d-115">Буфер содержит по крайней мере одну цифру.</span><span class="sxs-lookup"><span data-stu-id="0778d-115">The buffer contains at least one digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0778d-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**ЛИНЕГАСЕРТЕРМ \_ термдигит**</span><span class="sxs-lookup"><span data-stu-id="0778d-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM\_TERMDIGIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0778d-117">Одна из цифр завершения соответствует полученной цифре.</span><span class="sxs-lookup"><span data-stu-id="0778d-117">One of the termination digits matched a received digit.</span></span> <span data-ttu-id="0778d-118">Сопоставленная конечная цифра — это последняя цифра в буфере.</span><span class="sxs-lookup"><span data-stu-id="0778d-118">The matched termination digit is the last digit in the buffer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0778d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0778d-119">Remarks</span></span>

<span data-ttu-id="0778d-120">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="0778d-120">No extensibility.</span></span> <span data-ttu-id="0778d-121">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="0778d-121">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="0778d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0778d-122">Requirements</span></span>



| <span data-ttu-id="0778d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0778d-123">Requirement</span></span> | <span data-ttu-id="0778d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0778d-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0778d-125">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0778d-125">TAPI version</span></span><br/> | <span data-ttu-id="0778d-126">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0778d-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0778d-127">Header</span><span class="sxs-lookup"><span data-stu-id="0778d-127">Header</span></span><br/>       | <dl> <span data-ttu-id="0778d-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0778d-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




