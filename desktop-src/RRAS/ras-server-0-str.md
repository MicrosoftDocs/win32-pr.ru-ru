---
title: Структура RAS_SERVER_0 (Рассапи. h)
description: '\_Структура сервера RAS \_ 0 используется функцией расадминсервержетинфо для получения сведений о портах, настроенных на сервере удаленного доступа.'
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS структуры RAS_SERVER_0
- RAS — указатель структуры PRAS_SERVER_0
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650386"
---
# <a name="ras_server_0-structure"></a><span data-ttu-id="e5490-105">\_Структура сервера RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="e5490-105">RAS\_SERVER\_0 structure</span></span>

<span data-ttu-id="e5490-106">\[Структура **RAS- \_ сервера \_ 0** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="e5490-106">\[The **RAS\_SERVER\_0** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="e5490-107">Структура **\_ сервера RAS \_ 0** используется функцией [**расадминсервержетинфо**](rasadminservergetinfo.md) для получения сведений о портах, настроенных на сервере удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="e5490-107">The **RAS\_SERVER\_0** structure is used by the [**RasAdminServerGetInfo**](rasadminservergetinfo.md) function to return information about the ports configured on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5490-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5490-108">Syntax</span></span>


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a><span data-ttu-id="e5490-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e5490-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e5490-110">**тоталпортс**</span><span class="sxs-lookup"><span data-stu-id="e5490-110">**TotalPorts**</span></span>
</dt> <dd>

<span data-ttu-id="e5490-111">Указывает общее число портов, настроенных на сервере удаленного доступа, которые доступны удаленным клиентам для подключения.</span><span class="sxs-lookup"><span data-stu-id="e5490-111">Specifies the total number of ports configured on the RAS server that are available for remote clients to connect to.</span></span> <span data-ttu-id="e5490-112">Например, если общее число портов, настроенных для удаленного подключения к серверу, равно четырем, но один из портов в настоящее время используется для исходящих вызовов, **тоталпортс** — три.</span><span class="sxs-lookup"><span data-stu-id="e5490-112">For example, if the total number of ports configured for dialing in to a server is four, but one of the ports is currently in use for dialing out, **TotalPorts** is three.</span></span>

</dd> <dt>

<span data-ttu-id="e5490-113">**портсинусе**</span><span class="sxs-lookup"><span data-stu-id="e5490-113">**PortsInUse**</span></span>
</dt> <dd>

<span data-ttu-id="e5490-114">Указывает количество портов, используемых удаленными клиентами в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="e5490-114">Specifies the number of ports currently in use by remote clients.</span></span>

</dd> <dt>

<span data-ttu-id="e5490-115">**расверсион**</span><span class="sxs-lookup"><span data-stu-id="e5490-115">**RasVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e5490-116">Указывает версию сервера RAS.</span><span class="sxs-lookup"><span data-stu-id="e5490-116">Specifies the version of the RAS server.</span></span> <span data-ttu-id="e5490-117">Используйте эти сведения для выполнения действий, связанных с конкретной версией.</span><span class="sxs-lookup"><span data-stu-id="e5490-117">Use this information to take version-specific action.</span></span> <span data-ttu-id="e5490-118">Этот член является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e5490-118">This member is one of the following values.</span></span>



| <span data-ttu-id="e5490-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e5490-119">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="e5490-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e5490-120">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <span data-ttu-id="e5490-121"><dt>**расдовнлевел**</dt></span><span class="sxs-lookup"><span data-stu-id="e5490-121"><dt>**RASDOWNLEVEL**</dt></span></span> </dl>              | <span data-ttu-id="e5490-122">Указывает сервер удаленного доступа LAN Manager версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="e5490-122">Indicates a LAN Manager version 1.0 RAS server.</span></span><br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <span data-ttu-id="e5490-123"><dt>**РАСАДМИН \_ 35**</dt></span><span class="sxs-lookup"><span data-stu-id="e5490-123"><dt>**RASADMIN\_35**</dt></span></span> </dl>                | <span data-ttu-id="e5490-124">Указывает сервер или клиент RAS Windows NT 3,51 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="e5490-124">Indicates a Windows NT Server 3.51 and earlier RAS server or client.</span></span><br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <span data-ttu-id="e5490-125"><dt>**РАСАДМИН \_ текущий**</dt></span><span class="sxs-lookup"><span data-stu-id="e5490-125"><dt>**RASADMIN\_CURRENT**</dt></span></span> </dl> | <span data-ttu-id="e5490-126">Указывает сервер или клиент RAS Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="e5490-126">Indicates a Windows NT 4.0 RAS server or client.</span></span><br/>                     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5490-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e5490-127">Requirements</span></span>



| <span data-ttu-id="e5490-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e5490-128">Requirement</span></span> | <span data-ttu-id="e5490-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e5490-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5490-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5490-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e5490-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5490-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e5490-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5490-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e5490-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5490-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e5490-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e5490-134">End of client support</span></span><br/>    | <span data-ttu-id="e5490-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e5490-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="e5490-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e5490-136">End of server support</span></span><br/>    | <span data-ttu-id="e5490-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5490-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="e5490-138">Header</span><span class="sxs-lookup"><span data-stu-id="e5490-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5490-139"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5490-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5490-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5490-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5490-141">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="e5490-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="e5490-142">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="e5490-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="e5490-143">**расадминсервержетинфо**</span><span class="sxs-lookup"><span data-stu-id="e5490-143">**RasAdminServerGetInfo**</span></span>](rasadminservergetinfo.md)
</dt> </dl>

 

 





