---
title: Сообщение UDM_SETBASE (Коммктрл. h)
description: Задает основание системы счисления для элемента управления "вверх/вниз". Базовое значение определяет, будут ли в окне собеседника отображаться числа в десятичных или шестнадцатеричных цифрах. Шестнадцатеричные числа всегда являются беззнаковыми, а десятичные числа подписываются.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- Элементы управления Windows для UDM_SETBASE сообщений
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988979"
---
# <a name="udm_setbase-message"></a><span data-ttu-id="d2d1b-106">\_Сообщение СЕТБАСЕ UDM</span><span class="sxs-lookup"><span data-stu-id="d2d1b-106">UDM\_SETBASE message</span></span>

<span data-ttu-id="d2d1b-107">Задает основание системы счисления для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="d2d1b-107">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="d2d1b-108">Базовое значение определяет, будут ли в окне собеседника отображаться числа в десятичных или шестнадцатеричных цифрах.</span><span class="sxs-lookup"><span data-stu-id="d2d1b-108">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="d2d1b-109">Шестнадцатеричные числа всегда являются беззнаковыми, а десятичные числа подписываются.</span><span class="sxs-lookup"><span data-stu-id="d2d1b-109">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2d1b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2d1b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d1b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2d1b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2d1b-112">Новое базовое значение для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d2d1b-112">New base value for the control.</span></span> <span data-ttu-id="d2d1b-113">Этот параметр может быть равен 10 для десятичного или 16 в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="d2d1b-113">This parameter can be 10 for decimal or 16 for hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="d2d1b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2d1b-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2d1b-115">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d2d1b-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d1b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2d1b-116">Return value</span></span>

<span data-ttu-id="d2d1b-117">Возвращаемое значение является предыдущим базовым значением.</span><span class="sxs-lookup"><span data-stu-id="d2d1b-117">The return value is the previous base value.</span></span> <span data-ttu-id="d2d1b-118">Если задана недопустимая база данных, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d2d1b-118">If an invalid base is given, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d1b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d2d1b-119">Requirements</span></span>



| <span data-ttu-id="d2d1b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d2d1b-120">Requirement</span></span> | <span data-ttu-id="d2d1b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d2d1b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d1b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2d1b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d1b-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2d1b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2d1b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2d1b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d1b-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2d1b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2d1b-126">Header</span><span class="sxs-lookup"><span data-stu-id="d2d1b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2d1b-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d1b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





