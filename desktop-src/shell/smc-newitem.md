---
description: Уведомляет вас о новом элементе, как указано в сопутствующей структуре СМДАТА.
title: Сообщение SMC_NEWITEM (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e0ccf2db-cb46-469f-bc08-4b5100a410ba
api_name:
- SMC_NEWITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ebd8f1b6454a2fb592374b860811ebfc7a14f09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985740"
---
# <a name="smc_newitem-message"></a><span data-ttu-id="6d447-103">Сообщение о неsmc \_ NEWITEM</span><span class="sxs-lookup"><span data-stu-id="6d447-103">SMC\_NEWITEM message</span></span>

<span data-ttu-id="6d447-104">Уведомляет вас о новом элементе, как указано в сопутствующей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="6d447-104">Notifies you of a new item, as specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_NEWITEM
            
```



## <a name="parameters"></a><span data-ttu-id="6d447-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d447-105">Parameters</span></span>

<span data-ttu-id="6d447-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="6d447-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d447-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d447-107">Return value</span></span>

<span data-ttu-id="6d447-108">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6d447-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d447-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d447-109">Remarks</span></span>

<span data-ttu-id="6d447-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="6d447-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d447-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6d447-111">Requirements</span></span>



| <span data-ttu-id="6d447-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6d447-112">Requirement</span></span> | <span data-ttu-id="6d447-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6d447-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d447-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d447-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6d447-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d447-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d447-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d447-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6d447-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d447-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d447-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6d447-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d447-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d447-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d447-120">IDL</span><span class="sxs-lookup"><span data-stu-id="6d447-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d447-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d447-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




