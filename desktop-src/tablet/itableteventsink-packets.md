---
description: Происходит при перемещении пера на дигитайзер.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: 'Итаблетевентсинк: метод:P аккетс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998937"
---
# <a name="itableteventsinkpackets-method"></a><span data-ttu-id="7a21b-103">Итаблетевентсинк: метод:P аккетс</span><span class="sxs-lookup"><span data-stu-id="7a21b-103">ITabletEventSink::Packets method</span></span>

<span data-ttu-id="7a21b-104">Происходит при перемещении пера на дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="7a21b-104">Occurs when the stylus is moving on the digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a21b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a21b-105">Syntax</span></span>


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="7a21b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a21b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a21b-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a21b-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a21b-108">Идентификатор планшета.</span><span class="sxs-lookup"><span data-stu-id="7a21b-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="7a21b-109">*кпктс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a21b-109">*cPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a21b-110">Число пакетов.</span><span class="sxs-lookup"><span data-stu-id="7a21b-110">The number of packets.</span></span>

</dd> <dt>

<span data-ttu-id="7a21b-111">*кбпктс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a21b-111">*cbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a21b-112">Размер буфера пакета</span><span class="sxs-lookup"><span data-stu-id="7a21b-112">The size of packet buffer</span></span>

</dd> <dt>

<span data-ttu-id="7a21b-113">*пбпктс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a21b-113">*pbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a21b-114">Буфер пакетов.</span><span class="sxs-lookup"><span data-stu-id="7a21b-114">The packet buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7a21b-115">*пнсериалнумберс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a21b-115">*pnSerialNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a21b-116">Массив серийных номеров.</span><span class="sxs-lookup"><span data-stu-id="7a21b-116">The serial number array.</span></span>

</dd> <dt>

<span data-ttu-id="7a21b-117">*согласуется*</span><span class="sxs-lookup"><span data-stu-id="7a21b-117">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="7a21b-118">Идентификатор пера.</span><span class="sxs-lookup"><span data-stu-id="7a21b-118">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a21b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a21b-119">Return value</span></span>

<span data-ttu-id="7a21b-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7a21b-120">This method can return one of these values.</span></span>



| <span data-ttu-id="7a21b-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7a21b-121">Return code</span></span>                                                                            | <span data-ttu-id="7a21b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="7a21b-122">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7a21b-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7a21b-123"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7a21b-124">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7a21b-124">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7a21b-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="7a21b-125"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7a21b-126">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7a21b-126">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7a21b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7a21b-127">Requirements</span></span>



| <span data-ttu-id="7a21b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7a21b-128">Requirement</span></span> | <span data-ttu-id="7a21b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7a21b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a21b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a21b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a21b-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7a21b-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7a21b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a21b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a21b-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7a21b-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7a21b-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a21b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a21b-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a21b-135"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a21b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a21b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a21b-137">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="7a21b-137">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




