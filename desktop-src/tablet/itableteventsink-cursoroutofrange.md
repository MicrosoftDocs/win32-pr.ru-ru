---
description: Происходит, когда перо покидает диапазон физического обнаружения (близость) планшета.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: 'Метод Итаблетевентсинк:: Курсораутофранже'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e2250401f3888bd07ff250549c11c34e6a54576d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913296"
---
# <a name="itableteventsinkcursoroutofrange-method"></a><span data-ttu-id="a22e9-103">Метод Итаблетевентсинк:: Курсораутофранже</span><span class="sxs-lookup"><span data-stu-id="a22e9-103">ITabletEventSink::CursorOutOfRange method</span></span>

<span data-ttu-id="a22e9-104">Происходит, когда перо покидает диапазон физического обнаружения (близость) планшета.</span><span class="sxs-lookup"><span data-stu-id="a22e9-104">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a22e9-105">Syntax</span></span>


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="a22e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a22e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a22e9-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a22e9-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a22e9-108">Идентификатор планшета.</span><span class="sxs-lookup"><span data-stu-id="a22e9-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="a22e9-109">*согласуется*</span><span class="sxs-lookup"><span data-stu-id="a22e9-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="a22e9-110">Идентификатор пера.</span><span class="sxs-lookup"><span data-stu-id="a22e9-110">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a22e9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a22e9-111">Return value</span></span>

<span data-ttu-id="a22e9-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a22e9-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a22e9-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a22e9-113">Return code</span></span>                                                                            | <span data-ttu-id="a22e9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a22e9-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a22e9-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a22e9-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a22e9-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a22e9-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="a22e9-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a22e9-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a22e9-118">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a22e9-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a22e9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a22e9-119">Requirements</span></span>



| <span data-ttu-id="a22e9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a22e9-120">Requirement</span></span> | <span data-ttu-id="a22e9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a22e9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a22e9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a22e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a22e9-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a22e9-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a22e9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a22e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a22e9-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a22e9-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a22e9-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a22e9-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a22e9-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a22e9-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22e9-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a22e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22e9-129">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="a22e9-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




