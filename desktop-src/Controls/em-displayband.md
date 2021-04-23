---
title: Сообщение EM_DISPLAYBAND (RichEdit. h)
description: Отображает часть содержимого элемента управления Rich Edit, как было ранее отформатировано для устройства с помощью \_ сообщения EM форматранже.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- Элементы управления Windows для EM_DISPLAYBAND сообщений
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988914"
---
# <a name="em_displayband-message"></a><span data-ttu-id="5ddac-104">\_Сообщение ДИСПЛАЙБАНД EM</span><span class="sxs-lookup"><span data-stu-id="5ddac-104">EM\_DISPLAYBAND message</span></span>

<span data-ttu-id="5ddac-105">Отображает часть содержимого элемента управления Rich Edit, как было ранее отформатировано для устройства с помощью сообщения [**EM \_ форматранже**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="5ddac-105">Displays a portion of the contents of a rich edit control, as previously formatted for a device using the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ddac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ddac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ddac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ddac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddac-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5ddac-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5ddac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ddac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddac-110">Структура [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающая область дисплея устройства.</span><span class="sxs-lookup"><span data-stu-id="5ddac-110">A [**RECT**](/previous-versions//dd162897(v=vs.85)) structure specifying the display area of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ddac-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ddac-111">Return value</span></span>

<span data-ttu-id="5ddac-112">Если операция выполнена удачно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="5ddac-112">If the operation succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="5ddac-113">Если операция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="5ddac-113">If the operation fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ddac-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ddac-114">Remarks</span></span>

<span data-ttu-id="5ddac-115">Объекты текстовых и компонентных объектов модели (COM) обрезаются прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="5ddac-115">Text and Component Object Model (COM) objects are clipped by the rectangle.</span></span> <span data-ttu-id="5ddac-116">Приложению не нужно задавать область отсечения.</span><span class="sxs-lookup"><span data-stu-id="5ddac-116">The application does not need to set the clipping region.</span></span>

<span data-ttu-id="5ddac-117">Чередование — это процесс, с помощью которого одна страница выходных данных создается с использованием одного или нескольких отдельных прямоугольников или делений.</span><span class="sxs-lookup"><span data-stu-id="5ddac-117">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="5ddac-118">Когда на странице помещаются все полосы, происходит полное изображение.</span><span class="sxs-lookup"><span data-stu-id="5ddac-118">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="5ddac-119">Этот подход часто используется для растровых принтеров, которые не имеют достаточного объема памяти или могут одновременно создавать изображения на полной странице.</span><span class="sxs-lookup"><span data-stu-id="5ddac-119">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span> <span data-ttu-id="5ddac-120">К устройствам с чередованием относятся большинство матричных принтеров, а также некоторые лазерные принтеры.</span><span class="sxs-lookup"><span data-stu-id="5ddac-120">Banding devices include most dot matrix printers as well as some laser printers.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ddac-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5ddac-121">Requirements</span></span>



| <span data-ttu-id="5ddac-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5ddac-122">Requirement</span></span> | <span data-ttu-id="5ddac-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5ddac-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ddac-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ddac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5ddac-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ddac-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ddac-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ddac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5ddac-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5ddac-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ddac-128">Header</span><span class="sxs-lookup"><span data-stu-id="5ddac-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ddac-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ddac-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ddac-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ddac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddac-131">Печать элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="5ddac-131">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

