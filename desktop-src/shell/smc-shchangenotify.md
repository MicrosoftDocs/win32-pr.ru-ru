---
description: Уведомляет о том, что произошло изменение.
title: Сообщение SMC_SHCHANGENOTIFY (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 258a885ddaf61b45df1cfff9f9c77ce37a233dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985561"
---
# <a name="smc_shchangenotify-message"></a><span data-ttu-id="7b075-103">\_Сообщение SMC шчанженотифи</span><span class="sxs-lookup"><span data-stu-id="7b075-103">SMC\_SHCHANGENOTIFY message</span></span>

<span data-ttu-id="7b075-104">Уведомляет о том, что произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="7b075-104">Notifies you that a change has taken place.</span></span>


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a><span data-ttu-id="7b075-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b075-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b075-106">*псмк*</span><span class="sxs-lookup"><span data-stu-id="7b075-106">*psmc*</span></span> 
</dt> <dd>

<span data-ttu-id="7b075-107">Указатель на структуру [**смкшчанженотифиструкт**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) со сведениями об изменении.</span><span class="sxs-lookup"><span data-stu-id="7b075-107">A pointer to an [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) structure with information on the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b075-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b075-108">Return value</span></span>

<span data-ttu-id="7b075-109">Возвратите \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7b075-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b075-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b075-110">Remarks</span></span>

<span data-ttu-id="7b075-111">Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="7b075-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b075-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7b075-112">Requirements</span></span>



| <span data-ttu-id="7b075-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7b075-113">Requirement</span></span> | <span data-ttu-id="7b075-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7b075-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b075-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b075-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7b075-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b075-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b075-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b075-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7b075-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b075-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b075-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7b075-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b075-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b075-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b075-121">IDL</span><span class="sxs-lookup"><span data-stu-id="7b075-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b075-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b075-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




