---
description: Запрашивает сведения об элементе меню папки оболочки.
title: Сообщение SMC_GETSFINFO (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3a02b61565eb08f623978900d6ce47e30eea85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997786"
---
# <a name="smc_getsfinfo-message"></a><span data-ttu-id="b5a69-103">\_Сообщение SMC жетсфинфо</span><span class="sxs-lookup"><span data-stu-id="b5a69-103">SMC\_GETSFINFO message</span></span>

<span data-ttu-id="b5a69-104">Запрашивает сведения об элементе меню папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="b5a69-104">Requests information about a Shell folder menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="b5a69-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5a69-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a69-106">*псминфо*</span><span class="sxs-lookup"><span data-stu-id="b5a69-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a69-107">Указатель на структуру [**сминфо**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) .</span><span class="sxs-lookup"><span data-stu-id="b5a69-107">Pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="b5a69-108">Заполните структуру соответствующей информацией и возвратите значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b5a69-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a69-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5a69-109">Return value</span></span>

<span data-ttu-id="b5a69-110">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b5a69-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5a69-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5a69-111">Remarks</span></span>

<span data-ttu-id="b5a69-112">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="b5a69-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a69-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b5a69-113">Requirements</span></span>



| <span data-ttu-id="b5a69-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b5a69-114">Requirement</span></span> | <span data-ttu-id="b5a69-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b5a69-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a69-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5a69-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a69-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5a69-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b5a69-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5a69-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a69-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5a69-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5a69-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b5a69-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5a69-121"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5a69-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5a69-122">IDL</span><span class="sxs-lookup"><span data-stu-id="b5a69-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5a69-123"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5a69-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




