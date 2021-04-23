---
description: Уведомляет о создании строки меню.
title: Сообщение SMC_CREATE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 59219f376288431fa20e198d8c427ff40c7fba62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997799"
---
# <a name="smc_create-message"></a><span data-ttu-id="65e04-103">SMC \_ Создание сообщения</span><span class="sxs-lookup"><span data-stu-id="65e04-103">SMC\_CREATE message</span></span>

<span data-ttu-id="65e04-104">Уведомляет о создании строки меню.</span><span class="sxs-lookup"><span data-stu-id="65e04-104">Notifies you that a menu band has been created.</span></span>


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a><span data-ttu-id="65e04-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="65e04-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65e04-106">*псмд*</span><span class="sxs-lookup"><span data-stu-id="65e04-106">*psmd*</span></span> 
</dt> <dd>

<span data-ttu-id="65e04-107">Указатель на элемент **пвусердата** структуры [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="65e04-107">A pointer to the **pvUserData** member of an [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65e04-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65e04-108">Return value</span></span>

<span data-ttu-id="65e04-109">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="65e04-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="65e04-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="65e04-110">Remarks</span></span>

<span data-ttu-id="65e04-111">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="65e04-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e04-112">Требования</span><span class="sxs-lookup"><span data-stu-id="65e04-112">Requirements</span></span>



| <span data-ttu-id="65e04-113">Требование</span><span class="sxs-lookup"><span data-stu-id="65e04-113">Requirement</span></span> | <span data-ttu-id="65e04-114">Значение</span><span class="sxs-lookup"><span data-stu-id="65e04-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65e04-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65e04-115">Minimum supported client</span></span><br/> | <span data-ttu-id="65e04-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65e04-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65e04-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65e04-117">Minimum supported server</span></span><br/> | <span data-ttu-id="65e04-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65e04-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65e04-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="65e04-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="65e04-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65e04-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="65e04-121">IDL</span><span class="sxs-lookup"><span data-stu-id="65e04-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65e04-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65e04-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




