---
title: Сообщение TB_AUTOSIZE (Коммктрл. h)
description: Приводит к изменению размера панели инструментов.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- Элементы управления Windows для TB_AUTOSIZE сообщений
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535633"
---
# <a name="tb_autosize-message"></a><span data-ttu-id="8cc90-104">Размер \_ сообщения AUTOSIZE для ТБ</span><span class="sxs-lookup"><span data-stu-id="8cc90-104">TB\_AUTOSIZE message</span></span>

<span data-ttu-id="8cc90-105">Приводит к изменению размера панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="8cc90-105">Causes a toolbar to be resized.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cc90-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cc90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8cc90-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8cc90-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8cc90-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8cc90-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cc90-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8cc90-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8cc90-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc90-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cc90-111">Return value</span></span>

<span data-ttu-id="8cc90-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8cc90-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc90-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cc90-113">Remarks</span></span>

<span data-ttu-id="8cc90-114">Приложение отправляет сообщение **\_ AUTOSIZE** по размеру ТБ после изменения размера панели инструментов либо путем установки размера кнопки или растрового изображения, либо путем добавления строк в первый раз.</span><span class="sxs-lookup"><span data-stu-id="8cc90-114">An application sends the **TB\_AUTOSIZE** message after causing the size of a toolbar to change either by setting the button or bitmap size or by adding strings for the first time.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc90-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8cc90-115">Requirements</span></span>



| <span data-ttu-id="8cc90-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8cc90-116">Requirement</span></span> | <span data-ttu-id="8cc90-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8cc90-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc90-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cc90-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc90-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cc90-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cc90-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cc90-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc90-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cc90-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cc90-122">Header</span><span class="sxs-lookup"><span data-stu-id="8cc90-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cc90-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc90-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





