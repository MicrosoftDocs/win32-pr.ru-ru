---
title: Сообщение TB_SETBITMAPSIZE (Коммктрл. h)
description: Задает размер растровых изображений, добавляемых на панель инструментов.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- Элементы управления Windows для TB_SETBITMAPSIZE сообщений
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489030"
---
# <a name="tb_setbitmapsize-message"></a><span data-ttu-id="ae216-104">\_Сообщение СЕТБИТМАПСИЗЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="ae216-104">TB\_SETBITMAPSIZE message</span></span>

<span data-ttu-id="ae216-105">Задает размер растровых изображений, добавляемых на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="ae216-105">Sets the size of the bitmapped images to be added to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae216-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae216-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae216-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae216-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae216-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ae216-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ae216-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae216-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae216-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает ширину (в пикселях) растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="ae216-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the bitmapped images.</span></span> <span data-ttu-id="ae216-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает высоту растровых изображений в пикселях.</span><span class="sxs-lookup"><span data-stu-id="ae216-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the bitmapped images.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae216-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae216-112">Return value</span></span>

<span data-ttu-id="ae216-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ae216-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae216-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae216-114">Remarks</span></span>

<span data-ttu-id="ae216-115">Размер можно задать только перед добавлением точечных рисунков на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="ae216-115">The size can be set only before adding any bitmaps to the toolbar.</span></span> <span data-ttu-id="ae216-116">Если в приложении явно не задан размер точечного рисунка, размер по умолчанию равен 16 x 15 пикселей.</span><span class="sxs-lookup"><span data-stu-id="ae216-116">If an application does not explicitly set the bitmap size, the size defaults to 16 by 15 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae216-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ae216-117">Requirements</span></span>



| <span data-ttu-id="ae216-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ae216-118">Requirement</span></span> | <span data-ttu-id="ae216-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ae216-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae216-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae216-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae216-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae216-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae216-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae216-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae216-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae216-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae216-124">Header</span><span class="sxs-lookup"><span data-stu-id="ae216-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae216-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae216-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

