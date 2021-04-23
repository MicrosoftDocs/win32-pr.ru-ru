---
title: Сообщение RB_SETBANDINFO (Коммктрл. h)
description: Задает характеристики существующей полосы в элементе управления "Главная панель".
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- Элементы управления Windows для RB_SETBANDINFO сообщений
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491757"
---
# <a name="rb_setbandinfo-message"></a><span data-ttu-id="11a6a-104">\_Сообщение СЕТБАНДИНФО RB</span><span class="sxs-lookup"><span data-stu-id="11a6a-104">RB\_SETBANDINFO message</span></span>

<span data-ttu-id="11a6a-105">Задает характеристики существующей полосы в элементе управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="11a6a-105">Sets characteristics of an existing band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="11a6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11a6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11a6a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11a6a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11a6a-108">Отсчитываемый от нуля индекс диапазона для получения новых параметров.</span><span class="sxs-lookup"><span data-stu-id="11a6a-108">Zero-based index of the band to receive the new settings.</span></span>

</dd> <dt>

<span data-ttu-id="11a6a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11a6a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11a6a-110">Указатель на структуру [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) , определяющую изменяемую полосу и новые параметры.</span><span class="sxs-lookup"><span data-stu-id="11a6a-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be modified and the new settings.</span></span> <span data-ttu-id="11a6a-111">Перед отправкой этого сообщения необходимо присвоить элементу **кбсизе** этой структуры значение структуры **sizeof**(ребарбандинфо).</span><span class="sxs-lookup"><span data-stu-id="11a6a-111">Before sending this message, you must set the **cbSize** member of this structure to the **sizeof**(REBARBANDINFO) structure.</span></span> <span data-ttu-id="11a6a-112">Кроме того, необходимо задать для элемента **Кч** структуры **Ребарбандинфо** размер буфера **лптекст** , если \_ задан рббим Text.</span><span class="sxs-lookup"><span data-stu-id="11a6a-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11a6a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11a6a-113">Return value</span></span>

<span data-ttu-id="11a6a-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="11a6a-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="11a6a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="11a6a-115">Requirements</span></span>



| <span data-ttu-id="11a6a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="11a6a-116">Requirement</span></span> | <span data-ttu-id="11a6a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="11a6a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11a6a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11a6a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11a6a-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11a6a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11a6a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11a6a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11a6a-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="11a6a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11a6a-122">Header</span><span class="sxs-lookup"><span data-stu-id="11a6a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11a6a-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="11a6a-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="11a6a-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="11a6a-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="11a6a-125">**RB \_ СЕТБАНДИНФОВ** (Юникод) и **RB \_ сетбандинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="11a6a-125">**RB\_SETBANDINFOW** (Unicode) and **RB\_SETBANDINFOA** (ANSI)</span></span><br/>             |



 

 





