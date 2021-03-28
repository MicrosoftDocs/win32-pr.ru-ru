---
description: Выполните элемент папки оболочки, указанный в сопутствующей структуре СМДАТА.
title: Сообщение SMC_SFEXEC (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b4e414cd7dab9968882272b19b9b21b95da0f1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985732"
---
# <a name="smc_sfexec-message"></a><span data-ttu-id="e09dd-103">\_Сообщение SMC сфексек</span><span class="sxs-lookup"><span data-stu-id="e09dd-103">SMC\_SFEXEC message</span></span>

<span data-ttu-id="e09dd-104">Выполните элемент папки оболочки, указанный в сопутствующей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="e09dd-104">Execute the Shell folder item specified in the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFEXEC
            
```



## <a name="parameters"></a><span data-ttu-id="e09dd-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="e09dd-105">Parameters</span></span>

<span data-ttu-id="e09dd-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="e09dd-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e09dd-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e09dd-107">Return value</span></span>

<span data-ttu-id="e09dd-108">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e09dd-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e09dd-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="e09dd-109">Remarks</span></span>

<span data-ttu-id="e09dd-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="e09dd-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e09dd-111">Требования</span><span class="sxs-lookup"><span data-stu-id="e09dd-111">Requirements</span></span>



| <span data-ttu-id="e09dd-112">Требование</span><span class="sxs-lookup"><span data-stu-id="e09dd-112">Requirement</span></span> | <span data-ttu-id="e09dd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e09dd-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e09dd-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e09dd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e09dd-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e09dd-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e09dd-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e09dd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e09dd-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e09dd-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e09dd-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e09dd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e09dd-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e09dd-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="e09dd-120">IDL</span><span class="sxs-lookup"><span data-stu-id="e09dd-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e09dd-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e09dd-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




