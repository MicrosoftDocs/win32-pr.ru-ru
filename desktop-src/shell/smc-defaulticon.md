---
description: Возвращает значок по умолчанию для элемента, указанного сопутствующей структурой СМДАТА.
title: Сообщение SMC_DEFAULTICON (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10edab26c87dae4b1c9d2d5f06390fc608ba1edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997794"
---
# <a name="smc_defaulticon-message"></a><span data-ttu-id="42a69-103">\_Сообщение SMC дефаултикон</span><span class="sxs-lookup"><span data-stu-id="42a69-103">SMC\_DEFAULTICON message</span></span>

<span data-ttu-id="42a69-104">Возвращает значок по умолчанию для элемента, указанного сопутствующей структурой [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="42a69-104">Return the default icon for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a><span data-ttu-id="42a69-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="42a69-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a69-106">*пвсзикон*</span><span class="sxs-lookup"><span data-stu-id="42a69-106">*pwszIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="42a69-107">Указатель на строку, которая получает полный путь к файлу, содержащему значок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42a69-107">A pointer to a string that receives the fully qualified path of the file that contains the default icon.</span></span>

</dd> <dt>

<span data-ttu-id="42a69-108">*iIcon*</span><span class="sxs-lookup"><span data-stu-id="42a69-108">*iIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="42a69-109">Указатель на целое число, которое получает индекс значка в файле, указанном параметром *пвсзикон*.</span><span class="sxs-lookup"><span data-stu-id="42a69-109">A pointer to an integer that receives the index of the icon in the file specified by *pwszIcon*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a69-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42a69-110">Return value</span></span>

<span data-ttu-id="42a69-111">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="42a69-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a69-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="42a69-112">Remarks</span></span>

<span data-ttu-id="42a69-113">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="42a69-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a69-114">Требования</span><span class="sxs-lookup"><span data-stu-id="42a69-114">Requirements</span></span>



| <span data-ttu-id="42a69-115">Требование</span><span class="sxs-lookup"><span data-stu-id="42a69-115">Requirement</span></span> | <span data-ttu-id="42a69-116">Значение</span><span class="sxs-lookup"><span data-stu-id="42a69-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42a69-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42a69-117">Minimum supported client</span></span><br/> | <span data-ttu-id="42a69-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42a69-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="42a69-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42a69-119">Minimum supported server</span></span><br/> | <span data-ttu-id="42a69-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42a69-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="42a69-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="42a69-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a69-122"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a69-122"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="42a69-123">IDL</span><span class="sxs-lookup"><span data-stu-id="42a69-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42a69-124"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42a69-124"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




