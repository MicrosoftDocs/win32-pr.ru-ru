---
description: Запрашивает заголовок и текст всплывающей подсказки для элемента, указанного сопутствующей структурой СМДАТА.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Сообщение SMC_CHEVRONGETTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985748"
---
# <a name="smc_chevrongettip-message"></a><span data-ttu-id="5c513-103">\_Сообщение SMC чевронжеттип</span><span class="sxs-lookup"><span data-stu-id="5c513-103">SMC\_CHEVRONGETTIP message</span></span>

<span data-ttu-id="5c513-104">Запрашивает заголовок и текст всплывающей подсказки для элемента, указанного сопутствующей структурой [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="5c513-104">Requests the title and text for a chevron infotip for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a><span data-ttu-id="5c513-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c513-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c513-106">*пвсзтиптитле*</span><span class="sxs-lookup"><span data-stu-id="5c513-106">*pwszTipTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="5c513-107">Указатель на буфер, который получает строку в Юникоде, завершающуюся **нулем**, которая содержит заголовок подсказки.</span><span class="sxs-lookup"><span data-stu-id="5c513-107">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's title.</span></span> <span data-ttu-id="5c513-108">Длина этой строки не должна превышать максимальное число \_ символов в пути, включая завершающий символ **null** .</span><span class="sxs-lookup"><span data-stu-id="5c513-108">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="5c513-109">*пвсзтиптекст*</span><span class="sxs-lookup"><span data-stu-id="5c513-109">*pwszTipText*</span></span> 
</dt> <dd>

<span data-ttu-id="5c513-110">Указатель на буфер, который получает строку в Юникоде, завершающуюся **нулем**, которая содержит текст подсказки.</span><span class="sxs-lookup"><span data-stu-id="5c513-110">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's text.</span></span> <span data-ttu-id="5c513-111">Длина этой строки не должна превышать максимальное число \_ символов в пути, включая завершающий символ **null** .</span><span class="sxs-lookup"><span data-stu-id="5c513-111">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c513-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c513-112">Return value</span></span>

<span data-ttu-id="5c513-113">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5c513-113">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c513-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c513-114">Remarks</span></span>

<span data-ttu-id="5c513-115">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="5c513-115">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c513-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5c513-116">Requirements</span></span>



| <span data-ttu-id="5c513-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5c513-117">Requirement</span></span> | <span data-ttu-id="5c513-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5c513-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c513-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c513-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c513-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c513-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5c513-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c513-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c513-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c513-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c513-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5c513-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c513-124"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c513-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c513-125">IDL</span><span class="sxs-lookup"><span data-stu-id="5c513-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c513-126"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c513-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




