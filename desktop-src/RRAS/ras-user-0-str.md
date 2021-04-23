---
title: Структура RAS_USER_0 (Рассапи. h)
description: '\_Структура пользователя RAS \_ 0 используется в функциях Расадминусерсетинфо и расадминусержетинфо для указания сведений о пользователе.'
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS структуры RAS_USER_0
- RAS — указатель структуры PRAS_USER_0
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534103"
---
# <a name="ras_user_0-structure"></a><span data-ttu-id="8e688-105">\_Структура пользователя RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="8e688-105">RAS\_USER\_0 structure</span></span>

<span data-ttu-id="8e688-106">\[Эта версия структуры **пользователя RAS \_ \_ 0** не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8e688-106">\[This version of the **RAS\_USER\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="8e688-107">Используйте более новый [**\_ пользователь RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) , определенный в мпрапи. h.\]</span><span class="sxs-lookup"><span data-stu-id="8e688-107">Use the newer [**RAS\_USER\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="8e688-108">Структура **\_ пользователя RAS \_ 0** используется в функциях [**расадминусерсетинфо**](rasadminusersetinfo.md) и [**расадминусержетинфо**](rasadminusergetinfo.md) для указания сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="8e688-108">The **RAS\_USER\_0** structure is used in the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) and [**RasAdminUserGetInfo**](rasadminusergetinfo.md) functions to specify information about a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e688-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e688-109">Syntax</span></span>


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a><span data-ttu-id="8e688-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8e688-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="8e688-111">**бфпривилеже**</span><span class="sxs-lookup"><span data-stu-id="8e688-111">**bfPrivilege**</span></span>
</dt> <dd>

<span data-ttu-id="8e688-112">Набор битовых флагов, задающих права доступа RAS для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8e688-112">A set of bit flags that specify the RAS privileges of the user.</span></span> <span data-ttu-id="8e688-113">Этот член может быть сочетанием \_ флага расприв диалинпривилеже и одним из флагов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8e688-113">This member can be a combination of the RASPRIV\_DialinPrivilege flag and one of the call-back flags.</span></span> <span data-ttu-id="8e688-114">Используйте \_ маску КАЛЛБАККТИПЕ расприв, чтобы указать тип привилегий обратного вызова, предоставленный пользователю.</span><span class="sxs-lookup"><span data-stu-id="8e688-114">Use the RASPRIV\_CallbackType mask to identify the type of call-back privilege provided to the user.</span></span> <span data-ttu-id="8e688-115">Определены следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="8e688-115">The following flags are defined.</span></span>



| <span data-ttu-id="8e688-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8e688-116">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="8e688-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8e688-117">Meaning</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <span data-ttu-id="8e688-118"><dt>**\_Обратный вызов расприв**</dt></span><span class="sxs-lookup"><span data-stu-id="8e688-118"><dt>**RASPRIV\_NoCallback**</dt></span></span> </dl>                             | <span data-ttu-id="8e688-119">У пользователя нет прав на обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="8e688-119">The user has no call-back privilege.</span></span><br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <span data-ttu-id="8e688-120"><dt>**РАСПРИВ \_ админсеткаллбакк**</dt></span><span class="sxs-lookup"><span data-stu-id="8e688-120"><dt>**RASPRIV\_AdminSetCallback**</dt></span></span> </dl>     | <span data-ttu-id="8e688-121">Учетная запись пользователя настроена так, чтобы администратор установил номер обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8e688-121">The user account is configured to have the administrator set the call-back number.</span></span><br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <span data-ttu-id="8e688-122"><dt>**РАСПРИВ \_ каллерсеткаллбакк**</dt></span><span class="sxs-lookup"><span data-stu-id="8e688-122"><dt>**RASPRIV\_CallerSetCallback**</dt></span></span> </dl> | <span data-ttu-id="8e688-123">Удаленный пользователь может указать номер телефона для обратного вызова при наборе номера.</span><span class="sxs-lookup"><span data-stu-id="8e688-123">The remote user can specify a call-back phone number when dialing in.</span></span><br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <span data-ttu-id="8e688-124"><dt>**РАСПРИВ \_ диалинпривилеже**</dt></span><span class="sxs-lookup"><span data-stu-id="8e688-124"><dt>**RASPRIV\_DialinPrivilege**</dt></span></span> </dl>         | <span data-ttu-id="8e688-125">Пользователь имеет разрешение на вызов на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="8e688-125">The user has permission to dial in to this server.</span></span><br/>                                 |



 

<span data-ttu-id="8e688-126">Укажите один из флагов обратного вызова в вызове функции [**расадминусерсетинфо**](rasadminusersetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="8e688-126">Specify one of the call-back flags in the call to the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8e688-127">**сзфоненумбер**</span><span class="sxs-lookup"><span data-stu-id="8e688-127">**szPhoneNumber**</span></span>
</dt> <dd>

<span data-ttu-id="8e688-128">Строка в Юникоде, заканчивающаяся нулем, которая указывает номер телефона для обратного вызова для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8e688-128">A null-terminated Unicode string that specifies the call-back phone number for the user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e688-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8e688-129">Requirements</span></span>



| <span data-ttu-id="8e688-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8e688-130">Requirement</span></span> | <span data-ttu-id="8e688-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8e688-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8e688-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e688-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8e688-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8e688-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8e688-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e688-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8e688-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8e688-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8e688-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8e688-136">End of client support</span></span><br/>    | <span data-ttu-id="8e688-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e688-137">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="8e688-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8e688-138">End of server support</span></span><br/>    | <span data-ttu-id="8e688-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e688-139">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="8e688-140">Header</span><span class="sxs-lookup"><span data-stu-id="8e688-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e688-141"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e688-141"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e688-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e688-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e688-143">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="8e688-143">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="8e688-144">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="8e688-144">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="8e688-145">**расадминусержетинфо**</span><span class="sxs-lookup"><span data-stu-id="8e688-145">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="8e688-146">**расадминусерсетинфо**</span><span class="sxs-lookup"><span data-stu-id="8e688-146">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

 





