---
description: Оповещает систему об изменении расположения панель приложений. Панель приложений должен вызывать это сообщение в ответ на \_ сообщение ВИНДОВПОСЧАНЖЕД WM.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: Сообщение ABM_WINDOWPOSCHANGED (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497049"
---
# <a name="abm_windowposchanged-message"></a><span data-ttu-id="315aa-104">\_Сообщение АБМ виндовпосчанжед</span><span class="sxs-lookup"><span data-stu-id="315aa-104">ABM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="315aa-105">Оповещает систему об изменении расположения панель приложений.</span><span class="sxs-lookup"><span data-stu-id="315aa-105">Notifies the system when an appbar's position has changed.</span></span> <span data-ttu-id="315aa-106">Панель приложений должен вызывать это сообщение в ответ на сообщение [**\_ виндовпосчанжед WM**](/windows/desktop/winmsg/wm-windowposchanged) .</span><span class="sxs-lookup"><span data-stu-id="315aa-106">An appbar should call this message in response to the [**WM\_WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) message.</span></span>


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="315aa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="315aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315aa-108">*пабд*</span><span class="sxs-lookup"><span data-stu-id="315aa-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="315aa-109">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) , определяющую панель приложений для активации.</span><span class="sxs-lookup"><span data-stu-id="315aa-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="315aa-110">При отправке этого сообщения необходимо указать элементы **кбсизе** и **HWND** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="315aa-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315aa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="315aa-111">Return value</span></span>

<span data-ttu-id="315aa-112">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="315aa-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="315aa-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="315aa-113">Remarks</span></span>

<span data-ttu-id="315aa-114">Это сообщение пропускается, если элемент **HWND** структуры, на который указывает *пабд* , определяет панель приложений автоскрытия.</span><span class="sxs-lookup"><span data-stu-id="315aa-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="315aa-115">Требования</span><span class="sxs-lookup"><span data-stu-id="315aa-115">Requirements</span></span>



| <span data-ttu-id="315aa-116">Требование</span><span class="sxs-lookup"><span data-stu-id="315aa-116">Requirement</span></span> | <span data-ttu-id="315aa-117">Значение</span><span class="sxs-lookup"><span data-stu-id="315aa-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="315aa-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="315aa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="315aa-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="315aa-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="315aa-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="315aa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="315aa-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="315aa-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="315aa-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="315aa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="315aa-123"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="315aa-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

