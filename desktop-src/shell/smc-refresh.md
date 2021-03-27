---
description: Отправляет уведомление о том, что меню полностью Обновлено, и вы можете сбросить состояние.
title: Сообщение SMC_REFRESH (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aab18245c6502d4d3424e6ed6727eceb5a329d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911156"
---
# <a name="smc_refresh-message"></a><span data-ttu-id="69e0e-103">\_Сообщение об обновлении SMC</span><span class="sxs-lookup"><span data-stu-id="69e0e-103">SMC\_REFRESH message</span></span>

<span data-ttu-id="69e0e-104">Отправляет уведомление о том, что меню полностью Обновлено, и вы можете сбросить состояние.</span><span class="sxs-lookup"><span data-stu-id="69e0e-104">Sends notification that the menus have completely refreshed and you can reset your state.</span></span>


```C++
SMC_REFRESH
            
```



## <a name="parameters"></a><span data-ttu-id="69e0e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="69e0e-105">Parameters</span></span>

<span data-ttu-id="69e0e-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="69e0e-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69e0e-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69e0e-107">Return value</span></span>

<span data-ttu-id="69e0e-108">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="69e0e-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="69e0e-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="69e0e-109">Remarks</span></span>

<span data-ttu-id="69e0e-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="69e0e-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e0e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="69e0e-111">Requirements</span></span>



| <span data-ttu-id="69e0e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="69e0e-112">Requirement</span></span> | <span data-ttu-id="69e0e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="69e0e-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69e0e-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69e0e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="69e0e-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="69e0e-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="69e0e-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69e0e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="69e0e-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="69e0e-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69e0e-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="69e0e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="69e0e-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69e0e-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="69e0e-120">IDL</span><span class="sxs-lookup"><span data-stu-id="69e0e-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="69e0e-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="69e0e-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




