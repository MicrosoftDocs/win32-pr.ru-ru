---
title: Структура RAS_PPP_NBFCP_RESULT (Рассапи. h)
description: '\_ \_ Структура результатов RAS PPP нбфкп \_ используется для передачи результатов операции проекции PPP-протокола NetBEUI (NBF) для порта.'
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS структуры RAS_PPP_NBFCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136111"
---
# <a name="ras_ppp_nbfcp_result-structure"></a><span data-ttu-id="9ff6e-104">\_ \_ Структура результата нбфкп PPP для RAS \_</span><span class="sxs-lookup"><span data-stu-id="9ff6e-104">RAS\_PPP\_NBFCP\_RESULT structure</span></span>

<span data-ttu-id="9ff6e-105">\[Структура **\_ \_ \_ результата RAS PPP Нбфкп** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="9ff6e-105">\[The **RAS\_PPP\_NBFCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="9ff6e-106">Структура **\_ \_ \_ результатов RAS PPP нбфкп** используется для передачи результатов операции проекции PPP-протокола NetBEUI (NBF) для порта.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-106">The **RAS\_PPP\_NBFCP\_RESULT** structure is used to report the result of a PPP NetBEUI Framer (NBF) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff6e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ff6e-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="9ff6e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9ff6e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ff6e-109">**дверрор**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="9ff6e-110">Указывает результаты операции NBF "Проекция".</span><span class="sxs-lookup"><span data-stu-id="9ff6e-110">Indicates the results of the NBF projection operation.</span></span> <span data-ttu-id="9ff6e-111">Значение NO \_ Error указывает на успешное выполнение. в этом случае член **всзвкста** содержит имя удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-111">A value of NO\_ERROR indicates success, in which case, the **wszWksta** member contains the name of the remote computer.</span></span> <span data-ttu-id="9ff6e-112">Если операция проекции не выполнена, **дверрор** является кодом ошибки из Winerror. h или расеррор. h.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-113">**двнетбиосеррор**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-113">**dwNetBiosError**</span></span>
</dt> <dd>

<span data-ttu-id="9ff6e-114">Пропускать этот элемент на сервере; Он относится только к клиенту.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-114">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-115">**szName**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-115">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="9ff6e-116">Пропускать этот элемент на сервере; Он относится только к клиенту.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-116">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-117">**всзвкста**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-117">**wszWksta**</span></span>
</dt> <dd>

<span data-ttu-id="9ff6e-118">Строка в Юникоде, заканчивающаяся нулем и указывающая NetBIOS-имя клиентской рабочей станции RAS.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-118">A null-terminated Unicode string that specifies the NetBIOS name of the RAS client workstation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ff6e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9ff6e-119">Requirements</span></span>



| <span data-ttu-id="9ff6e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9ff6e-120">Requirement</span></span> | <span data-ttu-id="9ff6e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9ff6e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff6e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ff6e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff6e-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ff6e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9ff6e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ff6e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff6e-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ff6e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9ff6e-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9ff6e-126">End of client support</span></span><br/>    | <span data-ttu-id="9ff6e-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ff6e-127">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="9ff6e-128">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9ff6e-128">End of server support</span></span><br/>    | <span data-ttu-id="9ff6e-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ff6e-129">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="9ff6e-130">Header</span><span class="sxs-lookup"><span data-stu-id="9ff6e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff6e-131"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff6e-131"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ff6e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ff6e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff6e-133">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-133">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-134">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="9ff6e-134">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-135">**\_Порт RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-135">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-136">**\_ \_ результат проекции PPP для RAS \_**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-136">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-137">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-137">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





