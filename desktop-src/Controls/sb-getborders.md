---
title: Сообщение SB_GETBORDERS (Коммктрл. h)
description: Извлекает текущие значения ширины горизонтальных и вертикальных границ окна состояния.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- Элементы управления Windows для SB_GETBORDERS сообщений
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136834"
---
# <a name="sb_getborders-message"></a><span data-ttu-id="2a0e0-104">Сообщение SB с \_ ВЫграничными границами</span><span class="sxs-lookup"><span data-stu-id="2a0e0-104">SB\_GETBORDERS message</span></span>

<span data-ttu-id="2a0e0-105">Извлекает текущие значения ширины горизонтальных и вертикальных границ окна состояния.</span><span class="sxs-lookup"><span data-stu-id="2a0e0-105">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a0e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a0e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a0e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a0e0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2a0e0-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2a0e0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2a0e0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a0e0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a0e0-110">Указатель на целочисленный массив с тремя элементами.</span><span class="sxs-lookup"><span data-stu-id="2a0e0-110">Pointer to an integer array that has three elements.</span></span> <span data-ttu-id="2a0e0-111">Первый элемент получает ширину горизонтальной границы, второй получает ширину вертикальной границы, а третья — ширину границы между прямоугольниками.</span><span class="sxs-lookup"><span data-stu-id="2a0e0-111">The first element receives the width of the horizontal border, the second receives the width of the vertical border, and the third receives the width of the border between rectangles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a0e0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a0e0-112">Return value</span></span>

<span data-ttu-id="2a0e0-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2a0e0-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a0e0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a0e0-114">Remarks</span></span>

<span data-ttu-id="2a0e0-115">Границы определяют интервал между внешним краями окна и прямоугольниками в окне, содержащими текст.</span><span class="sxs-lookup"><span data-stu-id="2a0e0-115">The borders determine the spacing between the outside edge of the window and the rectangles within the window that contain text.</span></span> <span data-ttu-id="2a0e0-116">Кроме того, границы определяют интервал между прямоугольниками.</span><span class="sxs-lookup"><span data-stu-id="2a0e0-116">The borders also determine the spacing between rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a0e0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2a0e0-117">Requirements</span></span>



| <span data-ttu-id="2a0e0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2a0e0-118">Requirement</span></span> | <span data-ttu-id="2a0e0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0e0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0e0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a0e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a0e0-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a0e0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a0e0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a0e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a0e0-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a0e0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a0e0-124">Header</span><span class="sxs-lookup"><span data-stu-id="2a0e0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a0e0-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a0e0-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





