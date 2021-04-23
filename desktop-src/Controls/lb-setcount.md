---
title: Сообщение LB_SETCOUNT (Winuser. h)
description: Задает количество элементов в списке, созданных с помощью стиля «нехасстрингс ФУНТа» \_ и не создаваемого с помощью стиля фунта \_ .
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- Элементы управления Windows для LB_SETCOUNT сообщений
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071909"
---
# <a name="lb_setcount-message"></a><span data-ttu-id="58819-104">Сообщение сеткаунт балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="58819-104">LB\_SETCOUNT message</span></span>

<span data-ttu-id="58819-105">Задает количество элементов в списке, созданных с помощью стиля « [**\_ Нехасстрингс**](list-box-styles.md) [**\_ фунта**](list-box-styles.md) » и не создаваемого с помощью стиля фунта.</span><span class="sxs-lookup"><span data-stu-id="58819-105">Sets the count of items in a list box created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="58819-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="58819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58819-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58819-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58819-108">Указывает новое число элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="58819-108">Specifies the new count of items in the list box.</span></span>

<span data-ttu-id="58819-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="58819-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="58819-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="58819-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="58819-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="58819-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="58819-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58819-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58819-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="58819-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58819-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58819-114">Return value</span></span>

<span data-ttu-id="58819-115">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="58819-115">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="58819-116">Если недостаточно памяти для хранения элементов, возвращается значение фунтов \_ еррспаце.</span><span class="sxs-lookup"><span data-stu-id="58819-116">If there is insufficient memory to store the items, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="58819-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58819-117">Remarks</span></span>

<span data-ttu-id="58819-118">Сообщение **\_ сеткаунт** поддерживается только в списках, созданных с помощью стиля «недоступность фунтов» и не созданного с помощью стиля [**фунта \_ хасстрингс**](list-box-styles.md) . [**\_**](list-box-styles.md)</span><span class="sxs-lookup"><span data-stu-id="58819-118">The **LB\_SETCOUNT** message is supported only by list boxes created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span> <span data-ttu-id="58819-119">Все остальные списки возвращают ошибку балансировки нагрузки \_ .</span><span class="sxs-lookup"><span data-stu-id="58819-119">All other list boxes return LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="58819-120">Требования</span><span class="sxs-lookup"><span data-stu-id="58819-120">Requirements</span></span>



| <span data-ttu-id="58819-121">Требование</span><span class="sxs-lookup"><span data-stu-id="58819-121">Requirement</span></span> | <span data-ttu-id="58819-122">Значение</span><span class="sxs-lookup"><span data-stu-id="58819-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58819-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58819-123">Minimum supported client</span></span><br/> | <span data-ttu-id="58819-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58819-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58819-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58819-125">Minimum supported server</span></span><br/> | <span data-ttu-id="58819-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58819-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58819-127">Header</span><span class="sxs-lookup"><span data-stu-id="58819-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="58819-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58819-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58819-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58819-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58819-130">**\_Счетчик фунтов**</span><span class="sxs-lookup"><span data-stu-id="58819-130">**LB\_GETCOUNT**</span></span>](lb-getcount.md)
</dt> </dl>

 

 





