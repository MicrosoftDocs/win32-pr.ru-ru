---
description: Происходит при наведении курсора мыши на планшетном дигитайзере.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'Метод Итаблетевентсинк:: Курсормове'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684406"
---
# <a name="itableteventsinkcursormove-method"></a><span data-ttu-id="7b0da-103">Метод Итаблетевентсинк:: Курсормове</span><span class="sxs-lookup"><span data-stu-id="7b0da-103">ITabletEventSink::CursorMove method</span></span>

<span data-ttu-id="7b0da-104">Происходит при наведении курсора мыши на планшетном дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="7b0da-104">Occurs when the cursor moves over the tablet digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b0da-105">Syntax</span></span>


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a><span data-ttu-id="7b0da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b0da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b0da-107">*тЦид*</span><span class="sxs-lookup"><span data-stu-id="7b0da-107">*tcid*</span></span> 
</dt> <dd>

<span data-ttu-id="7b0da-108">Уникальный дентифиер планшетного дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="7b0da-108">Unique dentifier of the tablet digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="7b0da-109">*согласуется*</span><span class="sxs-lookup"><span data-stu-id="7b0da-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="7b0da-110">Уникальный идентификатор пера планшета.</span><span class="sxs-lookup"><span data-stu-id="7b0da-110">Unique identifier of the tablet stylus.</span></span>

</dd> <dt>

<span data-ttu-id="7b0da-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="7b0da-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7b0da-112">Окно, в которое переместился курсор.</span><span class="sxs-lookup"><span data-stu-id="7b0da-112">The window over which the cursor moved.</span></span>

</dd> <dt>

<span data-ttu-id="7b0da-113">*кспос*</span><span class="sxs-lookup"><span data-stu-id="7b0da-113">*xPos*</span></span> 
</dt> <dd>

<span data-ttu-id="7b0da-114">Координата X пера.</span><span class="sxs-lookup"><span data-stu-id="7b0da-114">The X position of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="7b0da-115">*ипос*</span><span class="sxs-lookup"><span data-stu-id="7b0da-115">*yPos*</span></span> 
</dt> <dd>

<span data-ttu-id="7b0da-116">Координата Y пера.</span><span class="sxs-lookup"><span data-stu-id="7b0da-116">The Y position of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b0da-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b0da-117">Return value</span></span>

<span data-ttu-id="7b0da-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7b0da-118">This method can return one of these values.</span></span>



| <span data-ttu-id="7b0da-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7b0da-119">Return code</span></span>                                                                            | <span data-ttu-id="7b0da-120">Описание</span><span class="sxs-lookup"><span data-stu-id="7b0da-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7b0da-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7b0da-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7b0da-122">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7b0da-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7b0da-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="7b0da-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7b0da-124">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7b0da-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7b0da-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7b0da-125">Requirements</span></span>



| <span data-ttu-id="7b0da-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7b0da-126">Requirement</span></span> | <span data-ttu-id="7b0da-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7b0da-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0da-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b0da-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7b0da-129">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b0da-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7b0da-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b0da-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7b0da-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7b0da-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7b0da-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7b0da-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b0da-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b0da-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0da-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b0da-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0da-135">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="7b0da-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




