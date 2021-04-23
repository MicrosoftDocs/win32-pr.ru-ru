---
title: Сообщение TB_MAPACCELERATOR (Коммктрл. h)
description: Определяет идентификатор кнопки, соответствующей указанному символу ускорителя.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- Элементы управления Windows для TB_MAPACCELERATOR сообщений
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803143"
---
# <a name="tb_mapaccelerator-message"></a><span data-ttu-id="e1ffd-104">\_Сообщение МАПАКЦЕЛЕРАТОР ТБ</span><span class="sxs-lookup"><span data-stu-id="e1ffd-104">TB\_MAPACCELERATOR message</span></span>

<span data-ttu-id="e1ffd-105">Определяет идентификатор кнопки, соответствующей указанному символу ускорителя.</span><span class="sxs-lookup"><span data-stu-id="e1ffd-105">Determines the ID of the button that corresponds to the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1ffd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ffd-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1ffd-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ffd-108">Символ ускорителя.</span><span class="sxs-lookup"><span data-stu-id="e1ffd-108">The accelerator character.</span></span>

</dd> <dt>

<span data-ttu-id="e1ffd-109">*lParam* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e1ffd-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ffd-110">Указатель на **uint**.</span><span class="sxs-lookup"><span data-stu-id="e1ffd-110">Pointer to a **UINT**.</span></span> <span data-ttu-id="e1ffd-111">При возвращении в случае успеха этот параметр будет содержать идентификатор кнопки, имеющей *wParam* в качестве символа ускорителя.</span><span class="sxs-lookup"><span data-stu-id="e1ffd-111">On return, if successful, this parameter will hold the id of the button that has *wParam* as its accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1ffd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1ffd-112">Return value</span></span>

<span data-ttu-id="e1ffd-113">Функция возвращает ненулевое значение, если одна из кнопок имеет параметр *wParam* в качестве символа ускорителя, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e1ffd-113">Returns a nonzero value if one of the buttons has *wParam* as its accelerator character, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ffd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e1ffd-114">Requirements</span></span>



| <span data-ttu-id="e1ffd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e1ffd-115">Requirement</span></span> | <span data-ttu-id="e1ffd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e1ffd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ffd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1ffd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ffd-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1ffd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1ffd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1ffd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ffd-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1ffd-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1ffd-121">Header</span><span class="sxs-lookup"><span data-stu-id="e1ffd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1ffd-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ffd-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e1ffd-123">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="e1ffd-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e1ffd-124">**ТБ \_ МАПАКЦЕЛЕРАТОРВ** (Юникод) и **ТБ \_ мапакцелератора** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e1ffd-124">**TB\_MAPACCELERATORW** (Unicode) and **TB\_MAPACCELERATORA** (ANSI)</span></span><br/>       |



 

 





