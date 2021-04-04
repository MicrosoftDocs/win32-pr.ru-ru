---
title: Сообщение TB_GETBITMAPFLAGS (Коммктрл. h)
description: Получает флаги, описывающие тип используемого точечного рисунка.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- Элементы управления Windows для TB_GETBITMAPFLAGS сообщений
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137847"
---
# <a name="tb_getbitmapflags-message"></a><span data-ttu-id="73eae-104">\_Сообщение ЖЕТБИТМАПФЛАГС ТБ</span><span class="sxs-lookup"><span data-stu-id="73eae-104">TB\_GETBITMAPFLAGS message</span></span>

<span data-ttu-id="73eae-105">Получает флаги, описывающие тип используемого точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="73eae-105">Retrieves the flags that describe the type of bitmap to be used.</span></span>

## <a name="parameters"></a><span data-ttu-id="73eae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73eae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73eae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73eae-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="73eae-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="73eae-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="73eae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73eae-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="73eae-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="73eae-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73eae-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73eae-111">Return value</span></span>

<span data-ttu-id="73eae-112">Возвращает значение типа **DWORD** , описывающее тип точечного рисунка, который следует использовать.</span><span class="sxs-lookup"><span data-stu-id="73eae-112">Returns a **DWORD** value that describes the type of bitmap that should be used.</span></span> <span data-ttu-id="73eae-113">Если для этого возвращаемого значения установлен \_ большой флаг ТББФ, приложения должны использовать крупные точечные рисунки (24 x 24); в противном случае приложения должны использовать небольшие точечные рисунки (16 x 16).</span><span class="sxs-lookup"><span data-stu-id="73eae-113">If this return value has the TBBF\_LARGE flag set, applications should use large bitmaps (24 x 24); otherwise, applications should use small bitmaps (16 x 16).</span></span> <span data-ttu-id="73eae-114">Все остальные биты зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="73eae-114">All other bits are reserved.</span></span>

## <a name="remarks"></a><span data-ttu-id="73eae-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73eae-115">Remarks</span></span>

<span data-ttu-id="73eae-116">Значение, возвращаемое **ТБ \_ жетбитмапфлагс** , — это только рекомендации.</span><span class="sxs-lookup"><span data-stu-id="73eae-116">The value returned by **TB\_GETBITMAPFLAGS** is only advisory.</span></span> <span data-ttu-id="73eae-117">Элемент управления ToolBar рекомендует крупные или небольшие растровые изображения в зависимости от того, выбраны ли для пользователя крупные или малые шрифты.</span><span class="sxs-lookup"><span data-stu-id="73eae-117">The toolbar control recommends large or small bitmaps based upon whether the user has chosen large or small fonts.</span></span>

## <a name="requirements"></a><span data-ttu-id="73eae-118">Требования</span><span class="sxs-lookup"><span data-stu-id="73eae-118">Requirements</span></span>



| <span data-ttu-id="73eae-119">Требование</span><span class="sxs-lookup"><span data-stu-id="73eae-119">Requirement</span></span> | <span data-ttu-id="73eae-120">Значение</span><span class="sxs-lookup"><span data-stu-id="73eae-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73eae-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73eae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="73eae-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73eae-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73eae-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73eae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="73eae-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73eae-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73eae-125">Header</span><span class="sxs-lookup"><span data-stu-id="73eae-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="73eae-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="73eae-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





