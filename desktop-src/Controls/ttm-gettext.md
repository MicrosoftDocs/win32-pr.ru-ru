---
title: Сообщение TTM_GETTEXT (Коммктрл. h)
description: Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- Элементы управления Windows для TTM_GETTEXT сообщений
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654502"
---
# <a name="ttm_gettext-message"></a><span data-ttu-id="bedb5-104">ТТМ \_ SMS</span><span class="sxs-lookup"><span data-stu-id="bedb5-104">TTM\_GETTEXT message</span></span>

<span data-ttu-id="bedb5-105">Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="bedb5-105">Retrieves the information a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="bedb5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bedb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bedb5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bedb5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bedb5-108">Число **тчарс**, включая завершающее **значение NULL**, для копирования в буфер, на который указывает **лпсзтекст**.</span><span class="sxs-lookup"><span data-stu-id="bedb5-108">The number of **TCHARs**, including the terminating **NULL**, to copy to the buffer pointed to by **lpszText**.</span></span> </dd> <dt>

<span data-ttu-id="bedb5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bedb5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bedb5-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="bedb5-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="bedb5-111">Задайте для элемента **кбсизе** этой структуры значение `sizeof(TOOLINFO)` перед отправкой этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="bedb5-111">Set the **cbSize** member of this structure to `sizeof(TOOLINFO)` before sending this message.</span></span> <span data-ttu-id="bedb5-112">Задайте элементы **HWND** и **uId** , чтобы определить средство, для которого требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="bedb5-112">Set the **hwnd** and **uId** members to identify the tool for which to retrieve information.</span></span> <span data-ttu-id="bedb5-113">Выделение буфера размера, указанного параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="bedb5-113">Allocate a buffer of size specified by *wParam*.</span></span> <span data-ttu-id="bedb5-114">Установите элемент **лпсзтекст** , чтобы он указывал на буфер для получения текста инструмента.</span><span class="sxs-lookup"><span data-stu-id="bedb5-114">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bedb5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bedb5-115">Return value</span></span>

<span data-ttu-id="bedb5-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="bedb5-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bedb5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bedb5-117">Requirements</span></span>



| <span data-ttu-id="bedb5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bedb5-118">Requirement</span></span> | <span data-ttu-id="bedb5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bedb5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bedb5-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bedb5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bedb5-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bedb5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bedb5-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bedb5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bedb5-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bedb5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bedb5-124">Header</span><span class="sxs-lookup"><span data-stu-id="bedb5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bedb5-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bedb5-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bedb5-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="bedb5-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bedb5-127">**ТТМ \_ ЖЕТТЕКСТВ** (Юникод) и **ТТМ \_ gettext** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bedb5-127">**TTM\_GETTEXTW** (Unicode) and **TTM\_GETTEXTA** (ANSI)</span></span><br/>                   |



 

 





