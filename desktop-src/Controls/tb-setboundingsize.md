---
title: Сообщение TB_SETBOUNDINGSIZE (Коммктрл. h)
description: Задает ограничивающий размер для элемента управления панели инструментов с несколькими столбцами.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- Элементы управления Windows для TB_SETBOUNDINGSIZE сообщений
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891409"
---
# <a name="tb_setboundingsize-message"></a><span data-ttu-id="70fe8-104">\_Сообщение СЕТБАУНДИНГСИЗЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="70fe8-104">TB\_SETBOUNDINGSIZE message</span></span>

<span data-ttu-id="70fe8-105">\[Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</span><span class="sxs-lookup"><span data-stu-id="70fe8-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="70fe8-106">Это сообщение может не поддерживаться в будущих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70fe8-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="70fe8-107">Задает ограничивающий размер для элемента управления панели инструментов с несколькими столбцами.</span><span class="sxs-lookup"><span data-stu-id="70fe8-107">Sets the bounding size for a multi-column toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="70fe8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="70fe8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70fe8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70fe8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70fe8-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="70fe8-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="70fe8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70fe8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70fe8-112">Указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) , чей элемент **CY** содержит ограничивающую высоту.</span><span class="sxs-lookup"><span data-stu-id="70fe8-112">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure whose **cy** member contains the bounding height.</span></span> <span data-ttu-id="70fe8-113">Элемент **CX** (ширина) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="70fe8-113">The **cx** member (the width) is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70fe8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70fe8-114">Return value</span></span>

<span data-ttu-id="70fe8-115">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="70fe8-115">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="70fe8-116">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="70fe8-116">Security Considerations</span></span>

<span data-ttu-id="70fe8-117">Использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="70fe8-117">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="70fe8-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70fe8-118">Remarks</span></span>

<span data-ttu-id="70fe8-119">Ограничивающий размер управляет тем, как кнопки организованы в столбцы.</span><span class="sxs-lookup"><span data-stu-id="70fe8-119">The bounding size controls how buttons are organized into columns.</span></span> <span data-ttu-id="70fe8-120">Если элемент управления "панель инструментов" не имеет стиля [**тбстиле \_ ex \_ Column**](toolbar-extended-styles.md) , это сообщение не действует.</span><span class="sxs-lookup"><span data-stu-id="70fe8-120">If the toolbar control does not have the [**TBSTYLE\_EX\_MULTICOLUMN**](toolbar-extended-styles.md) style, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="70fe8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="70fe8-121">Requirements</span></span>



| <span data-ttu-id="70fe8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="70fe8-122">Requirement</span></span> | <span data-ttu-id="70fe8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="70fe8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70fe8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70fe8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="70fe8-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70fe8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70fe8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70fe8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="70fe8-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70fe8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70fe8-128">Header</span><span class="sxs-lookup"><span data-stu-id="70fe8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="70fe8-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="70fe8-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

