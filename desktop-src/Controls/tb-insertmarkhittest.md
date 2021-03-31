---
title: Сообщение TB_INSERTMARKHITTEST (Коммктрл. h)
description: Извлекает данные метки вставки для точки на панели инструментов.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- Элементы управления Windows для TB_INSERTMARKHITTEST сообщений
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071448"
---
# <a name="tb_insertmarkhittest-message"></a><span data-ttu-id="53d79-104">\_Сообщение ИНСЕРТМАРКХИТТЕСТ ТБ</span><span class="sxs-lookup"><span data-stu-id="53d79-104">TB\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="53d79-105">Извлекает данные метки вставки для точки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="53d79-105">Retrieves the insertion mark information for a point in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="53d79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53d79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d79-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53d79-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53d79-108">Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , содержащую координаты проверки попадания относительно клиентской области панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="53d79-108">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the hit test coordinates, relative to the client area of the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="53d79-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53d79-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53d79-110">Указатель на структуру [**тбинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) , которая получает сведения о метке вставки.</span><span class="sxs-lookup"><span data-stu-id="53d79-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53d79-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53d79-111">Return value</span></span>

<span data-ttu-id="53d79-112">Возвращает ненулевое значение, если точка является отметкой вставки, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="53d79-112">Returns nonzero if the point is an insertion mark, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d79-113">Требования</span><span class="sxs-lookup"><span data-stu-id="53d79-113">Requirements</span></span>



| <span data-ttu-id="53d79-114">Требование</span><span class="sxs-lookup"><span data-stu-id="53d79-114">Requirement</span></span> | <span data-ttu-id="53d79-115">Значение</span><span class="sxs-lookup"><span data-stu-id="53d79-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53d79-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53d79-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53d79-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53d79-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53d79-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53d79-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53d79-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53d79-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53d79-120">Header</span><span class="sxs-lookup"><span data-stu-id="53d79-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53d79-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="53d79-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

