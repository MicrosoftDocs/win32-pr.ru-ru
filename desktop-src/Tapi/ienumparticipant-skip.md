---
description: Метод Skip пропускает следующее заданное число элементов в последовательности перечисления. Этот метод скрыт от Visual Basic и языков сценариев.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'Метод ИенумпартиЦипант:: Skip (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689127"
---
# <a name="ienumparticipantskip-method"></a><span data-ttu-id="6390f-104">Метод ИенумпартиЦипант:: Skip</span><span class="sxs-lookup"><span data-stu-id="6390f-104">IEnumParticipant::Skip method</span></span>

<span data-ttu-id="6390f-105">\[**Пропуск** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6390f-105">\[**Skip** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6390f-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="6390f-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6390f-107">Метод **Skip** пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="6390f-107">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="6390f-108">Этот метод скрыт от Visual Basic и языков сценариев.</span><span class="sxs-lookup"><span data-stu-id="6390f-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="6390f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6390f-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="6390f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6390f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6390f-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6390f-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6390f-112">Число пропускаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="6390f-112">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6390f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6390f-113">Return value</span></span>

<span data-ttu-id="6390f-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="6390f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="6390f-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6390f-115">Return code</span></span>                                                                                   | <span data-ttu-id="6390f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6390f-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6390f-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6390f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6390f-118">Число пропущенных элементов: *celt*.</span><span class="sxs-lookup"><span data-stu-id="6390f-118">Number of elements skipped was *celt*.</span></span><br/>               |
| <dl> <span data-ttu-id="6390f-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6390f-119"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="6390f-120">Число пропущенных элементов не является *celt*.</span><span class="sxs-lookup"><span data-stu-id="6390f-120">Number of elements skipped was not *celt*.</span></span><br/>           |
| <dl> <span data-ttu-id="6390f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6390f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6390f-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="6390f-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6390f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6390f-123">Requirements</span></span>



| <span data-ttu-id="6390f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6390f-124">Requirement</span></span> | <span data-ttu-id="6390f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6390f-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6390f-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="6390f-126">TAPI version</span></span><br/> | <span data-ttu-id="6390f-127">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6390f-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6390f-128">Header</span><span class="sxs-lookup"><span data-stu-id="6390f-128">Header</span></span><br/>       | <dl> <span data-ttu-id="6390f-129"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="6390f-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="6390f-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6390f-130">Library</span></span><br/>      | <dl> <span data-ttu-id="6390f-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6390f-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6390f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6390f-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="6390f-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6390f-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6390f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6390f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6390f-135">**иенумпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="6390f-135">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="6390f-136">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="6390f-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




