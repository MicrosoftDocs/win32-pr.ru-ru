---
description: Помещает указанный объект пользователя в строке для разрешения имен.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Дисккуотаконтрол. Гивеусернамересолутионприорити, метод (Дсккуота. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540466"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a><span data-ttu-id="6313f-103">Дисккуотаконтрол. Гивеусернамересолутионприорити, метод</span><span class="sxs-lookup"><span data-stu-id="6313f-103">DiskQuotaControl.GiveUserNameResolutionPriority method</span></span>

<span data-ttu-id="6313f-104">Помещает указанный объект пользователя в строке для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="6313f-104">Places the specified user object next in line for name resolution.</span></span>

## <a name="syntax"></a><span data-ttu-id="6313f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6313f-105">Syntax</span></span>


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="6313f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6313f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6313f-107">*аусер*</span><span class="sxs-lookup"><span data-stu-id="6313f-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="6313f-108">Тип: **объект**</span><span class="sxs-lookup"><span data-stu-id="6313f-108">Type: **Object**</span></span>

<span data-ttu-id="6313f-109">Выражение объекта, результатом которого является объект [**дидисккуотаусер**](didiskquotauser-object.md) пользователя.</span><span class="sxs-lookup"><span data-stu-id="6313f-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6313f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6313f-110">Return value</span></span>

<span data-ttu-id="6313f-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6313f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6313f-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="6313f-112">Remarks</span></span>

<span data-ttu-id="6313f-113">Если включено асинхронное разрешение имен, объекты пользователя помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="6313f-113">If asynchronous name resolution is enabled, user objects are placed in a queue.</span></span> <span data-ttu-id="6313f-114">По умолчанию они обслуживаются в том порядке, в котором они размещены в очереди.</span><span class="sxs-lookup"><span data-stu-id="6313f-114">By default, they are serviced in the order they are placed in the queue.</span></span> <span data-ttu-id="6313f-115">Метод **гивеусернамересолутионприорити** перемещает объект на передний план, чтобы он находящихся рядом в строке для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6313f-115">The **GiveUserNameResolutionPriority** method moves an object to the front of the queue so that it is next in line to be serviced.</span></span>

<span data-ttu-id="6313f-116">Чтобы включить асинхронное разрешение имен, используйте свойство [**усернамересолутион**](diskquotacontrol-usernameresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="6313f-116">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to enable asynchronous name resolution.</span></span>

## <a name="requirements"></a><span data-ttu-id="6313f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6313f-117">Requirements</span></span>



| <span data-ttu-id="6313f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6313f-118">Requirement</span></span> | <span data-ttu-id="6313f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6313f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6313f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6313f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6313f-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6313f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6313f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6313f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6313f-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6313f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6313f-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6313f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6313f-125"><dt>Дсккуота. h</dt></span><span class="sxs-lookup"><span data-stu-id="6313f-125"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="6313f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6313f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6313f-127"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6313f-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6313f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6313f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6313f-129">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="6313f-129">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




