---
title: Сообщение TTM_GETCURRENTTOOL (Коммктрл. h)
description: Извлекает сведения о текущем инструменте в элементе управления ToolTip.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- Элементы управления Windows для TTM_GETCURRENTTOOL сообщений
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988677"
---
# <a name="ttm_getcurrenttool-message"></a><span data-ttu-id="209ef-104">\_Сообщение ТТМ жеткурренттул</span><span class="sxs-lookup"><span data-stu-id="209ef-104">TTM\_GETCURRENTTOOL message</span></span>

<span data-ttu-id="209ef-105">Извлекает сведения о текущем инструменте в элементе управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="209ef-105">Retrieves the information for the current tool in a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="209ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="209ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="209ef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="209ef-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="209ef-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="209ef-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="209ef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="209ef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="209ef-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , которая получает сведения о текущем инструменте.</span><span class="sxs-lookup"><span data-stu-id="209ef-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the current tool.</span></span> <span data-ttu-id="209ef-111">Если это значение равно **null**, то возвращаемое значение указывает на существование текущего средства без фактического извлечения сведений об инструменте.</span><span class="sxs-lookup"><span data-stu-id="209ef-111">If this value is **NULL**, the return value indicates the existence of the current tool without actually retrieving the tool information.</span></span> <span data-ttu-id="209ef-112">Если это значение не **равно NULL**, перед отправкой этого сообщения необходимо заполнить элемент **кбсизе** структуры **тулинфо** .</span><span class="sxs-lookup"><span data-stu-id="209ef-112">If this value is not **NULL**, the **cbSize** member of the **TOOLINFO** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="209ef-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="209ef-113">Return value</span></span>

<span data-ttu-id="209ef-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="209ef-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="209ef-115">Если значение *lParam* равно **null**, функция возвращает ненулевой, если текущий инструмент существует, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="209ef-115">If *lParam* is **NULL**, returns nonzero if a current tool exists, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="209ef-116">Требования</span><span class="sxs-lookup"><span data-stu-id="209ef-116">Requirements</span></span>



| <span data-ttu-id="209ef-117">Требование</span><span class="sxs-lookup"><span data-stu-id="209ef-117">Requirement</span></span> | <span data-ttu-id="209ef-118">Значение</span><span class="sxs-lookup"><span data-stu-id="209ef-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="209ef-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="209ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="209ef-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="209ef-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="209ef-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="209ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="209ef-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="209ef-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="209ef-123">Header</span><span class="sxs-lookup"><span data-stu-id="209ef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="209ef-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="209ef-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="209ef-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="209ef-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="209ef-126">**ТТМ \_ ЖЕТКУРРЕНТТУЛВ** (Юникод) и **ТТМ \_ жеткурренттула** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="209ef-126">**TTM\_GETCURRENTTOOLW** (Unicode) and **TTM\_GETCURRENTTOOLA** (ANSI)</span></span><br/>     |



 

 





