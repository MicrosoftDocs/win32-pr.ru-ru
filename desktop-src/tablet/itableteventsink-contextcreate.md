---
description: Происходит при создании нового контекста планшета.
ms.assetid: 64e1f778-90c1-417d-a80b-37aeecffd411
title: 'Метод Итаблетевентсинк:: Контексткреате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextCreate
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e622a246c7c317cf9e3373cbd3791108ed071e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349412"
---
# <a name="itableteventsinkcontextcreate-method"></a><span data-ttu-id="5097a-103">Метод Итаблетевентсинк:: Контексткреате</span><span class="sxs-lookup"><span data-stu-id="5097a-103">ITabletEventSink::ContextCreate method</span></span>

<span data-ttu-id="5097a-104">Происходит при создании нового контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="5097a-104">Occurs when a new tablet context is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="5097a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5097a-105">Syntax</span></span>


```C++
HRESULT ContextCreate(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="5097a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5097a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5097a-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5097a-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5097a-108">Идентификатор создаваемого контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="5097a-108">The identifier of the tablet context being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5097a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5097a-109">Return value</span></span>

<span data-ttu-id="5097a-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5097a-110">This method can return one of these values.</span></span>



| <span data-ttu-id="5097a-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5097a-111">Return code</span></span>                                                                            | <span data-ttu-id="5097a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5097a-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="5097a-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5097a-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="5097a-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5097a-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="5097a-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="5097a-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="5097a-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5097a-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5097a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5097a-117">Requirements</span></span>



| <span data-ttu-id="5097a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5097a-118">Requirement</span></span> | <span data-ttu-id="5097a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5097a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5097a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5097a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5097a-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5097a-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5097a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5097a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5097a-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5097a-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5097a-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5097a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="5097a-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5097a-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5097a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5097a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5097a-127">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="5097a-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




