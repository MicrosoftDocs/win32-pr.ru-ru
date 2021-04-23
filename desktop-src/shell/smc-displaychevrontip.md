---
description: Уведомляет о том, что всплывающая подсказка будет отображаться для шеврона, связанного с элементом, указанным в сопровождающей структуре СМДАТА.
title: Сообщение SMC_DISPLAYCHEVRONTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497883"
---
# <a name="smc_displaychevrontip-message"></a><span data-ttu-id="04a5d-103">\_Сообщение SMC дисплайчевронтип</span><span class="sxs-lookup"><span data-stu-id="04a5d-103">SMC\_DISPLAYCHEVRONTIP message</span></span>

<span data-ttu-id="04a5d-104">Уведомляет о том, что всплывающая подсказка будет отображаться для шеврона, связанного с элементом, указанным в сопровождающей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="04a5d-104">Notifies you that an infotip is about to be displayed for the chevron associated with the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a><span data-ttu-id="04a5d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="04a5d-105">Parameters</span></span>

<span data-ttu-id="04a5d-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="04a5d-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04a5d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04a5d-107">Return value</span></span>

<span data-ttu-id="04a5d-108">Возвратите \_ ОК, чтобы отобразить всплывающую подсказку.</span><span class="sxs-lookup"><span data-stu-id="04a5d-108">Return S\_OK to display the infotip.</span></span> <span data-ttu-id="04a5d-109">Возвращает \_ значение false, чтобы предотвратить отображение подсказки.</span><span class="sxs-lookup"><span data-stu-id="04a5d-109">Return S\_FALSE to prevent the infotip from being displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a5d-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="04a5d-110">Remarks</span></span>

<span data-ttu-id="04a5d-111">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="04a5d-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a5d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="04a5d-112">Requirements</span></span>



| <span data-ttu-id="04a5d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="04a5d-113">Requirement</span></span> | <span data-ttu-id="04a5d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="04a5d-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04a5d-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04a5d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="04a5d-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="04a5d-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="04a5d-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04a5d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="04a5d-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="04a5d-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04a5d-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="04a5d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="04a5d-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a5d-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="04a5d-121">IDL</span><span class="sxs-lookup"><span data-stu-id="04a5d-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04a5d-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04a5d-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




