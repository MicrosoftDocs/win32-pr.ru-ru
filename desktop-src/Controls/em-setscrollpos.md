---
title: Сообщение EM_SETSCROLLPOS (RichEdit. h)
description: Прокручивает содержимое элемента управления Rich Edit до указанной точки.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- Элементы управления Windows для EM_SETSCROLLPOS сообщений
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492450"
---
# <a name="em_setscrollpos-message"></a><span data-ttu-id="650b2-104">\_Сообщение СЕТСКРОЛЛПОС EM</span><span class="sxs-lookup"><span data-stu-id="650b2-104">EM\_SETSCROLLPOS message</span></span>

<span data-ttu-id="650b2-105">Прокручивает содержимое элемента управления Rich Edit до указанной точки.</span><span class="sxs-lookup"><span data-stu-id="650b2-105">Scrolls the contents of a rich edit control to the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="650b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="650b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="650b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="650b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="650b2-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="650b2-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="650b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="650b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="650b2-110">Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , указывающую точку в виртуальном текстовом пространстве документа, выраженную в пикселях.</span><span class="sxs-lookup"><span data-stu-id="650b2-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure which specifies a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="650b2-111">Документ будет прокручиваться до тех пор, пока эта точка не будет расположена в левом верхнем углу окна редактирования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="650b2-111">The document will be scrolled until this point is located in the upper-left corner of the edit control window.</span></span> <span data-ttu-id="650b2-112">Если необходимо изменить представление так, чтобы левый верхний угол представления был не больше двух строк, а затем один символ из левого края.</span><span class="sxs-lookup"><span data-stu-id="650b2-112">If you want to change the view such that the upper left corner of the view is two lines down and one character in from the left edge.</span></span> <span data-ttu-id="650b2-113">Необходимо передать точку (7, 22).</span><span class="sxs-lookup"><span data-stu-id="650b2-113">You would pass a point of (7, 22).</span></span>

<span data-ttu-id="650b2-114">Форматируемый элемент управления "поле ввода" проверяет координаты x и y и корректирует их при необходимости, чтобы в верхней части отображалась полная строка.</span><span class="sxs-lookup"><span data-stu-id="650b2-114">The rich edit control checks the x and y coordinates and adjusts them if necessary, so that a complete line is displayed at the top.</span></span> <span data-ttu-id="650b2-115">Это также гарантирует, что текст не будет полностью прокручиваться за пределы прямоугольника представления.</span><span class="sxs-lookup"><span data-stu-id="650b2-115">It also ensures that the text is never completely scrolled off the view rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="650b2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="650b2-116">Return value</span></span>

<span data-ttu-id="650b2-117">Это сообщение всегда возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="650b2-117">This message always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="650b2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="650b2-118">Requirements</span></span>



| <span data-ttu-id="650b2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="650b2-119">Requirement</span></span> | <span data-ttu-id="650b2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="650b2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="650b2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="650b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="650b2-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="650b2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="650b2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="650b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="650b2-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="650b2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="650b2-125">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="650b2-125">Redistributable</span></span><br/>          | <span data-ttu-id="650b2-126">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="650b2-126">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="650b2-127">Header</span><span class="sxs-lookup"><span data-stu-id="650b2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="650b2-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="650b2-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="650b2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="650b2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650b2-130">**EM \_ жетскроллпос**</span><span class="sxs-lookup"><span data-stu-id="650b2-130">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> </dl>

 

