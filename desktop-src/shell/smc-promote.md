---
description: Повышение уровня элемента, указанного сопутствующей структурой СМДАТА.
title: Сообщение SMC_PROMOTE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b1208673-06b4-42b2-b4ac-872fd22927df
api_name:
- SMC_PROMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 22718e51d6ef1bf7e3c5652741b95cadb4db9937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985736"
---
# <a name="smc_promote-message"></a><span data-ttu-id="a251f-103">SMC \_ продвижение сообщения</span><span class="sxs-lookup"><span data-stu-id="a251f-103">SMC\_PROMOTE message</span></span>

<span data-ttu-id="a251f-104">Повышение уровня элемента, указанного сопутствующей структурой [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="a251f-104">Promote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_PROMOTE
```



## <a name="parameters"></a><span data-ttu-id="a251f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a251f-105">Parameters</span></span>

<span data-ttu-id="a251f-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="a251f-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a251f-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a251f-107">Return value</span></span>

<span data-ttu-id="a251f-108">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a251f-108">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a251f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="a251f-109">Remarks</span></span>

<span data-ttu-id="a251f-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="a251f-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a251f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a251f-111">Requirements</span></span>



| <span data-ttu-id="a251f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a251f-112">Requirement</span></span> | <span data-ttu-id="a251f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a251f-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a251f-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a251f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a251f-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a251f-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a251f-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a251f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a251f-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a251f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a251f-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a251f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a251f-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a251f-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="a251f-120">IDL</span><span class="sxs-lookup"><span data-stu-id="a251f-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a251f-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a251f-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




