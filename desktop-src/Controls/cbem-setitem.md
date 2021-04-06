---
title: Сообщение CBEM_SETITEM (Коммктрл. h)
description: Задает атрибуты элемента в элементе управления ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- Элементы управления Windows для CBEM_SETITEM сообщений
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803700"
---
# <a name="cbem_setitem-message"></a><span data-ttu-id="43a26-104">\_Сообщение кбем сетитем</span><span class="sxs-lookup"><span data-stu-id="43a26-104">CBEM\_SETITEM message</span></span>

<span data-ttu-id="43a26-105">Задает атрибуты элемента в элементе управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="43a26-105">Sets the attributes for an item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="43a26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43a26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a26-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43a26-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43a26-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="43a26-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="43a26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43a26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43a26-110">Указатель на структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , содержащую сведения об элементе, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="43a26-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains the item information to be set.</span></span> <span data-ttu-id="43a26-111">При отправке сообщения элемент **маски** структуры должен быть установлен, чтобы указать, какие атрибуты являются допустимыми, а элемент **Член iItem** должен указывать Отсчитываемый от нуля индекс изменяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="43a26-111">When the message is sent, the **mask** member of the structure must be set to indicate which attributes are valid and the **iItem** member must specify the zero-based index of the item to be modified.</span></span> <span data-ttu-id="43a26-112">Установка элемента **Член iItem** в значение-1 приведет к изменению элемента, отображаемого в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="43a26-112">Setting the **iItem** member to -1 will modify the item displayed in the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a26-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43a26-113">Return value</span></span>

<span data-ttu-id="43a26-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="43a26-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a26-115">Требования</span><span class="sxs-lookup"><span data-stu-id="43a26-115">Requirements</span></span>



| <span data-ttu-id="43a26-116">Требование</span><span class="sxs-lookup"><span data-stu-id="43a26-116">Requirement</span></span> | <span data-ttu-id="43a26-117">Значение</span><span class="sxs-lookup"><span data-stu-id="43a26-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43a26-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43a26-118">Minimum supported client</span></span><br/> | <span data-ttu-id="43a26-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43a26-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43a26-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43a26-120">Minimum supported server</span></span><br/> | <span data-ttu-id="43a26-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43a26-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43a26-122">Header</span><span class="sxs-lookup"><span data-stu-id="43a26-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a26-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a26-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="43a26-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="43a26-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="43a26-125">**Кбем \_ СЕТИТЕМВ** (Юникод) и **кбем \_ сетитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="43a26-125">**CBEM\_SETITEMW** (Unicode) and **CBEM\_SETITEMA** (ANSI)</span></span><br/>                 |



 

 





