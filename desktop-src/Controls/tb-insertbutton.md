---
title: Сообщение TB_INSERTBUTTON (Коммктрл. h)
description: Вставляет кнопку на панель инструментов.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- Элементы управления Windows для TB_INSERTBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135575"
---
# <a name="tb_insertbutton-message"></a><span data-ttu-id="6a69f-104">\_Сообщение ИНСЕРТБУТТОН ТБ</span><span class="sxs-lookup"><span data-stu-id="6a69f-104">TB\_INSERTBUTTON message</span></span>

<span data-ttu-id="6a69f-105">Вставляет кнопку на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="6a69f-105">Inserts a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a69f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a69f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a69f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a69f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a69f-108">Отсчитываемый от нуля индекс кнопки.</span><span class="sxs-lookup"><span data-stu-id="6a69f-108">Zero-based index of a button.</span></span> <span data-ttu-id="6a69f-109">Сообщение вставляет кнопку Создать слева от этой кнопки.</span><span class="sxs-lookup"><span data-stu-id="6a69f-109">The message inserts the new button to the left of this button.</span></span>

</dd> <dt>

<span data-ttu-id="6a69f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a69f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a69f-111">Указатель на структуру [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , содержащую сведения о вставляемой кнопке.</span><span class="sxs-lookup"><span data-stu-id="6a69f-111">Pointer to a [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure containing information about the button to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a69f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a69f-112">Return value</span></span>

<span data-ttu-id="6a69f-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6a69f-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a69f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6a69f-114">Requirements</span></span>



| <span data-ttu-id="6a69f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6a69f-115">Requirement</span></span> | <span data-ttu-id="6a69f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6a69f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a69f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a69f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a69f-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a69f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a69f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a69f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a69f-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a69f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a69f-121">Header</span><span class="sxs-lookup"><span data-stu-id="6a69f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a69f-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a69f-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6a69f-123">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="6a69f-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6a69f-124">**ТБ \_ ИНСЕРТБУТТОНВ** (Юникод) и **ТБ \_ инсертбуттона** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6a69f-124">**TB\_INSERTBUTTONW** (Unicode) and **TB\_INSERTBUTTONA** (ANSI)</span></span><br/>           |



 

 





