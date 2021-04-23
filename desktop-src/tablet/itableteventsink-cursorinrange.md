---
description: Происходит, когда перо попадает в диапазон обнаружения дигитайзера.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'Метод Итаблетевентсинк:: Курсоринранже'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eec2b4f309480ecaecd50de2120d701c916b6fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684512"
---
# <a name="itableteventsinkcursorinrange-method"></a><span data-ttu-id="d9fcf-103">Метод Итаблетевентсинк:: Курсоринранже</span><span class="sxs-lookup"><span data-stu-id="d9fcf-103">ITabletEventSink::CursorInRange method</span></span>

<span data-ttu-id="d9fcf-104">Происходит, когда перо попадает в диапазон обнаружения дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="d9fcf-104">Occurs when a stylus comes within the digitizer's range of detection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9fcf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9fcf-105">Syntax</span></span>


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="d9fcf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9fcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9fcf-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9fcf-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9fcf-108">Идентификатор объекта планшета, который обнаружил перо.</span><span class="sxs-lookup"><span data-stu-id="d9fcf-108">The identifier of the tablet object that detected the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="d9fcf-109">*согласуется*</span><span class="sxs-lookup"><span data-stu-id="d9fcf-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="d9fcf-110">Идентификатор объекта пера, который находится в диапазоне диджитайзера.</span><span class="sxs-lookup"><span data-stu-id="d9fcf-110">The identifier of the stylus object that has come in range of the digitizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9fcf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9fcf-111">Return value</span></span>

<span data-ttu-id="d9fcf-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d9fcf-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d9fcf-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d9fcf-113">Return code</span></span>                                                                            | <span data-ttu-id="d9fcf-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d9fcf-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d9fcf-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d9fcf-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d9fcf-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d9fcf-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d9fcf-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="d9fcf-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d9fcf-118">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d9fcf-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d9fcf-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d9fcf-119">Requirements</span></span>



| <span data-ttu-id="d9fcf-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d9fcf-120">Requirement</span></span> | <span data-ttu-id="d9fcf-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d9fcf-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9fcf-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9fcf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d9fcf-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d9fcf-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d9fcf-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9fcf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d9fcf-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d9fcf-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d9fcf-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9fcf-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9fcf-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d9fcf-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9fcf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9fcf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9fcf-129">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="d9fcf-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




