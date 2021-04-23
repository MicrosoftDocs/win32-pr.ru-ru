---
title: Сообщение HDM_GETORDERARRAY (Коммктрл. h)
description: Возвращает текущий порядок элементов в элементе управления "заголовок" слева направо. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса жетордераррай.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- Элементы управления Windows для HDM_GETORDERARRAY сообщений
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135959"
---
# <a name="hdm_getorderarray-message"></a><span data-ttu-id="8b5fa-105">\_Сообщение ЖЕТОРДЕРАРРАЙ HDM</span><span class="sxs-lookup"><span data-stu-id="8b5fa-105">HDM\_GETORDERARRAY message</span></span>

<span data-ttu-id="8b5fa-106">Возвращает текущий порядок элементов в элементе управления "заголовок" слева направо.</span><span class="sxs-lookup"><span data-stu-id="8b5fa-106">Gets the current left-to-right order of items in a header control.</span></span> <span data-ttu-id="8b5fa-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ жетордераррай**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .</span><span class="sxs-lookup"><span data-stu-id="8b5fa-107">You can send this message explicitly or use the [**Header\_GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b5fa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b5fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5fa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b5fa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fa-110">Число целочисленных элементов, которые может содержать *lParam* .</span><span class="sxs-lookup"><span data-stu-id="8b5fa-110">The number of integer elements that *lParam* can hold.</span></span> <span data-ttu-id="8b5fa-111">Это значение должно быть равно числу элементов в элементе управления (см. раздел [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).</span><span class="sxs-lookup"><span data-stu-id="8b5fa-111">This value must be equal to the number of items in the control (see [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8b5fa-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b5fa-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fa-113">Указатель на массив целых чисел, получающий значения индекса для элементов в заголовке.</span><span class="sxs-lookup"><span data-stu-id="8b5fa-113">A pointer to an array of integers that receive the index values for items in the header.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5fa-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b5fa-114">Return value</span></span>

<span data-ttu-id="8b5fa-115">Возвращает ненулевое значение в случае успеха, и буфер в *lParam* получает номер элемента для каждого элемента в элементе управления "заголовок" в том порядке, в котором они отображаются слева направо.</span><span class="sxs-lookup"><span data-stu-id="8b5fa-115">Returns nonzero if successful, and the buffer at *lParam* receives the item number for each item in the header control in the order in which they appear from left to right.</span></span> <span data-ttu-id="8b5fa-116">В противном случае сообщение возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8b5fa-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b5fa-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b5fa-117">Remarks</span></span>

<span data-ttu-id="8b5fa-118">Число элементов в параметре *lParam* указывается в параметре *wParam* и должно быть равно числу элементов в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="8b5fa-118">The number of elements in *lParam* is specified in *wParam* and must be equal to the number of items in the control.</span></span> <span data-ttu-id="8b5fa-119">Например, следующий фрагмент кода зарезервирует достаточно памяти для хранения значений индекса.</span><span class="sxs-lookup"><span data-stu-id="8b5fa-119">For example, the following code fragment will reserve enough memory to hold the index values.</span></span>


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a><span data-ttu-id="8b5fa-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8b5fa-120">Requirements</span></span>



| <span data-ttu-id="8b5fa-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8b5fa-121">Requirement</span></span> | <span data-ttu-id="8b5fa-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8b5fa-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5fa-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b5fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b5fa-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b5fa-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b5fa-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b5fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b5fa-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b5fa-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b5fa-127">Header</span><span class="sxs-lookup"><span data-stu-id="8b5fa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b5fa-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b5fa-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





