---
title: Сообщение MCIWNDM_NOTIFYPOS (VFW. h)
description: Сообщение МЦИВНДМ \_ нотифипос уведомляет родительское окно приложения о том, что его расположение изменилось.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989157"
---
# <a name="mciwndm_notifypos-message"></a><span data-ttu-id="977b5-104">\_Сообщение мЦивндм нотифипос</span><span class="sxs-lookup"><span data-stu-id="977b5-104">MCIWNDM\_NOTIFYPOS message</span></span>

<span data-ttu-id="977b5-105">Сообщение **мЦивндм \_ нотифипос** уведомляет родительское окно приложения о том, что его расположение изменилось.</span><span class="sxs-lookup"><span data-stu-id="977b5-105">The **MCIWNDM\_NOTIFYPOS** message notifies the parent window of an application that the window position has changed.</span></span>


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a><span data-ttu-id="977b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="977b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="977b5-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="977b5-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="977b5-108">Обработайте окно МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="977b5-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="977b5-109"><span id="pos"></span><span id="POS"></span>*POS*</span><span class="sxs-lookup"><span data-stu-id="977b5-109"><span id="pos"></span><span id="POS"></span>*pos*</span></span>
</dt> <dd>

<span data-ttu-id="977b5-110">Описывает новую точку.</span><span class="sxs-lookup"><span data-stu-id="977b5-110">Describes the new position.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="977b5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="977b5-111">Remarks</span></span>

<span data-ttu-id="977b5-112">Вы можете включить уведомления об изменениях в положении окна МЦивнд, указав \_ стиль окна мЦивндф нотифипос.</span><span class="sxs-lookup"><span data-stu-id="977b5-112">You can enable notification of changes in the position of an MCIWnd window by specifying the MCIWNDF\_NOTIFYPOS window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="977b5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="977b5-113">Requirements</span></span>



| <span data-ttu-id="977b5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="977b5-114">Requirement</span></span> | <span data-ttu-id="977b5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="977b5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="977b5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="977b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="977b5-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="977b5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="977b5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="977b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="977b5-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="977b5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="977b5-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="977b5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="977b5-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="977b5-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





