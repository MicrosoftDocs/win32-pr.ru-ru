---
description: Задает размер и расположение окна Панель приложений.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Сообщение ABM_SETPOS (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540594"
---
# <a name="abm_setpos-message"></a><span data-ttu-id="97695-103">\_Сообщение АБМ сетпос</span><span class="sxs-lookup"><span data-stu-id="97695-103">ABM\_SETPOS message</span></span>

<span data-ttu-id="97695-104">Задает размер и расположение окна Панель приложений.</span><span class="sxs-lookup"><span data-stu-id="97695-104">Sets the size and screen position of an appbar.</span></span> <span data-ttu-id="97695-105">В сообщении указывается ребро экрана и ограничивающий прямоугольник для панель приложений.</span><span class="sxs-lookup"><span data-stu-id="97695-105">The message specifies a screen edge and the bounding rectangle for the appbar.</span></span> <span data-ttu-id="97695-106">Система может настроить ограничивающий прямоугольник таким образом, чтобы панель приложений не влиял на панель задач Windows или другие AppBar.</span><span class="sxs-lookup"><span data-stu-id="97695-106">The system may adjust the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="97695-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="97695-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97695-108">*пабд*</span><span class="sxs-lookup"><span data-stu-id="97695-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="97695-109">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="97695-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="97695-110">Элемент **уедже** задает ребро экрана, а элемент **RC** содержит ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="97695-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the bounding rectangle.</span></span> <span data-ttu-id="97695-111">Когда функция [**шаппбармессаже**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) возвращает, **RC** содержит утвержденный ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="97695-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="97695-112">При отправке этого сообщения необходимо указать члены **кбсизе**, **HWND**, **уедже** и **RC** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="97695-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97695-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97695-113">Return value</span></span>

<span data-ttu-id="97695-114">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="97695-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97695-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="97695-115">Remarks</span></span>

<span data-ttu-id="97695-116">Это сообщение приводит к тому, что система отправляет сообщение уведомления [**АБН \_ посчанжед**](abn-poschanged.md) всем AppBar.</span><span class="sxs-lookup"><span data-stu-id="97695-116">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="97695-117">Требования</span><span class="sxs-lookup"><span data-stu-id="97695-117">Requirements</span></span>



| <span data-ttu-id="97695-118">Требование</span><span class="sxs-lookup"><span data-stu-id="97695-118">Requirement</span></span> | <span data-ttu-id="97695-119">Значение</span><span class="sxs-lookup"><span data-stu-id="97695-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97695-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97695-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97695-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="97695-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="97695-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97695-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97695-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="97695-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97695-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="97695-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97695-125"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="97695-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




