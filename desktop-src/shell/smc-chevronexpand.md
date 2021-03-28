---
description: Пользователь щелкнул Шеврон, чтобы развернуть элемент, указанный в соответствующей структуре СМДАТА.
title: Сообщение SMC_CHEVRONEXPAND (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6ecf8f86e111326b3f37f3111c382d2d04ef2fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265309"
---
# <a name="smc_chevronexpand-message"></a><span data-ttu-id="d9fcd-103">\_Сообщение SMC чевронекспанд</span><span class="sxs-lookup"><span data-stu-id="d9fcd-103">SMC\_CHEVRONEXPAND message</span></span>

<span data-ttu-id="d9fcd-104">Пользователь щелкнул Шеврон, чтобы развернуть элемент, указанный в соответствующей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="d9fcd-104">The user has clicked a chevron to expand the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a><span data-ttu-id="d9fcd-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9fcd-105">Parameters</span></span>

<span data-ttu-id="d9fcd-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="d9fcd-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9fcd-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9fcd-107">Return value</span></span>

<span data-ttu-id="d9fcd-108">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d9fcd-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9fcd-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9fcd-109">Remarks</span></span>

<span data-ttu-id="d9fcd-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="d9fcd-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9fcd-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d9fcd-111">Requirements</span></span>



| <span data-ttu-id="d9fcd-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d9fcd-112">Requirement</span></span> | <span data-ttu-id="d9fcd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d9fcd-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9fcd-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9fcd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d9fcd-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9fcd-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d9fcd-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9fcd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d9fcd-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9fcd-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9fcd-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9fcd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9fcd-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9fcd-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9fcd-120">IDL</span><span class="sxs-lookup"><span data-stu-id="d9fcd-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d9fcd-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d9fcd-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




