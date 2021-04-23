---
description: '\_Тип данных обработчика сцесвк — это непрозрачный маркер, предоставляемый набором средств настройки безопасности.'
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (Сцесвк. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540975"
---
# <a name="scesvc_handle"></a><span data-ttu-id="0ee3a-103">СЦЕСВК, \_ обработчик</span><span class="sxs-lookup"><span data-stu-id="0ee3a-103">SCESVC\_HANDLE</span></span>

<span data-ttu-id="0ee3a-104">Тип **данных \_ обработчика сцесвк** — это непрозрачный маркер, предоставляемый набором средств настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="0ee3a-104">The **SCESVC\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="0ee3a-105">Он используется методами интерфейсов [**исцесвкаттачментдата**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) и [**исцесвкаттачментперсистинфо**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) для передачи информации между оснасткой настройки безопасности и расширением оснастки.</span><span class="sxs-lookup"><span data-stu-id="0ee3a-105">It is used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span>


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="0ee3a-106">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee3a-106">Requirements</span></span>



| <span data-ttu-id="0ee3a-107">Требование</span><span class="sxs-lookup"><span data-stu-id="0ee3a-107">Requirement</span></span> | <span data-ttu-id="0ee3a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0ee3a-108">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee3a-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ee3a-109">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee3a-110">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0ee3a-110">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0ee3a-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ee3a-111">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee3a-112">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ee3a-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0ee3a-113">Header</span><span class="sxs-lookup"><span data-stu-id="0ee3a-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ee3a-114"><dt>Сцесвк. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ee3a-114"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee3a-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ee3a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee3a-116">**исцесвкаттачментдата**</span><span class="sxs-lookup"><span data-stu-id="0ee3a-116">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[<span data-ttu-id="0ee3a-117">**исцесвкаттачментперсистинфо**</span><span class="sxs-lookup"><span data-stu-id="0ee3a-117">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




