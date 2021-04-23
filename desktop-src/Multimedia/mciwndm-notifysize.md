---
title: Сообщение MCIWNDM_NOTIFYSIZE (VFW. h)
description: Сообщение МЦИВНДМ \_ нотифисизе уведомляет родительское окно приложения о том, что размер окна изменился.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135667"
---
# <a name="mciwndm_notifysize-message"></a><span data-ttu-id="42392-104">\_Сообщение мЦивндм нотифисизе</span><span class="sxs-lookup"><span data-stu-id="42392-104">MCIWNDM\_NOTIFYSIZE message</span></span>

<span data-ttu-id="42392-105">Сообщение **мЦивндм \_ нотифисизе** уведомляет родительское окно приложения о том, что размер окна изменился.</span><span class="sxs-lookup"><span data-stu-id="42392-105">The **MCIWNDM\_NOTIFYSIZE** message notifies the parent window of an application that the window size has changed.</span></span>


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="42392-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42392-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="42392-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="42392-108">Обработайте окно МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="42392-108">Handle to the MCIWnd window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42392-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42392-109">Remarks</span></span>

<span data-ttu-id="42392-110">Вы можете включить уведомления об изменениях в размере окна МЦивнд, указав \_ стиль окна мЦивндф нотифисизе.</span><span class="sxs-lookup"><span data-stu-id="42392-110">You can enable notification of changes in the size of an MCIWnd window by specifying the MCIWNDF\_NOTIFYSIZE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="42392-111">Требования</span><span class="sxs-lookup"><span data-stu-id="42392-111">Requirements</span></span>



| <span data-ttu-id="42392-112">Требование</span><span class="sxs-lookup"><span data-stu-id="42392-112">Requirement</span></span> | <span data-ttu-id="42392-113">Значение</span><span class="sxs-lookup"><span data-stu-id="42392-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="42392-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42392-114">Minimum supported client</span></span><br/> | <span data-ttu-id="42392-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42392-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="42392-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42392-116">Minimum supported server</span></span><br/> | <span data-ttu-id="42392-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42392-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="42392-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="42392-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="42392-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="42392-119"><dt>Vfw.h</dt></span></span> </dl> |



 

 





