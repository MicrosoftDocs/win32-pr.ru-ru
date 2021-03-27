---
description: Уведомляет панель приложений, когда полноэкранное приложение открывается или закрывается. Это уведомление отправляется в виде определяемого приложением сообщения, которое задается \_ новым сообщением АБМ.
title: Сообщение ABN_FULLSCREENAPP (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143990"
---
# <a name="abn_fullscreenapp-message"></a><span data-ttu-id="98fd2-104">\_Сообщение АБН фуллскринапп</span><span class="sxs-lookup"><span data-stu-id="98fd2-104">ABN\_FULLSCREENAPP message</span></span>

<span data-ttu-id="98fd2-105">Уведомляет панель приложений, когда полноэкранное приложение открывается или закрывается.</span><span class="sxs-lookup"><span data-stu-id="98fd2-105">Notifies an appbar when a full-screen application is opening or closing.</span></span> <span data-ttu-id="98fd2-106">Это уведомление отправляется в виде определяемого приложением сообщения, которое задается новым сообщением [**АБМ \_**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="98fd2-106">This notification is sent in the form of an application-defined message that is set by the [**ABM\_NEW**](abm-new.md) message.</span></span>


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a><span data-ttu-id="98fd2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="98fd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98fd2-108">*fOpen*</span><span class="sxs-lookup"><span data-stu-id="98fd2-108">*fOpen*</span></span> 
</dt> <dd>

<span data-ttu-id="98fd2-109">Флаг, указывающий, будет ли полноэкранное приложение открываться или закрываться.</span><span class="sxs-lookup"><span data-stu-id="98fd2-109">A flag specifying whether a full-screen application is opening or closing.</span></span> <span data-ttu-id="98fd2-110">Этот параметр имеет **значение true** , если приложение открывается, или **значение false** , если оно закрывается.</span><span class="sxs-lookup"><span data-stu-id="98fd2-110">This parameter is **TRUE** if the application is opening or **FALSE** if it is closing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98fd2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98fd2-111">Return value</span></span>

<span data-ttu-id="98fd2-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="98fd2-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98fd2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="98fd2-113">Remarks</span></span>

<span data-ttu-id="98fd2-114">При открытии полноэкранного приложения панель приложений должен быть направлен в нижнюю часть z-порядка.</span><span class="sxs-lookup"><span data-stu-id="98fd2-114">When a full-screen application is opening, an appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="98fd2-115">Когда он закрывается, панель приложений должен восстановить свою координату z-порядка.</span><span class="sxs-lookup"><span data-stu-id="98fd2-115">When it is closing, the appbar should restore its z-order position.</span></span>

## <a name="requirements"></a><span data-ttu-id="98fd2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="98fd2-116">Requirements</span></span>



| <span data-ttu-id="98fd2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="98fd2-117">Requirement</span></span> | <span data-ttu-id="98fd2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="98fd2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98fd2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98fd2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98fd2-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="98fd2-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="98fd2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98fd2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98fd2-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98fd2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98fd2-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="98fd2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98fd2-124"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="98fd2-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




