---
description: Запрашивает возможность удаления объекта данных в элементе, указанном сопутствующей структурой СМДАТА.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Сообщение SMC_SFDDRESTRICTED (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985733"
---
# <a name="smc_sfddrestricted-message"></a><span data-ttu-id="e2538-103">\_Сообщение SMC сфддрестриктед</span><span class="sxs-lookup"><span data-stu-id="e2538-103">SMC\_SFDDRESTRICTED message</span></span>

<span data-ttu-id="e2538-104">Запрашивает возможность удаления объекта данных в элементе, указанном сопутствующей структурой [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="e2538-104">Requests whether it is acceptable to drop a data object on the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a><span data-ttu-id="e2538-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2538-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2538-106">*пдроптаржет*</span><span class="sxs-lookup"><span data-stu-id="e2538-106">*pDropTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="e2538-107">Адрес указателя void, который получает указатель на интерфейс [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="e2538-107">The address of a void pointer that receives a pointer to your [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span> <span data-ttu-id="e2538-108">Если вы не хотите принимать объект данных, присвойте этому параметру значение **null** .</span><span class="sxs-lookup"><span data-stu-id="e2538-108">Set this value to **NULL** if you do not want to accept the data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2538-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2538-109">Return value</span></span>

<span data-ttu-id="e2538-110">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e2538-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2538-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2538-111">Remarks</span></span>

<span data-ttu-id="e2538-112">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="e2538-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2538-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e2538-113">Requirements</span></span>



| <span data-ttu-id="e2538-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e2538-114">Requirement</span></span> | <span data-ttu-id="e2538-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e2538-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2538-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2538-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2538-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e2538-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e2538-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2538-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2538-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e2538-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2538-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e2538-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2538-121"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2538-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2538-122">IDL</span><span class="sxs-lookup"><span data-stu-id="e2538-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2538-123"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2538-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
