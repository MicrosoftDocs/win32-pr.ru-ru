---
description: Запрашивает размер и расположение экрана для панель приложений.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Сообщение ABM_QUERYPOS (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342865"
---
# <a name="abm_querypos-message"></a><span data-ttu-id="70a1f-103">\_Сообщение АБМ куерипос</span><span class="sxs-lookup"><span data-stu-id="70a1f-103">ABM\_QUERYPOS message</span></span>

<span data-ttu-id="70a1f-104">Запрашивает размер и расположение экрана для панель приложений.</span><span class="sxs-lookup"><span data-stu-id="70a1f-104">Requests a size and screen position for an appbar.</span></span> <span data-ttu-id="70a1f-105">При выполнении запроса в сообщении предлагается ребро экрана и ограничивающий прямоугольник для панель приложений.</span><span class="sxs-lookup"><span data-stu-id="70a1f-105">When the request is made, the message proposes a screen edge and a bounding rectangle for the appbar.</span></span> <span data-ttu-id="70a1f-106">Система корректирует ограничивающий прямоугольник таким образом, чтобы панель приложений не влияла на панель задач Windows или другие AppBar.</span><span class="sxs-lookup"><span data-stu-id="70a1f-106">The system adjusts the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="70a1f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="70a1f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70a1f-108">*пабд*</span><span class="sxs-lookup"><span data-stu-id="70a1f-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="70a1f-109">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="70a1f-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="70a1f-110">Элемент **уедже** задает ребро экрана, а член **RC** содержит предложенный ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="70a1f-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the proposed bounding rectangle.</span></span> <span data-ttu-id="70a1f-111">Когда функция [**шаппбармессаже**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) возвращает, **RC** содержит утвержденный ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="70a1f-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="70a1f-112">При отправке этого сообщения необходимо указать члены **кбсизе**, **HWND**, **уедже** и **RC** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="70a1f-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70a1f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70a1f-113">Return value</span></span>

<span data-ttu-id="70a1f-114">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="70a1f-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="70a1f-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="70a1f-115">Remarks</span></span>

<span data-ttu-id="70a1f-116">Объект панель приложений должен отправить это сообщение перед отправкой сообщения [**\_ сетпос АБМ**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="70a1f-116">An appbar should send this message before sending the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a1f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="70a1f-117">Requirements</span></span>



| <span data-ttu-id="70a1f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="70a1f-118">Requirement</span></span> | <span data-ttu-id="70a1f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="70a1f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70a1f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70a1f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70a1f-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="70a1f-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="70a1f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70a1f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70a1f-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70a1f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70a1f-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="70a1f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="70a1f-125"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="70a1f-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




