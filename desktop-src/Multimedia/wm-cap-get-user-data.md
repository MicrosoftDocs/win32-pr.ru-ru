---
title: Сообщение WM_CAP_GET_USER_DATA (VFW. h)
description: Сообщение о \_ \_ получении \_ \_ данных об ошибке WM Cap Получает длинное \_ значение типа PTR, связанное с окном сбора данных. Это сообщение можно отправить явно или с помощью макроса Капжетусердата.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535021"
---
# <a name="wm_cap_get_user_data-message"></a><span data-ttu-id="6538f-105">\_Сообщение о \_ получении \_ \_ данных пользователя с креплениями WM</span><span class="sxs-lookup"><span data-stu-id="6538f-105">WM\_CAP\_GET\_USER\_DATA message</span></span>

<span data-ttu-id="6538f-106">Сообщение **о \_ \_ получении \_ \_ данных** об ошибке WM Cap получает **длинное значение \_ типа PTR** , связанное с окном сбора данных.</span><span class="sxs-lookup"><span data-stu-id="6538f-106">The **WM\_CAP\_GET\_USER\_DATA** message retrieves a **LONG\_PTR** data value associated with a capture window.</span></span> <span data-ttu-id="6538f-107">Это сообщение можно отправить явно или с помощью макроса [**капжетусердата**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="6538f-107">You can send this message explicitly or by using the [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) macro.</span></span>


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="6538f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6538f-108">Return Value</span></span>

<span data-ttu-id="6538f-109">Возвращает значение, сохраненное ранее с помощью сообщения о [**\_ \_ \_ пользовательских \_ данных для установки крепления WM**](wm-cap-set-user-data.md) .</span><span class="sxs-lookup"><span data-stu-id="6538f-109">Returns a value previously saved by using the [**WM\_CAP\_SET\_USER\_DATA**](wm-cap-set-user-data.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6538f-110">Требования</span><span class="sxs-lookup"><span data-stu-id="6538f-110">Requirements</span></span>



| <span data-ttu-id="6538f-111">Требование</span><span class="sxs-lookup"><span data-stu-id="6538f-111">Requirement</span></span> | <span data-ttu-id="6538f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6538f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6538f-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6538f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6538f-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6538f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6538f-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6538f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6538f-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6538f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6538f-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6538f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6538f-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6538f-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6538f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6538f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6538f-120">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="6538f-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6538f-121">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="6538f-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





