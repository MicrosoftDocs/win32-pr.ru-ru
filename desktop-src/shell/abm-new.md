---
description: Регистрирует новый панель приложений и указывает идентификатор сообщения, который система должна использовать для отправки сообщений уведомления. Панель приложений должен отправить это сообщение перед отправкой любых других сообщений панель приложений.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Сообщение ABM_NEW (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808884"
---
# <a name="abm_new-message"></a><span data-ttu-id="c4438-104">АБМ \_ новое сообщение</span><span class="sxs-lookup"><span data-stu-id="c4438-104">ABM\_NEW message</span></span>

<span data-ttu-id="c4438-105">Регистрирует новый панель приложений и указывает идентификатор сообщения, который система должна использовать для отправки сообщений уведомления.</span><span class="sxs-lookup"><span data-stu-id="c4438-105">Registers a new appbar and specifies the message identifier that the system should use to send it notification messages.</span></span> <span data-ttu-id="c4438-106">Панель приложений должен отправить это сообщение перед отправкой любых других сообщений панель приложений.</span><span class="sxs-lookup"><span data-stu-id="c4438-106">An appbar should send this message before sending any other appbar messages.</span></span>


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="c4438-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4438-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4438-108">*пабд*</span><span class="sxs-lookup"><span data-stu-id="c4438-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="c4438-109">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) , которая содержит маркер окна нового панель приложений и идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="c4438-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the new appbar's window handle and message identifier.</span></span> <span data-ttu-id="c4438-110">При отправке этого сообщения необходимо указать члены **кбсизе**, **HWND** и **укаллбаккмессаже** ; все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="c4438-110">You must specify the **cbSize**, **hWnd**, and **uCallbackMessage** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4438-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4438-111">Return value</span></span>

<span data-ttu-id="c4438-112">Возвращает **значение true** в случае успеха или **значение false** , если возникла ошибка, или если панель приложений уже зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="c4438-112">Returns **TRUE** if successful, or **FALSE** if an error occurs or if the appbar is already registered.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4438-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c4438-113">Requirements</span></span>



| <span data-ttu-id="c4438-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c4438-114">Requirement</span></span> | <span data-ttu-id="c4438-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c4438-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4438-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4438-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c4438-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c4438-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c4438-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4438-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c4438-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4438-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4438-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c4438-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4438-121"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4438-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




