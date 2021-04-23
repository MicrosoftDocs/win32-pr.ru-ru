---
description: Уведомляет о сохранении переданного объекта.
title: Сообщение SMC_SETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265303"
---
# <a name="smc_setsfobject-message"></a><span data-ttu-id="28af0-103">\_Сообщение SMC сетсфобжект</span><span class="sxs-lookup"><span data-stu-id="28af0-103">SMC\_SETSFOBJECT message</span></span>

<span data-ttu-id="28af0-104">Уведомляет о сохранении переданного объекта.</span><span class="sxs-lookup"><span data-stu-id="28af0-104">Notifies you to save the passed object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="28af0-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="28af0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28af0-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="28af0-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="28af0-107">IID, связанный с объектом.</span><span class="sxs-lookup"><span data-stu-id="28af0-107">The IID associated with the object.</span></span>

</dd> <dt>

<span data-ttu-id="28af0-108">*PV*</span><span class="sxs-lookup"><span data-stu-id="28af0-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="28af0-109">Указатель интерфейса на объект, указанный с помощью *IID*.</span><span class="sxs-lookup"><span data-stu-id="28af0-109">A pointer the interface on the object specified by *iid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28af0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28af0-110">Return value</span></span>

<span data-ttu-id="28af0-111">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="28af0-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="28af0-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="28af0-112">Remarks</span></span>

<span data-ttu-id="28af0-113">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="28af0-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

<span data-ttu-id="28af0-114">Уведомление **SMC \_ сетсфобжект** используется с \_ потоком IID.</span><span class="sxs-lookup"><span data-stu-id="28af0-114">The **SMC\_SETSFOBJECT** notification is used with IID\_Stream.</span></span> <span data-ttu-id="28af0-115">Объект сохраняется в сохраненном виде в реестре и не выполняется с счетчиком ссылок на объект, переданный в.</span><span class="sxs-lookup"><span data-stu-id="28af0-115">The object is saved into a persisted form in the registry and nothing is done with the reference count on the object passed in.</span></span>

## <a name="requirements"></a><span data-ttu-id="28af0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="28af0-116">Requirements</span></span>



| <span data-ttu-id="28af0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="28af0-117">Requirement</span></span> | <span data-ttu-id="28af0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="28af0-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28af0-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28af0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="28af0-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28af0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="28af0-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28af0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="28af0-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28af0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28af0-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="28af0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="28af0-124"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28af0-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="28af0-125">IDL</span><span class="sxs-lookup"><span data-stu-id="28af0-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28af0-126"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28af0-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




