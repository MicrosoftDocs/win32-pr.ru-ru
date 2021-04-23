---
description: Понизить элемент, указанный в сопровождающей структуре СМДАТА.
title: Сообщение SMC_DEMOTE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 46e5505571402feec24d81a9184b713e1c61ae0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997795"
---
# <a name="smc_demote-message"></a><span data-ttu-id="7b896-103">SMC \_ понизить сообщение</span><span class="sxs-lookup"><span data-stu-id="7b896-103">SMC\_DEMOTE message</span></span>

<span data-ttu-id="7b896-104">Понизить элемент, указанный в сопровождающей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="7b896-104">Demote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a><span data-ttu-id="7b896-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b896-105">Parameters</span></span>

<span data-ttu-id="7b896-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="7b896-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b896-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b896-107">Return value</span></span>

<span data-ttu-id="7b896-108">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7b896-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b896-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b896-109">Remarks</span></span>

<span data-ttu-id="7b896-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="7b896-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b896-111">Требования</span><span class="sxs-lookup"><span data-stu-id="7b896-111">Requirements</span></span>



| <span data-ttu-id="7b896-112">Требование</span><span class="sxs-lookup"><span data-stu-id="7b896-112">Requirement</span></span> | <span data-ttu-id="7b896-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7b896-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b896-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b896-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7b896-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b896-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b896-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b896-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7b896-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b896-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b896-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7b896-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b896-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b896-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b896-120">IDL</span><span class="sxs-lookup"><span data-stu-id="7b896-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b896-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b896-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




