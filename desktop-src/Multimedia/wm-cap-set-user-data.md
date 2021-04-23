---
title: Сообщение WM_CAP_SET_USER_DATA (VFW. h)
description: '\_ \_ Сообщение пользовательских данных для установки крепления WM \_ \_ связывает длинное \_ значение PTR с окном записи. Это сообщение можно отправить явно или с помощью макроса Капсетусердата.'
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137518"
---
# <a name="wm_cap_set_user_data-message"></a><span data-ttu-id="0a6bd-105">\_Сообщение о \_ задании \_ \_ данных пользователя с закреплениями WM</span><span class="sxs-lookup"><span data-stu-id="0a6bd-105">WM\_CAP\_SET\_USER\_DATA message</span></span>

<span data-ttu-id="0a6bd-106">Сообщение **\_ \_ \_ пользовательских \_ данных для установки крепления WM** связывает **длинное значение \_ ptr** с окном записи.</span><span class="sxs-lookup"><span data-stu-id="0a6bd-106">The **WM\_CAP\_SET\_USER\_DATA** message associates a **LONG\_PTR** data value with a capture window.</span></span> <span data-ttu-id="0a6bd-107">Это сообщение можно отправить явно или с помощью макроса [**капсетусердата**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="0a6bd-107">You can send this message explicitly or by using the [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) macro.</span></span>


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a><span data-ttu-id="0a6bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a6bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a6bd-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*лусер*</span><span class="sxs-lookup"><span data-stu-id="0a6bd-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span></span>
</dt> <dd>

<span data-ttu-id="0a6bd-110">Значение типа данных, связываемое с окном записи.</span><span class="sxs-lookup"><span data-stu-id="0a6bd-110">Data value to associate with a capture window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a6bd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a6bd-111">Return Value</span></span>

<span data-ttu-id="0a6bd-112">Возвращает **значение true** в случае успеха или **false** , если потоковая запись выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a6bd-112">Returns **TRUE** if successful or **FALSE** if streaming capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a6bd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a6bd-113">Remarks</span></span>

<span data-ttu-id="0a6bd-114">Обычно это сообщение используется для указания на блок данных, связанных с окном записи.</span><span class="sxs-lookup"><span data-stu-id="0a6bd-114">Typically this message is used to point to a block of data associated with a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a6bd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0a6bd-115">Requirements</span></span>



| <span data-ttu-id="0a6bd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0a6bd-116">Requirement</span></span> | <span data-ttu-id="0a6bd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0a6bd-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0a6bd-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a6bd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a6bd-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0a6bd-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0a6bd-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a6bd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a6bd-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0a6bd-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0a6bd-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0a6bd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a6bd-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a6bd-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a6bd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a6bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6bd-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="0a6bd-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0a6bd-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="0a6bd-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





