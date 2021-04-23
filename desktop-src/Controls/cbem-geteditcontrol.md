---
title: Сообщение CBEM_GETEDITCONTROL (Коммктрл. h)
description: Возвращает маркер для элемента управления "поле ввода" элемента управления ComboBoxEx. Элемент управления ComboBoxEx использует поле ввода, если для него задан \_ стиль раскрывающегося списка CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- Элементы управления Windows для CBEM_GETEDITCONTROL сообщений
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137178"
---
# <a name="cbem_geteditcontrol-message"></a><span data-ttu-id="8b4e2-105">\_Сообщение кбем жетедитконтрол</span><span class="sxs-lookup"><span data-stu-id="8b4e2-105">CBEM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="8b4e2-106">Возвращает маркер для элемента управления "поле ввода" элемента управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="8b4e2-106">Gets the handle to the edit control portion of a ComboBoxEx control.</span></span> <span data-ttu-id="8b4e2-107">Элемент управления ComboBoxEx использует поле ввода, если для него задан стиль [**\_ раскрывающегося списка CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8b4e2-107">A ComboBoxEx control uses an edit box when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b4e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b4e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b4e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b4e2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8b4e2-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8b4e2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8b4e2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b4e2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8b4e2-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8b4e2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b4e2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b4e2-113">Return value</span></span>

<span data-ttu-id="8b4e2-114">Возвращает маркер элемента управления "поле ввода" в элементе управления ComboBoxEx, если он использует стиль [**\_ раскрывающегося списка CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8b4e2-114">Returns the handle to the edit control within the ComboBoxEx control if it uses the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="8b4e2-115">В противном случае сообщение возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8b4e2-115">Otherwise, the message returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b4e2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8b4e2-116">Requirements</span></span>



| <span data-ttu-id="8b4e2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8b4e2-117">Requirement</span></span> | <span data-ttu-id="8b4e2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8b4e2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4e2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b4e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8b4e2-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b4e2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b4e2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b4e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8b4e2-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b4e2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b4e2-123">Header</span><span class="sxs-lookup"><span data-stu-id="8b4e2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b4e2-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b4e2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





