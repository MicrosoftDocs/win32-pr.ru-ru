---
title: Сообщение TB_SETMAXTEXTROWS (Коммктрл. h)
description: Задает максимальное число строк текста, отображаемых на кнопке панели инструментов.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- Элементы управления Windows для TB_SETMAXTEXTROWS сообщений
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988373"
---
# <a name="tb_setmaxtextrows-message"></a><span data-ttu-id="9004f-104">\_Сообщение СЕТМАКСТЕКСТРОВС ТБ</span><span class="sxs-lookup"><span data-stu-id="9004f-104">TB\_SETMAXTEXTROWS message</span></span>

<span data-ttu-id="9004f-105">Задает максимальное число строк текста, отображаемых на кнопке панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9004f-105">Sets the maximum number of text rows displayed on a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="9004f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9004f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9004f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9004f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9004f-108">Максимальное количество строк текста, которое может быть отображено.</span><span class="sxs-lookup"><span data-stu-id="9004f-108">Maximum number of rows of text that can be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="9004f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9004f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9004f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9004f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9004f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9004f-111">Return value</span></span>

<span data-ttu-id="9004f-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9004f-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9004f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9004f-113">Remarks</span></span>

<span data-ttu-id="9004f-114">Чтобы переносить текст, необходимо задать максимальную ширину кнопки, отправив [**ТБ \_ сетбуттонвидс**](tb-setbuttonwidth.md) сообщение.</span><span class="sxs-lookup"><span data-stu-id="9004f-114">To cause text to wrap, you must set the maximum button width by sending a [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) message.</span></span> <span data-ttu-id="9004f-115">Текст переносится при разрыве слова; разрывы строк (" \\ n") в тексте не учитываются.</span><span class="sxs-lookup"><span data-stu-id="9004f-115">The text wraps at a word break; line breaks ("\\n") in the text are ignored.</span></span> <span data-ttu-id="9004f-116">Текст в \_ панелях инструментов списка тбстиле всегда отображается в одной строке.</span><span class="sxs-lookup"><span data-stu-id="9004f-116">Text in TBSTYLE\_LIST toolbars is always shown on a single line.</span></span>

## <a name="requirements"></a><span data-ttu-id="9004f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9004f-117">Requirements</span></span>



| <span data-ttu-id="9004f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9004f-118">Requirement</span></span> | <span data-ttu-id="9004f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9004f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9004f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9004f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9004f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9004f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9004f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9004f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9004f-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9004f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9004f-124">Header</span><span class="sxs-lookup"><span data-stu-id="9004f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9004f-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9004f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





