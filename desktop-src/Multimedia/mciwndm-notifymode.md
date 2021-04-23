---
title: Сообщение MCIWNDM_NOTIFYMODE (VFW. h)
description: Сообщение МЦИВНДМ \_ нотифимоде уведомляет родительское окно приложения о том, что режим работы устройства mci изменился.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071090"
---
# <a name="mciwndm_notifymode-message"></a><span data-ttu-id="387a5-104">\_Сообщение мЦивндм нотифимоде</span><span class="sxs-lookup"><span data-stu-id="387a5-104">MCIWNDM\_NOTIFYMODE message</span></span>

<span data-ttu-id="387a5-105">Сообщение **мЦивндм \_ нотифимоде** уведомляет родительское окно приложения о том, что режим работы устройства mci изменился.</span><span class="sxs-lookup"><span data-stu-id="387a5-105">The **MCIWNDM\_NOTIFYMODE** message notifies the parent window of an application that the operating mode of the MCI device has changed.</span></span>


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a><span data-ttu-id="387a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="387a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387a5-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="387a5-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="387a5-108">Обработайте окно МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="387a5-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="387a5-109"><span id="mode"></span><span id="MODE"></span>*режима*</span><span class="sxs-lookup"><span data-stu-id="387a5-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="387a5-110">Целое число, соответствующее режиму MCI.</span><span class="sxs-lookup"><span data-stu-id="387a5-110">Integer corresponding to the MCI mode.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="387a5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="387a5-111">Remarks</span></span>

<span data-ttu-id="387a5-112">Вы можете включить уведомления об изменениях режима устройства MCI, указав \_ стиль окна мЦивндф нотифимоде.</span><span class="sxs-lookup"><span data-stu-id="387a5-112">You can enable notification of mode changes of an MCI device by specifying the MCIWNDF\_NOTIFYMODE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="387a5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="387a5-113">Requirements</span></span>



| <span data-ttu-id="387a5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="387a5-114">Requirement</span></span> | <span data-ttu-id="387a5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="387a5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="387a5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="387a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="387a5-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="387a5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="387a5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="387a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="387a5-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="387a5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="387a5-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="387a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="387a5-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="387a5-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





