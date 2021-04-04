---
title: Сообщение PBM_SETMARQUEE (Коммктрл. h)
description: Задает индикатор выполнения в режиме бегущей строки. Это приводит к тому, что индикатор выполнения перемещается как бегущая строка.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- Элементы управления Windows для PBM_SETMARQUEE сообщений
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988998"
---
# <a name="pbm_setmarquee-message"></a><span data-ttu-id="26567-105">\_Сообщение СЕТМАРКУИ PBM</span><span class="sxs-lookup"><span data-stu-id="26567-105">PBM\_SETMARQUEE message</span></span>

<span data-ttu-id="26567-106">Задает индикатор выполнения в режиме бегущей строки.</span><span class="sxs-lookup"><span data-stu-id="26567-106">Sets the progress bar to marquee mode.</span></span> <span data-ttu-id="26567-107">Это приводит к тому, что индикатор выполнения перемещается как бегущая строка.</span><span class="sxs-lookup"><span data-stu-id="26567-107">This causes the progress bar to move like a marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="26567-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="26567-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26567-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26567-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26567-110">Указывает, следует ли включать или отключать режим бегущей строки.</span><span class="sxs-lookup"><span data-stu-id="26567-110">Indicates whether to turn the marquee mode on or off.</span></span>

</dd> <dt>

<span data-ttu-id="26567-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26567-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="26567-112">Время в миллисекундах между обновлениями анимации с областью.</span><span class="sxs-lookup"><span data-stu-id="26567-112">Time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="26567-113">Если этот параметр равен нулю, то анимация бегущей строки обновляется каждые 30 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="26567-113">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26567-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26567-114">Return value</span></span>

<span data-ttu-id="26567-115">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="26567-115">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="26567-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26567-116">Remarks</span></span>

<span data-ttu-id="26567-117">Используйте это сообщение, если вы не узнаете о ходе выполнения в сторону завершения, но хотите указать, что выполняется выполнение.</span><span class="sxs-lookup"><span data-stu-id="26567-117">Use this message when you do not know the amount of progress toward completion but wish to indicate that progress is being made.</span></span>

<span data-ttu-id="26567-118">Отправка сообщения **\_ сетмаркуи PBM** для запуска или завершения анимации.</span><span class="sxs-lookup"><span data-stu-id="26567-118">Send the **PBM\_SETMARQUEE** message to start or stop the animation.</span></span>

> [!Note]  
> <span data-ttu-id="26567-119">Прежде чем пытаться запустить анимацию, необходимо задать стиль элемента управления в [**PBS \_ область**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="26567-119">You must set the control style to [**PBS\_MARQUEE**](progress-bar-control-styles.md) before attempting to start the animation.</span></span>

 

> [!Note]  
> <span data-ttu-id="26567-120">Для этого сообщения требуется ComCtl32.dll версии 6,00 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="26567-120">This message requires ComCtl32.dll version 6.00 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26567-121">Требования</span><span class="sxs-lookup"><span data-stu-id="26567-121">Requirements</span></span>



| <span data-ttu-id="26567-122">Требование</span><span class="sxs-lookup"><span data-stu-id="26567-122">Requirement</span></span> | <span data-ttu-id="26567-123">Значение</span><span class="sxs-lookup"><span data-stu-id="26567-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26567-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26567-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26567-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26567-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26567-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26567-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26567-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26567-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26567-128">Header</span><span class="sxs-lookup"><span data-stu-id="26567-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="26567-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="26567-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





