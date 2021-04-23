---
title: Сообщение LB_SETLOCALE (Winuser. h)
description: Задает текущий языковой стандарт для списка. Языковой стандарт можно использовать для определения правильного порядка сортировки отображаемого текста (для списков с \_ стилем сортировки фунтов) и текста, добавленного \_ сообщением ADDSTRING балансировки нагрузки.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- Элементы управления Windows для LB_SETLOCALE сообщений
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071908"
---
# <a name="lb_setlocale-message"></a><span data-ttu-id="10884-105">Сообщение ФУНТОВой \_ SETLOCALE</span><span class="sxs-lookup"><span data-stu-id="10884-105">LB\_SETLOCALE message</span></span>

<span data-ttu-id="10884-106">Задает текущий языковой стандарт для списка.</span><span class="sxs-lookup"><span data-stu-id="10884-106">Sets the current locale of the list box.</span></span> <span data-ttu-id="10884-107">Языковой стандарт можно использовать для определения правильного порядка сортировки отображаемого текста (для списков с стилем [**\_ сортировки фунтов**](list-box-styles.md) ) и текста, добавленного сообщением [**\_ ADDSTRING балансировки нагрузки**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="10884-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="10884-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="10884-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10884-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10884-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10884-110">Указывает код локали, который будет использоваться списком для сортировки при добавлении текста.</span><span class="sxs-lookup"><span data-stu-id="10884-110">Specifies the locale identifier that the list box will use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="10884-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10884-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10884-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="10884-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10884-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10884-113">Return value</span></span>

<span data-ttu-id="10884-114">Возвращаемое значение — это предыдущий идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="10884-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="10884-115">Если параметр *wParam* задает языковой стандарт, который не установлен в системе, возвращается значение фунтов \_ Err, а текущий языковой стандарт списка не изменяется.</span><span class="sxs-lookup"><span data-stu-id="10884-115">If the *wParam* parameter specifies a locale that is not installed on the system, the return value is LB\_ERR and the current list box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="10884-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10884-116">Remarks</span></span>

<span data-ttu-id="10884-117">Используйте макрос [**макелЦид**](/windows/desktop/api/winnt/nf-winnt-makelcid) для создания идентификатора локали.</span><span class="sxs-lookup"><span data-stu-id="10884-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="10884-118">Требования</span><span class="sxs-lookup"><span data-stu-id="10884-118">Requirements</span></span>



| <span data-ttu-id="10884-119">Требование</span><span class="sxs-lookup"><span data-stu-id="10884-119">Requirement</span></span> | <span data-ttu-id="10884-120">Значение</span><span class="sxs-lookup"><span data-stu-id="10884-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10884-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10884-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10884-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10884-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="10884-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10884-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10884-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10884-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10884-125">Header</span><span class="sxs-lookup"><span data-stu-id="10884-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="10884-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10884-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10884-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10884-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="10884-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="10884-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10884-129">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="10884-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="10884-130">**Нестандартная балансировка нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="10884-130">**LB\_GETLOCALE**</span></span>](lb-getlocale.md)
</dt> </dl>

 

