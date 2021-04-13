---
description: Пользователь выбрал элемент, указанный в сопровождающей структуре СМДАТА.
title: Сообщение SMC_SFSELECTITEM (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 82c3dfca-98a8-43ca-bebc-85bfdf640d38
api_name:
- SMC_SFSELECTITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cfb3384fcfff73d264d21c53a91ede554cc7da5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985564"
---
# <a name="smc_sfselectitem-message"></a><span data-ttu-id="07939-103">\_Сообщение SMC сфселектитем</span><span class="sxs-lookup"><span data-stu-id="07939-103">SMC\_SFSELECTITEM message</span></span>

<span data-ttu-id="07939-104">Пользователь выбрал элемент, указанный в сопровождающей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="07939-104">The user has selected the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFSELECTITEM
            
```



## <a name="parameters"></a><span data-ttu-id="07939-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="07939-105">Parameters</span></span>

<span data-ttu-id="07939-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="07939-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07939-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07939-107">Return value</span></span>

<span data-ttu-id="07939-108">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="07939-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="07939-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="07939-109">Remarks</span></span>

<span data-ttu-id="07939-110">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="07939-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07939-111">Требования</span><span class="sxs-lookup"><span data-stu-id="07939-111">Requirements</span></span>



| <span data-ttu-id="07939-112">Требование</span><span class="sxs-lookup"><span data-stu-id="07939-112">Requirement</span></span> | <span data-ttu-id="07939-113">Значение</span><span class="sxs-lookup"><span data-stu-id="07939-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07939-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07939-114">Minimum supported client</span></span><br/> | <span data-ttu-id="07939-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07939-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="07939-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07939-116">Minimum supported server</span></span><br/> | <span data-ttu-id="07939-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07939-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07939-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="07939-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="07939-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07939-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="07939-120">IDL</span><span class="sxs-lookup"><span data-stu-id="07939-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07939-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="07939-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




