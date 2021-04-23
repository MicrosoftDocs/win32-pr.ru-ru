---
title: Сообщение EM_SETEDITSTYLE (RichEdit. h)
description: Задает текущие флаги изменения стиля для элемента управления Rich Edit.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- Элементы управления Windows для EM_SETEDITSTYLE сообщений
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535057"
---
# <a name="em_seteditstyle-message"></a><span data-ttu-id="ea7a6-104">\_Сообщение СЕТЕДИТСТИЛЕ EM</span><span class="sxs-lookup"><span data-stu-id="ea7a6-104">EM\_SETEDITSTYLE message</span></span>

<span data-ttu-id="ea7a6-105">Задает текущие флаги изменения стиля для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-105">Sets the current edit style flags for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea7a6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea7a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea7a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea7a6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea7a6-108">Задает один или несколько флагов редактирования стиля.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-108">Specifies one or more edit style flags.</span></span> <span data-ttu-id="ea7a6-109">Список возможных значений см. в разделе [**EM \_ жетедитстиле**](em-geteditstyle.md).</span><span class="sxs-lookup"><span data-stu-id="ea7a6-109">For a list of possible values, see [**EM\_GETEDITSTYLE**](em-geteditstyle.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea7a6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea7a6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea7a6-111">Маска, состоящая из одного или нескольких значений *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ea7a6-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="ea7a6-112">Будут установлены или сняты только значения, указанные в этой маске.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="ea7a6-113">Это позволяет устанавливать или снимать один флаг без считывания текущих состояний флагов.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea7a6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea7a6-114">Return value</span></span>

<span data-ttu-id="ea7a6-115">Возвращаемое значение является состоянием флагов стиля правки после того, как элемент управления Rich Edit попытается применить изменения стиля редактирования.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-115">The return value is the state of the edit style flags after the rich edit control has attempted to implement your edit style changes.</span></span> <span data-ttu-id="ea7a6-116">Флаги редактирования стиля представляют собой набор флагов, указывающих текущий стиль редактирования.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea7a6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ea7a6-117">Requirements</span></span>



| <span data-ttu-id="ea7a6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ea7a6-118">Requirement</span></span> | <span data-ttu-id="ea7a6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ea7a6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea7a6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea7a6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea7a6-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea7a6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea7a6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea7a6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea7a6-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea7a6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea7a6-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ea7a6-124">Redistributable</span></span><br/>          | <span data-ttu-id="ea7a6-125">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="ea7a6-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="ea7a6-126">Header</span><span class="sxs-lookup"><span data-stu-id="ea7a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea7a6-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea7a6-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea7a6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea7a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea7a6-129">**EM \_ жетедитстиле**</span><span class="sxs-lookup"><span data-stu-id="ea7a6-129">**EM\_GETEDITSTYLE**</span></span>](em-geteditstyle.md)
</dt> </dl>

 

 





