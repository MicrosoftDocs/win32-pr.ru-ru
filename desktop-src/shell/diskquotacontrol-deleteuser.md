---
description: Удаляет пользователя из тома.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Дисккуотаконтрол. Делетеусер, метод (Дсккуота. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262905"
---
# <a name="diskquotacontroldeleteuser-method"></a><span data-ttu-id="36c45-103">Дисккуотаконтрол. Делетеусер, метод</span><span class="sxs-lookup"><span data-stu-id="36c45-103">DiskQuotaControl.DeleteUser method</span></span>

<span data-ttu-id="36c45-104">Удаляет пользователя из тома.</span><span class="sxs-lookup"><span data-stu-id="36c45-104">Deletes a user from the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c45-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36c45-105">Syntax</span></span>


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="36c45-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36c45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36c45-107">*аусер*</span><span class="sxs-lookup"><span data-stu-id="36c45-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="36c45-108">Тип: **объект**</span><span class="sxs-lookup"><span data-stu-id="36c45-108">Type: **Object**</span></span>

<span data-ttu-id="36c45-109">Выражение объекта, результатом которого является объект [**дидисккуотаусер**](didiskquotauser-object.md) пользователя.</span><span class="sxs-lookup"><span data-stu-id="36c45-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36c45-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36c45-110">Return value</span></span>

<span data-ttu-id="36c45-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="36c45-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c45-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="36c45-112">Remarks</span></span>

<span data-ttu-id="36c45-113">Этот метод завершается сбоем, если пользователь владеет любым хранилищем на томе.</span><span class="sxs-lookup"><span data-stu-id="36c45-113">This method fails if the user owns any storage on the volume.</span></span> <span data-ttu-id="36c45-114">Перед удалением пользователя из тома необходимо удалить все хранилища для этого пользователя, переместить его на другой том или передать его владение другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="36c45-114">Before you delete a user from a volume, all storage for that user must be deleted, be moved to another volume, or have its ownership transferred to another user.</span></span>

## <a name="requirements"></a><span data-ttu-id="36c45-115">Требования</span><span class="sxs-lookup"><span data-stu-id="36c45-115">Requirements</span></span>



| <span data-ttu-id="36c45-116">Требование</span><span class="sxs-lookup"><span data-stu-id="36c45-116">Requirement</span></span> | <span data-ttu-id="36c45-117">Значение</span><span class="sxs-lookup"><span data-stu-id="36c45-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36c45-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36c45-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36c45-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36c45-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36c45-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36c45-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36c45-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36c45-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="36c45-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36c45-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36c45-123"><dt>Дсккуота. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c45-123"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="36c45-124">DLL</span><span class="sxs-lookup"><span data-stu-id="36c45-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36c45-125"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="36c45-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c45-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36c45-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c45-127">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="36c45-127">**AddUser**</span></span>](diskquotacontrol-adduser.md)
</dt> <dt>

[<span data-ttu-id="36c45-128">**дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="36c45-128">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




