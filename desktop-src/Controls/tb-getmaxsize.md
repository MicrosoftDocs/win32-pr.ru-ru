---
title: Сообщение TB_GETMAXSIZE (Коммктрл. h)
description: Возвращает общий размер всех видимых кнопок и разделителей на панели инструментов.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- Элементы управления Windows для TB_GETMAXSIZE сообщений
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4829e65d90c04181369dd73b9c54634f1077144
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654601"
---
# <a name="tb_getmaxsize-message"></a><span data-ttu-id="3f024-104">\_Сообщение ЖЕТМАКССИЗЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="3f024-104">TB\_GETMAXSIZE message</span></span>

<span data-ttu-id="3f024-105">Возвращает общий размер всех видимых кнопок и разделителей на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="3f024-105">Retrieves the total size of all of the visible buttons and separators in the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f024-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f024-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f024-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f024-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3f024-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3f024-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3f024-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f024-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f024-110">Указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) , которая получает размер элементов.</span><span class="sxs-lookup"><span data-stu-id="3f024-110">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the size of the items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f024-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f024-111">Return value</span></span>

<span data-ttu-id="3f024-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3f024-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f024-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3f024-113">Requirements</span></span>



| <span data-ttu-id="3f024-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3f024-114">Requirement</span></span> | <span data-ttu-id="3f024-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3f024-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f024-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f024-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3f024-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f024-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f024-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f024-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3f024-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3f024-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f024-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f024-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f024-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f024-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

