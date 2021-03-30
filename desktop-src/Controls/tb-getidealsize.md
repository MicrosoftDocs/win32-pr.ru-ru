---
title: Сообщение TB_GETIDEALSIZE (Коммктрл. h)
description: Получает идеальный размер панели инструментов.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- Элементы управления Windows для TB_GETIDEALSIZE сообщений
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071250"
---
# <a name="tb_getidealsize-message"></a><span data-ttu-id="958f7-104">\_Сообщение ЖЕТИДЕАЛСИЗЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="958f7-104">TB\_GETIDEALSIZE message</span></span>

<span data-ttu-id="958f7-105">Получает идеальный размер панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="958f7-105">Gets the ideal size of the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="958f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="958f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="958f7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="958f7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="958f7-108">**Логическое** значение, указывающее, следует ли получить идеальную высоту или ширину панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="958f7-108">A **BOOL** that indicates whether to retrieve the ideal height or width of the toolbar.</span></span> <span data-ttu-id="958f7-109">Используйте **значение true** для получения идеальной высоты, **false** для получения идеальной ширины.</span><span class="sxs-lookup"><span data-stu-id="958f7-109">Use **TRUE** to retrieve the ideal height, **FALSE** to retrieve the ideal width.</span></span></dd> <dt>

<span data-ttu-id="958f7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="958f7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="958f7-111">Указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) , получающую высоту или ширину, на которой будут отображаться все кнопки.</span><span class="sxs-lookup"><span data-stu-id="958f7-111">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the height or width at which all buttons would be displayed.</span></span> <span data-ttu-id="958f7-112">Если параметр *wParam* имеет **значение true**, допустим только элемент **CY** (Height).</span><span class="sxs-lookup"><span data-stu-id="958f7-112">If *wParam* is **TRUE**, only the **cy** member (height) is valid.</span></span> <span data-ttu-id="958f7-113">Если параметр *wParam* имеет **значение false**, допустим только элемент **CX** (Width).</span><span class="sxs-lookup"><span data-stu-id="958f7-113">If *wParam* is **FALSE**, only the **cx** member (width) is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="958f7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="958f7-114">Return value</span></span>

<span data-ttu-id="958f7-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="958f7-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="958f7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="958f7-116">Requirements</span></span>



| <span data-ttu-id="958f7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="958f7-117">Requirement</span></span> | <span data-ttu-id="958f7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="958f7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="958f7-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="958f7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="958f7-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="958f7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="958f7-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="958f7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="958f7-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="958f7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="958f7-123">Header</span><span class="sxs-lookup"><span data-stu-id="958f7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="958f7-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="958f7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

