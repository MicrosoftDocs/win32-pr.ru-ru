---
description: Извлекает ограничивающий прямоугольник панели задач Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Сообщение ABM_GETTASKBARPOS (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540599"
---
# <a name="abm_gettaskbarpos-message"></a><span data-ttu-id="24ee7-103">\_Сообщение АБМ жеттаскбарпос</span><span class="sxs-lookup"><span data-stu-id="24ee7-103">ABM\_GETTASKBARPOS message</span></span>

<span data-ttu-id="24ee7-104">Извлекает ограничивающий прямоугольник панели задач Windows.</span><span class="sxs-lookup"><span data-stu-id="24ee7-104">Retrieves the bounding rectangle of the Windows taskbar.</span></span>


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a><span data-ttu-id="24ee7-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="24ee7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ee7-106">*пабд*</span><span class="sxs-lookup"><span data-stu-id="24ee7-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="24ee7-107">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) , член- **кандидат** которой получает ограничивающий прямоугольник (в экранных координатах) панели задач.</span><span class="sxs-lookup"><span data-stu-id="24ee7-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure whose **rc** member receives the bounding rectangle, in screen coordinates, of the taskbar.</span></span> <span data-ttu-id="24ee7-108">При отправке этого сообщения необходимо указать **кбсизе** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="24ee7-108">You must specify the **cbSize** when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ee7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24ee7-109">Return value</span></span>

<span data-ttu-id="24ee7-110">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="24ee7-110">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="24ee7-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="24ee7-111">Remarks</span></span>

<span data-ttu-id="24ee7-112">Обратите внимание, что это относится только к системной панели задач.</span><span class="sxs-lookup"><span data-stu-id="24ee7-112">Note that this applies only to the system taskbar.</span></span> <span data-ttu-id="24ee7-113">Также могут присутствовать другие объекты, в частности панели инструментов, предоставляемые сторонним программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="24ee7-113">Other objects, particularly toolbars supplied with third-party software, also can be present.</span></span> <span data-ttu-id="24ee7-114">В результате часть области экрана, не охваченной панелью задач Windows, может быть невидима для пользователя.</span><span class="sxs-lookup"><span data-stu-id="24ee7-114">As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user.</span></span> <span data-ttu-id="24ee7-115">Чтобы получить область экрана, не охваченную панелью задач и другими панелями приложений, доступной для приложения, используйте функцию [**жетмониторинфо**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="24ee7-115">To retrieve the area of the screen not covered by both the taskbar and other app bars the working area available to your application , use the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="24ee7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="24ee7-116">Requirements</span></span>



| <span data-ttu-id="24ee7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="24ee7-117">Requirement</span></span> | <span data-ttu-id="24ee7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="24ee7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24ee7-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24ee7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="24ee7-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="24ee7-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="24ee7-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24ee7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="24ee7-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24ee7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24ee7-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="24ee7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="24ee7-124"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="24ee7-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

