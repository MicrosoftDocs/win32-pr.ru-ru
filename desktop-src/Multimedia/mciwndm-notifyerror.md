---
title: Сообщение MCIWNDM_NOTIFYERROR (VFW. h)
description: Сообщение МЦИВНДМ \_ нотиферрор уведомляет родительское окно приложения о том, что произошла ошибка MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071495"
---
# <a name="mciwndm_notifyerror-message"></a><span data-ttu-id="95bc0-104">\_Сообщение мЦивндм нотиферрор</span><span class="sxs-lookup"><span data-stu-id="95bc0-104">MCIWNDM\_NOTIFYERROR message</span></span>

<span data-ttu-id="95bc0-105">Сообщение **мЦивндм \_ нотиферрор** уведомляет родительское окно приложения о том, что произошла ошибка MCI.</span><span class="sxs-lookup"><span data-stu-id="95bc0-105">The **MCIWNDM\_NOTIFYERROR** message notifies the parent window of an application that an MCI error occurred.</span></span>


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a><span data-ttu-id="95bc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95bc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95bc0-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="95bc0-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="95bc0-108">Обработайте окно МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="95bc0-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="95bc0-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*Код ошибки*</span><span class="sxs-lookup"><span data-stu-id="95bc0-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span></span>
</dt> <dd>

<span data-ttu-id="95bc0-110">Числовой код для ошибки MCI.</span><span class="sxs-lookup"><span data-stu-id="95bc0-110">Numerical code for the MCI error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95bc0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95bc0-111">Remarks</span></span>

<span data-ttu-id="95bc0-112">Вы можете включить уведомление об ошибке MCI, указав \_ стиль окна мЦивндф нотиферрор.</span><span class="sxs-lookup"><span data-stu-id="95bc0-112">You can enable MCI error notification by specifying the MCIWNDF\_NOTIFYERROR window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="95bc0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="95bc0-113">Requirements</span></span>



| <span data-ttu-id="95bc0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="95bc0-114">Requirement</span></span> | <span data-ttu-id="95bc0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="95bc0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="95bc0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95bc0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95bc0-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="95bc0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="95bc0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95bc0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95bc0-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="95bc0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="95bc0-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="95bc0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="95bc0-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="95bc0-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





