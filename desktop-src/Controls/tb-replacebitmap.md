---
title: Сообщение TB_REPLACEBITMAP (Коммктрл. h)
description: Заменяет существующий точечный рисунок новым растровым изображением.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- Элементы управления Windows для TB_REPLACEBITMAP сообщений
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892334"
---
# <a name="tb_replacebitmap-message"></a><span data-ttu-id="0fae1-104">\_Сообщение РЕПЛАЦЕБИТМАП ТБ</span><span class="sxs-lookup"><span data-stu-id="0fae1-104">TB\_REPLACEBITMAP message</span></span>

<span data-ttu-id="0fae1-105">Заменяет существующий точечный рисунок новым растровым изображением.</span><span class="sxs-lookup"><span data-stu-id="0fae1-105">Replaces an existing bitmap with a new bitmap.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fae1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fae1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fae1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fae1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0fae1-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0fae1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0fae1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fae1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fae1-110">Указатель на структуру [**тбреплацебитмап**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) , которая содержит сведения о заменяемом растровом изображении, и новое растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="0fae1-110">Pointer to a [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) structure that contains the information of the bitmap to be replaced and the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fae1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fae1-111">Return value</span></span>

<span data-ttu-id="0fae1-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0fae1-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fae1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0fae1-113">Requirements</span></span>



| <span data-ttu-id="0fae1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0fae1-114">Requirement</span></span> | <span data-ttu-id="0fae1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0fae1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fae1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fae1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0fae1-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fae1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fae1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fae1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0fae1-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0fae1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fae1-120">Header</span><span class="sxs-lookup"><span data-stu-id="0fae1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fae1-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fae1-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





