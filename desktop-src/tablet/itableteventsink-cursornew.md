---
description: Происходит при добавлении нового пера в систему.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: 'Метод Итаблетевентсинк:: Курсорнев'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 31db152eb15d6f980234dc556e277691d3f14959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272633"
---
# <a name="itableteventsinkcursornew-method"></a><span data-ttu-id="42dd8-103">Метод Итаблетевентсинк:: Курсорнев</span><span class="sxs-lookup"><span data-stu-id="42dd8-103">ITabletEventSink::CursorNew method</span></span>

<span data-ttu-id="42dd8-104">Происходит при добавлении нового пера в систему.</span><span class="sxs-lookup"><span data-stu-id="42dd8-104">Occurs when a new stylus is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="42dd8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42dd8-105">Syntax</span></span>


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="42dd8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42dd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42dd8-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42dd8-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42dd8-108">Идентификатор контекста планшета, в который было добавлено новое перо.</span><span class="sxs-lookup"><span data-stu-id="42dd8-108">The identifier of the tablet context where the new stylus was added.</span></span>

</dd> <dt>

<span data-ttu-id="42dd8-109">*согласуется*</span><span class="sxs-lookup"><span data-stu-id="42dd8-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="42dd8-110">Идентификатор нового объекта пера.</span><span class="sxs-lookup"><span data-stu-id="42dd8-110">The identifier of the new stylus object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42dd8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42dd8-111">Return value</span></span>

<span data-ttu-id="42dd8-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="42dd8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="42dd8-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="42dd8-113">Return code</span></span>                                                                            | <span data-ttu-id="42dd8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="42dd8-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="42dd8-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="42dd8-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="42dd8-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="42dd8-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="42dd8-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="42dd8-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="42dd8-118">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="42dd8-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="42dd8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="42dd8-119">Requirements</span></span>



| <span data-ttu-id="42dd8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="42dd8-120">Requirement</span></span> | <span data-ttu-id="42dd8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="42dd8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42dd8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42dd8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="42dd8-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="42dd8-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="42dd8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42dd8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="42dd8-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="42dd8-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="42dd8-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42dd8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="42dd8-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42dd8-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42dd8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42dd8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42dd8-129">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="42dd8-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




