---
title: Сообщение RB_GETBANDINFO (Коммктрл. h)
description: Извлекает сведения о заданной полосе в элементе управления "Главная панель".
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- Элементы управления Windows для RB_GETBANDINFO сообщений
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136639"
---
# <a name="rb_getbandinfo-message"></a><span data-ttu-id="f418c-104">\_Сообщение ЖЕТБАНДИНФО RB</span><span class="sxs-lookup"><span data-stu-id="f418c-104">RB\_GETBANDINFO message</span></span>

<span data-ttu-id="f418c-105">Извлекает сведения о заданной полосе в элементе управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="f418c-105">Retrieves information about a specified band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f418c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f418c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f418c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f418c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f418c-108">Отсчитываемый от нуля индекс диапазона, для которого будут извлечены сведения.</span><span class="sxs-lookup"><span data-stu-id="f418c-108">Zero-based index of the band for which the information will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f418c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f418c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f418c-110">Указатель на структуру [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) , которая будет принимать запрошенные сведения о полосе.</span><span class="sxs-lookup"><span data-stu-id="f418c-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that will receive the requested band information.</span></span> <span data-ttu-id="f418c-111">Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры размер структуры **ребарбандинфо** и установить элемент **фмаск** в качестве элементов, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f418c-111">Before sending this message, you must set the **cbSize** member of this structure to the size of the **REBARBANDINFO** structure and set the **fMask** member to the items you want to retrieve.</span></span> <span data-ttu-id="f418c-112">Кроме того, необходимо задать для элемента **Кч** структуры **Ребарбандинфо** размер буфера **лптекст** , если \_ задан рббим Text.</span><span class="sxs-lookup"><span data-stu-id="f418c-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f418c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f418c-113">Return value</span></span>

<span data-ttu-id="f418c-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f418c-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f418c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f418c-115">Requirements</span></span>



| <span data-ttu-id="f418c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f418c-116">Requirement</span></span> | <span data-ttu-id="f418c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f418c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f418c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f418c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f418c-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f418c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f418c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f418c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f418c-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f418c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f418c-122">Header</span><span class="sxs-lookup"><span data-stu-id="f418c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f418c-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f418c-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f418c-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f418c-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f418c-125">**RB \_ ЖЕТБАНДИНФОВ** (Юникод) и **RB \_ жетбандинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f418c-125">**RB\_GETBANDINFOW** (Unicode) and **RB\_GETBANDINFOA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f418c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f418c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f418c-127">**\_СЕТБАНДИНФО RB**</span><span class="sxs-lookup"><span data-stu-id="f418c-127">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





