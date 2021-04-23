---
description: Сообщает, что меню является свертыванием.
title: Сообщение SMC_EXITMENU (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 868b4819-1dbf-497a-9c79-5935f503969a
api_name:
- SMC_EXITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9a8680617a17ce0069a8633e1c70ff6b32a4be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998844"
---
# <a name="smc_exitmenu-message"></a><span data-ttu-id="9e564-103">\_Сообщение SMC екситмену</span><span class="sxs-lookup"><span data-stu-id="9e564-103">SMC\_EXITMENU message</span></span>

<span data-ttu-id="9e564-104">Сообщает, что меню является свертыванием.</span><span class="sxs-lookup"><span data-stu-id="9e564-104">Notifies you that the menu is collapsing.</span></span>


```C++
SMC_EXITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="9e564-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e564-105">Parameters</span></span>

<span data-ttu-id="9e564-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="9e564-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e564-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e564-107">Return value</span></span>

<span data-ttu-id="9e564-108">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9e564-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e564-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e564-109">Remarks</span></span>

<span data-ttu-id="9e564-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="9e564-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e564-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9e564-111">Requirements</span></span>



| <span data-ttu-id="9e564-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9e564-112">Requirement</span></span> | <span data-ttu-id="9e564-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9e564-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e564-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e564-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9e564-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e564-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9e564-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e564-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9e564-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e564-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9e564-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9e564-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e564-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e564-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e564-120">IDL</span><span class="sxs-lookup"><span data-stu-id="9e564-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e564-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e564-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




