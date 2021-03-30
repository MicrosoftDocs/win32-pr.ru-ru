---
description: Происходит, когда подсказка пера обращается к поверхности планшета в дигитайзере.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'Метод Итаблетевентсинк:: Курсордовн'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814432"
---
# <a name="itableteventsinkcursordown-method"></a><span data-ttu-id="c3809-103">Метод Итаблетевентсинк:: Курсордовн</span><span class="sxs-lookup"><span data-stu-id="c3809-103">ITabletEventSink::CursorDown method</span></span>

<span data-ttu-id="c3809-104">Происходит, когда подсказка пера обращается к поверхности планшета в дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="c3809-104">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3809-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3809-105">Syntax</span></span>


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="c3809-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3809-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3809-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3809-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3809-108">Идентификатор планшета.</span><span class="sxs-lookup"><span data-stu-id="c3809-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="c3809-109">*CID* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c3809-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3809-110">Идентификатор пера.</span><span class="sxs-lookup"><span data-stu-id="c3809-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="c3809-111">*нсериалнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3809-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3809-112">Серийный номер пера.</span><span class="sxs-lookup"><span data-stu-id="c3809-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="c3809-113">*кбпкт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3809-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3809-114">Число байтов в пакете данных пера.</span><span class="sxs-lookup"><span data-stu-id="c3809-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="c3809-115">*пбпкт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3809-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3809-116">Данные пера, указывающие расположение, в котором перо затронуло планшета.</span><span class="sxs-lookup"><span data-stu-id="c3809-116">The stylus data indicating the location where the stylus touched the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3809-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3809-117">Return value</span></span>

<span data-ttu-id="c3809-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c3809-118">This method can return one of these values.</span></span>



| <span data-ttu-id="c3809-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c3809-119">Return code</span></span>                                                                            | <span data-ttu-id="c3809-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c3809-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c3809-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c3809-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c3809-122">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c3809-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="c3809-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="c3809-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c3809-124">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c3809-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c3809-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c3809-125">Requirements</span></span>



| <span data-ttu-id="c3809-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c3809-126">Requirement</span></span> | <span data-ttu-id="c3809-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c3809-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3809-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3809-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c3809-129">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c3809-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c3809-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3809-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c3809-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c3809-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c3809-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3809-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3809-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3809-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3809-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3809-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3809-135">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="c3809-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




