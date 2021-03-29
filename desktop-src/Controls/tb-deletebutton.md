---
title: Сообщение TB_DELETEBUTTON (Коммктрл. h)
description: Удаляет кнопку с панели инструментов.
ms.assetid: 6ba569f0-c400-4c0d-bc9f-3a82bcef0360
keywords:
- Элементы управления Windows для TB_DELETEBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_DELETEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d9bbbca143351f70005990b5ac97fa4fa35cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989438"
---
# <a name="tb_deletebutton-message"></a><span data-ttu-id="37564-104">\_Сообщение ДЕЛЕТЕБУТТОН ТБ</span><span class="sxs-lookup"><span data-stu-id="37564-104">TB\_DELETEBUTTON message</span></span>

<span data-ttu-id="37564-105">Удаляет кнопку с панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="37564-105">Deletes a button from the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="37564-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37564-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37564-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37564-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37564-108">Отсчитываемый от нуля индекс удаляемой кнопки.</span><span class="sxs-lookup"><span data-stu-id="37564-108">Zero-based index of the button to delete.</span></span>

</dd> <dt>

<span data-ttu-id="37564-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37564-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="37564-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="37564-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37564-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37564-111">Return value</span></span>

<span data-ttu-id="37564-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="37564-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="37564-113">Требования</span><span class="sxs-lookup"><span data-stu-id="37564-113">Requirements</span></span>



| <span data-ttu-id="37564-114">Требование</span><span class="sxs-lookup"><span data-stu-id="37564-114">Requirement</span></span> | <span data-ttu-id="37564-115">Значение</span><span class="sxs-lookup"><span data-stu-id="37564-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37564-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37564-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37564-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37564-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37564-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37564-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37564-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37564-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37564-120">Header</span><span class="sxs-lookup"><span data-stu-id="37564-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="37564-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="37564-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





