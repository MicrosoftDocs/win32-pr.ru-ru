---
description: Уведомляет систему о том, что панель приложений был активирован. Объект панель приложений должен вызывать это сообщение в ответ на \_ сообщение активации WM.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Сообщение ABM_ACTIVATE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143999"
---
# <a name="abm_activate-message"></a><span data-ttu-id="33f8f-104">\_Сообщение о активации АБМ</span><span class="sxs-lookup"><span data-stu-id="33f8f-104">ABM\_ACTIVATE message</span></span>

<span data-ttu-id="33f8f-105">Уведомляет систему о том, что панель приложений был активирован.</span><span class="sxs-lookup"><span data-stu-id="33f8f-105">Notifies the system that an appbar has been activated.</span></span> <span data-ttu-id="33f8f-106">Объект панель приложений должен вызывать это сообщение в ответ на сообщение [**\_ активации WM**](/windows/desktop/inputdev/wm-activate) .</span><span class="sxs-lookup"><span data-stu-id="33f8f-106">An appbar should call this message in response to the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message.</span></span>


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a><span data-ttu-id="33f8f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="33f8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f8f-108">*пабд*</span><span class="sxs-lookup"><span data-stu-id="33f8f-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="33f8f-109">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) , определяющую панель приложений для активации.</span><span class="sxs-lookup"><span data-stu-id="33f8f-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="33f8f-110">При отправке этого сообщения необходимо указать элементы **кбсизе** и **HWND** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="33f8f-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33f8f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33f8f-111">Return value</span></span>

<span data-ttu-id="33f8f-112">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="33f8f-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="33f8f-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="33f8f-113">Remarks</span></span>

<span data-ttu-id="33f8f-114">Это сообщение пропускается, если элемент **HWND** структуры, на который указывает *пабд* , определяет панель приложений автоскрытия.</span><span class="sxs-lookup"><span data-stu-id="33f8f-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span> <span data-ttu-id="33f8f-115">Система автоматически задает z-порядок для автоскрытия AppBar.</span><span class="sxs-lookup"><span data-stu-id="33f8f-115">The system automatically sets the z-order for autohide appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f8f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="33f8f-116">Requirements</span></span>



| <span data-ttu-id="33f8f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="33f8f-117">Requirement</span></span> | <span data-ttu-id="33f8f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="33f8f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33f8f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33f8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="33f8f-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="33f8f-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="33f8f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33f8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="33f8f-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33f8f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33f8f-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="33f8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="33f8f-124"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="33f8f-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

