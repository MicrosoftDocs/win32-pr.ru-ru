---
title: Сообщение SB_SIMPLE (Коммктрл. h)
description: Указывает, отображает ли окно состояния простой текст или отображает все фрагменты окна, заданные предыдущим \_ сообщением SB сетпартс.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- Элементы управления Windows для SB_SIMPLE сообщений
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136822"
---
# <a name="sb_simple-message"></a><span data-ttu-id="785bc-104">\_Простое сообщение SB</span><span class="sxs-lookup"><span data-stu-id="785bc-104">SB\_SIMPLE message</span></span>

<span data-ttu-id="785bc-105">Указывает, отображает ли окно состояния простой текст или отображает все фрагменты окна, заданные предыдущим сообщением [**SB \_ сетпартс**](sb-setparts.md) .</span><span class="sxs-lookup"><span data-stu-id="785bc-105">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="785bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="785bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="785bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="785bc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="785bc-108">Флаг отображаемого типа.</span><span class="sxs-lookup"><span data-stu-id="785bc-108">Display type flag.</span></span> <span data-ttu-id="785bc-109">Если этот параметр имеет **значение true**, в окне отображается простой текст.</span><span class="sxs-lookup"><span data-stu-id="785bc-109">If this parameter is **TRUE**, the window displays simple text.</span></span> <span data-ttu-id="785bc-110">Если значение равно **false**, отображается несколько частей.</span><span class="sxs-lookup"><span data-stu-id="785bc-110">If it is **FALSE**, it displays multiple parts.</span></span>

</dd> <dt>

<span data-ttu-id="785bc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="785bc-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="785bc-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="785bc-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="785bc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="785bc-113">Return value</span></span>

<span data-ttu-id="785bc-114">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="785bc-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="785bc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="785bc-115">Remarks</span></span>

<span data-ttu-id="785bc-116">Если окно состояния изменяется с непростого на простой или наоборот, окно немедленно перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="785bc-116">If the status window is being changed from nonsimple to simple, or vice versa, the window is immediately redrawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="785bc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="785bc-117">Requirements</span></span>



| <span data-ttu-id="785bc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="785bc-118">Requirement</span></span> | <span data-ttu-id="785bc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="785bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="785bc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="785bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="785bc-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="785bc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="785bc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="785bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="785bc-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="785bc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="785bc-124">Header</span><span class="sxs-lookup"><span data-stu-id="785bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="785bc-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="785bc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





