---
description: Задает или возвращает значение, которое управляет способом разрешения идентификатора безопасности (SID) пользователя в имена пользователей.
title: Дисккуотаконтрол. Усернамересолутион, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841465"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="a1c58-103">Дисккуотаконтрол. Усернамересолутион, свойство</span><span class="sxs-lookup"><span data-stu-id="a1c58-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="a1c58-104">Задает или возвращает значение, которое управляет способом разрешения идентификатора безопасности (SID) пользователя в имена пользователей.</span><span class="sxs-lookup"><span data-stu-id="a1c58-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="a1c58-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a1c58-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c58-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1c58-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="a1c58-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a1c58-107">Property value</span></span>

<span data-ttu-id="a1c58-108">Этому свойству можно присвоить одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a1c58-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="a1c58-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="a1c58-109">Resolution Type</span></span> | <span data-ttu-id="a1c58-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a1c58-110">Value</span></span> | <span data-ttu-id="a1c58-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a1c58-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c58-112">дкресолвеноне</span><span class="sxs-lookup"><span data-stu-id="a1c58-112">dqResolveNone</span></span>   | <span data-ttu-id="a1c58-113">0</span><span class="sxs-lookup"><span data-stu-id="a1c58-113">0</span></span>     | <span data-ttu-id="a1c58-114">Не разрешать сведения о имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1c58-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="a1c58-115">дкресолвесинк</span><span class="sxs-lookup"><span data-stu-id="a1c58-115">dqResolveSync</span></span>   | <span data-ttu-id="a1c58-116">1</span><span class="sxs-lookup"><span data-stu-id="a1c58-116">1</span></span>     | <span data-ttu-id="a1c58-117">Подождите, пока разрешаются сведения о имени.</span><span class="sxs-lookup"><span data-stu-id="a1c58-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="a1c58-118">дкресолвеасинк</span><span class="sxs-lookup"><span data-stu-id="a1c58-118">dqResolveAsync</span></span>  | <span data-ttu-id="a1c58-119">2</span><span class="sxs-lookup"><span data-stu-id="a1c58-119">2</span></span>     | <span data-ttu-id="a1c58-120">Не следует ждать при разрешении сведений о имени.</span><span class="sxs-lookup"><span data-stu-id="a1c58-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="a1c58-121">Событие [**онусернамечанжед**](diskquotacontrol-onusernamechanged.md) срабатывает при разрешении имени.</span><span class="sxs-lookup"><span data-stu-id="a1c58-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a1c58-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="a1c58-122">Remarks</span></span>

<span data-ttu-id="a1c58-123">Это свойство влияет на перечисление объектов [**дидисккуотаусер**](didiskquotauser-object.md) , а также на методы [**adduser**](diskquotacontrol-adduser.md) и [**финдусер**](diskquotacontrol-finduser.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c58-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1c58-124">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="a1c58-124">Requirements</span></span>



| <span data-ttu-id="a1c58-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a1c58-125">Requirement</span></span> | <span data-ttu-id="a1c58-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a1c58-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c58-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1c58-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a1c58-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1c58-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1c58-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1c58-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a1c58-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1c58-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a1c58-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a1c58-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1c58-132"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a1c58-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1c58-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1c58-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c58-134">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="a1c58-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




