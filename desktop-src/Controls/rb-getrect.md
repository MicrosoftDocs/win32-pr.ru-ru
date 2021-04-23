---
title: Сообщение RB_GETRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для заданной полосы в элементе управления "Главная панель".
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- Элементы управления Windows для RB_GETRECT сообщений
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262200"
---
# <a name="rb_getrect-message"></a><span data-ttu-id="9a7df-104">\_Сообщение RB</span><span class="sxs-lookup"><span data-stu-id="9a7df-104">RB\_GETRECT message</span></span>

<span data-ttu-id="9a7df-105">Извлекает ограничивающий прямоугольник для заданной полосы в элементе управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="9a7df-105">Retrieves the bounding rectangle for a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a7df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a7df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a7df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a7df-108">Отсчитываемый от нуля индекс полосы в элементе управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="9a7df-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="9a7df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a7df-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a7df-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать границы полосы-панели.</span><span class="sxs-lookup"><span data-stu-id="9a7df-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounds of the rebar band.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7df-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a7df-111">Return value</span></span>

<span data-ttu-id="9a7df-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9a7df-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7df-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9a7df-113">Requirements</span></span>



| <span data-ttu-id="9a7df-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9a7df-114">Requirement</span></span> | <span data-ttu-id="9a7df-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9a7df-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7df-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a7df-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7df-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a7df-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a7df-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a7df-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7df-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a7df-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a7df-120">Header</span><span class="sxs-lookup"><span data-stu-id="9a7df-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7df-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7df-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

