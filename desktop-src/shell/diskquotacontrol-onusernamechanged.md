---
description: Происходит при разрешении сведений об имени для объекта Дидисккуотаусер.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Функция Онусернамечанжед (Дсккуота. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346435"
---
# <a name="onusernamechanged-function"></a><span data-ttu-id="b9d4b-103">Функция Онусернамечанжед</span><span class="sxs-lookup"><span data-stu-id="b9d4b-103">OnUserNameChanged function</span></span>

<span data-ttu-id="b9d4b-104">Происходит при разрешении сведений об имени для объекта [**дидисккуотаусер**](didiskquotauser-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b9d4b-104">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9d4b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9d4b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d4b-106">*аусер*</span><span class="sxs-lookup"><span data-stu-id="b9d4b-106">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d4b-107">**Объект** , результатом которого является объект [**дидисккуотаусер**](didiskquotauser-object.md) , связанный с пользователем, имя которого было разрешено.</span><span class="sxs-lookup"><span data-stu-id="b9d4b-107">The **Object** that evaluates to the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the user whose name has been resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9d4b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9d4b-108">Return value</span></span>

<span data-ttu-id="b9d4b-109">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b9d4b-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d4b-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9d4b-110">Remarks</span></span>

<span data-ttu-id="b9d4b-111">Когда клиент [**перечисляет пользователей**](didiskquotauser-object.md)или вызывает метод [**adduser**](diskquotacontrol-adduser.md) или [**финдусер**](diskquotacontrol-finduser.md) , имя пользователя должно быть разрешено соответствующему идентификатору безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="b9d4b-111">When a client [**enumerates users**](didiskquotauser-object.md), or calls the [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md) method, the user name must be resolved to the associated security ID (SID).</span></span> <span data-ttu-id="b9d4b-112">Поскольку эта процедура может занимать много времени, клиент может выполнять разрешение имен асинхронно в фоновом потоке.</span><span class="sxs-lookup"><span data-stu-id="b9d4b-112">Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread.</span></span> <span data-ttu-id="b9d4b-113">При разрешении имени пользователя объект [**дисккуотаконтрол**](diskquotacontrol-object.md) уведомляет свой клиент, выполнив событие **онусернамечанжед** .</span><span class="sxs-lookup"><span data-stu-id="b9d4b-113">When a user's name is resolved, the [**DiskQuotaControl**](diskquotacontrol-object.md) object notifies its client by firing the **OnUserNameChanged** event.</span></span> <span data-ttu-id="b9d4b-114">Объект **дидисккуотаусер** , связанный с пользователем, передается в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="b9d4b-114">A **DIDiskQuotaUser** object associated with the user is passed as a parameter.</span></span> <span data-ttu-id="b9d4b-115">Этот объект позволяет клиенту изменять параметры квоты пользователя.</span><span class="sxs-lookup"><span data-stu-id="b9d4b-115">This object allows the client to modify the user's quota settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9d4b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b9d4b-116">Requirements</span></span>



| <span data-ttu-id="b9d4b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b9d4b-117">Requirement</span></span> | <span data-ttu-id="b9d4b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b9d4b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d4b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9d4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9d4b-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9d4b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9d4b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9d4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9d4b-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9d4b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b9d4b-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b9d4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9d4b-124"><dt>Дсккуота. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9d4b-124"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="b9d4b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b9d4b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9d4b-126"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b9d4b-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9d4b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9d4b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d4b-128">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="b9d4b-128">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




