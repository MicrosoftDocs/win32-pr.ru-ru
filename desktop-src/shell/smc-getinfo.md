---
description: Запрашивает сведения о обычном элементе меню.
title: Сообщение SMC_GETINFO (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f60c1581ae7c4585de48eea943cc23b4d87fa4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997787"
---
# <a name="smc_getinfo-message"></a><span data-ttu-id="4fb17-103">\_Сообщение SMC info</span><span class="sxs-lookup"><span data-stu-id="4fb17-103">SMC\_GETINFO message</span></span>

<span data-ttu-id="4fb17-104">Запрашивает сведения о обычном элементе меню.</span><span class="sxs-lookup"><span data-stu-id="4fb17-104">Requests information about a regular menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="4fb17-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fb17-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb17-106">*псминфо*</span><span class="sxs-lookup"><span data-stu-id="4fb17-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4fb17-107">Указатель на структуру [**сминфо**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) .</span><span class="sxs-lookup"><span data-stu-id="4fb17-107">A pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="4fb17-108">Заполните структуру соответствующей информацией и возвратите значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4fb17-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fb17-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fb17-109">Return value</span></span>

<span data-ttu-id="4fb17-110">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4fb17-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fb17-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="4fb17-111">Remarks</span></span>

<span data-ttu-id="4fb17-112">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="4fb17-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb17-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4fb17-113">Requirements</span></span>



| <span data-ttu-id="4fb17-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4fb17-114">Requirement</span></span> | <span data-ttu-id="4fb17-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4fb17-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb17-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fb17-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb17-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4fb17-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4fb17-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fb17-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb17-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4fb17-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4fb17-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4fb17-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fb17-121"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb17-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fb17-122">IDL</span><span class="sxs-lookup"><span data-stu-id="4fb17-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fb17-123"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fb17-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




