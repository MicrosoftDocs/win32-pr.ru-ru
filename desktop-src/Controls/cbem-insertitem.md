---
title: Сообщение CBEM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- Элементы управления Windows для CBEM_INSERTITEM сообщений
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654707"
---
# <a name="cbem_insertitem-message"></a><span data-ttu-id="f6a77-104">\_Сообщение кбем INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="f6a77-104">CBEM\_INSERTITEM message</span></span>

<span data-ttu-id="f6a77-105">Вставляет новый элемент в элемент управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="f6a77-105">Inserts a new item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6a77-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6a77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6a77-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f6a77-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f6a77-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f6a77-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6a77-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6a77-110">Указатель на структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , содержащую сведения о вставляемом элементе.</span><span class="sxs-lookup"><span data-stu-id="f6a77-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains information about the item to be inserted.</span></span> <span data-ttu-id="f6a77-111">При отправке сообщения элемент **Член iItem** должен быть установлен в значение, указывающее на Отсчитываемый от нуля индекс, по которому нужно вставить элемент.</span><span class="sxs-lookup"><span data-stu-id="f6a77-111">When the message is sent, the **iItem** member must be set to indicate the zero-based index at which to insert the item.</span></span> <span data-ttu-id="f6a77-112">Чтобы вставить элемент в конец списка, установите для элемента **Член iItem** значение-1.</span><span class="sxs-lookup"><span data-stu-id="f6a77-112">To insert an item at the end of the list, set the **iItem** member to -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a77-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6a77-113">Return value</span></span>

<span data-ttu-id="f6a77-114">Возвращает индекс, по которому новый элемент был вставлен в случае успеха, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f6a77-114">Returns the index at which the new item was inserted if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a77-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f6a77-115">Requirements</span></span>



| <span data-ttu-id="f6a77-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f6a77-116">Requirement</span></span> | <span data-ttu-id="f6a77-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f6a77-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a77-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6a77-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6a77-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6a77-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6a77-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6a77-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6a77-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f6a77-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6a77-122">Header</span><span class="sxs-lookup"><span data-stu-id="f6a77-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6a77-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6a77-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f6a77-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f6a77-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f6a77-125">**Кбем \_ ИНСЕРТИТЕМВ** (Юникод) и **кбем \_ инсертитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f6a77-125">**CBEM\_INSERTITEMW** (Unicode) and **CBEM\_INSERTITEMA** (ANSI)</span></span><br/>           |



 

 





