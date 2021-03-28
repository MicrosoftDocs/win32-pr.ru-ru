---
description: Уведомляет вас о инициализации полосы меню.
title: Сообщение SMC_INITMENU (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 415ee805-2b57-4f8f-85d9-2b38cd05998d
api_name:
- SMC_INITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ed7f7be1786192fb2be42f6d36cfb4bf222136fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265304"
---
# <a name="smc_initmenu-message"></a><span data-ttu-id="c2420-103">\_Сообщение SMC инитмену</span><span class="sxs-lookup"><span data-stu-id="c2420-103">SMC\_INITMENU message</span></span>

<span data-ttu-id="c2420-104">Уведомляет вас о инициализации полосы меню.</span><span class="sxs-lookup"><span data-stu-id="c2420-104">Notifies you to initialize the menu band.</span></span>


```C++
SMC_INITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="c2420-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2420-105">Parameters</span></span>

<span data-ttu-id="c2420-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="c2420-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2420-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2420-107">Return value</span></span>

<span data-ttu-id="c2420-108">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c2420-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2420-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2420-109">Remarks</span></span>

<span data-ttu-id="c2420-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="c2420-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2420-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c2420-111">Requirements</span></span>



| <span data-ttu-id="c2420-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c2420-112">Requirement</span></span> | <span data-ttu-id="c2420-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c2420-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2420-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2420-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c2420-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c2420-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2420-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2420-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c2420-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c2420-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2420-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c2420-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2420-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2420-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2420-120">IDL</span><span class="sxs-lookup"><span data-stu-id="c2420-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2420-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2420-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




