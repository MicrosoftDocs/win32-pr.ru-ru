---
title: Структура RAS_PPP_PROJECTION_RESULT (Рассапи. h)
description: '\_ \_ Структура результата проекции PPP для RAS \_ используется для передачи результатов различных операций проекции PPP для порта.'
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS структуры RAS_PPP_PROJECTION_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802495"
---
# <a name="ras_ppp_projection_result-structure"></a><span data-ttu-id="5ffa9-104">\_ \_ Структура результата проекции PPP для RAS \_</span><span class="sxs-lookup"><span data-stu-id="5ffa9-104">RAS\_PPP\_PROJECTION\_RESULT structure</span></span>

<span data-ttu-id="5ffa9-105">\[Структура **\_ \_ \_ результата проекции PPP для RAS** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="5ffa9-105">\[The **RAS\_PPP\_PROJECTION\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="5ffa9-106">Структура **\_ \_ \_ результата проекции PPP для RAS** используется для передачи результатов различных операций проекции PPP для порта.</span><span class="sxs-lookup"><span data-stu-id="5ffa9-106">The **RAS\_PPP\_PROJECTION\_RESULT** structure is used to report the results of the various PPP projection operations for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ffa9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ffa9-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a><span data-ttu-id="5ffa9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5ffa9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ffa9-109">**nbf**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-109">**nbf**</span></span>
</dt> <dd>

<span data-ttu-id="5ffa9-110">Структура [**\_ \_ \_ результата нбфкп для RAS PPP**](ras-ppp-nbfcp-result-str.md) , которая сообщает результат операции проекции PPP NetBEUI (NBF).</span><span class="sxs-lookup"><span data-stu-id="5ffa9-110">A [**RAS\_PPP\_NBFCP\_RESULT**](ras-ppp-nbfcp-result-str.md) structure that reports the result of a PPP NetBEUI Framer (NBF) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ffa9-111">**см**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-111">**ip**</span></span>
</dt> <dd>

<span data-ttu-id="5ffa9-112">[**\_ \_ \_ Результирующая структура RAS PPP РРР**](ras-ppp-ipcp-result-str.md) , которая сообщает результат операции проекции протокола IP PPP.</span><span class="sxs-lookup"><span data-stu-id="5ffa9-112">A [**RAS\_PPP\_IPCP\_RESULT**](ras-ppp-ipcp-result-str.md) structure that reports the result of a PPP Internet Protocol (IP) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ffa9-113">**пользу**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-113">**ipx**</span></span>
</dt> <dd>

<span data-ttu-id="5ffa9-114">Структура [**\_ \_ \_ результата PPP РРР**](ras-ppp-ipxcp-result-str.md) , которая сообщает результат операции проецирования объединенной сети (IPX) PPP.</span><span class="sxs-lookup"><span data-stu-id="5ffa9-114">A [**RAS\_PPP\_IPXCP\_RESULT**](ras-ppp-ipxcp-result-str.md) structure that reports the result of a PPP Internetwork Packet Exchange (IPX) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ffa9-115">**at**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-115">**at**</span></span>
</dt> <dd>

<span data-ttu-id="5ffa9-116">[**\_ \_ \_ Результирующая структура RAS PPP**](ras-ppp-atcp-result-str.md) .</span><span class="sxs-lookup"><span data-stu-id="5ffa9-116">A [**RAS\_PPP\_ATCP\_RESULT**](ras-ppp-atcp-result-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ffa9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ffa9-117">Remarks</span></span>

<span data-ttu-id="5ffa9-118">Эта структура сообщает результаты проекции для протоколов NetBEUI, TCP/IP и IPX.</span><span class="sxs-lookup"><span data-stu-id="5ffa9-118">This structure reports the projection results for NetBEUI, TCP/IP, and IPX protocols.</span></span> <span data-ttu-id="5ffa9-119">Каждая структура PPP имеет элемент **дверрор** , который указывает, является ли действительная информация в структуре допустимой.</span><span class="sxs-lookup"><span data-stu-id="5ffa9-119">Each PPP structure has a **dwError** member that indicates whether the other information in the structure is valid.</span></span> <span data-ttu-id="5ffa9-120">Если **дверрор** не является \_ ошибкой, другие сведения являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="5ffa9-120">If **dwError** is NO\_ERROR, the other information is valid.</span></span> <span data-ttu-id="5ffa9-121">Если **дверрор** является одним из кодов ошибок в файле Winerror. h или расеррор. h, другие сведения являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="5ffa9-121">If **dwError** is one of the error codes in Winerror.h or Raserror.h, the other information is not valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ffa9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5ffa9-122">Requirements</span></span>



| <span data-ttu-id="5ffa9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5ffa9-123">Requirement</span></span> | <span data-ttu-id="5ffa9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5ffa9-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffa9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ffa9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5ffa9-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ffa9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5ffa9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ffa9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5ffa9-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ffa9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5ffa9-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5ffa9-129">End of client support</span></span><br/>    | <span data-ttu-id="5ffa9-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5ffa9-130">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="5ffa9-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5ffa9-131">End of server support</span></span><br/>    | <span data-ttu-id="5ffa9-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5ffa9-132">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="5ffa9-133">Header</span><span class="sxs-lookup"><span data-stu-id="5ffa9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ffa9-134"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ffa9-134"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ffa9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ffa9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ffa9-136">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="5ffa9-136">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="5ffa9-137">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="5ffa9-137">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="5ffa9-138">**\_Порт RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-138">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="5ffa9-139">**\_результат RAS \_ PPP \_**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-139">**RAS\_PPP\_ATCP\_RESULT**</span></span>](ras-ppp-atcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="5ffa9-140">**\_результат RAS \_ PPP \_**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-140">**RAS\_PPP\_IPCP\_RESULT**</span></span>](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="5ffa9-141">**\_результат PPP \_ для удаленного доступа \_**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-141">**RAS\_PPP\_IPXCP\_RESULT**</span></span>](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="5ffa9-142">**\_ \_ результат нбфкп PPP для RAS \_**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-142">**RAS\_PPP\_NBFCP\_RESULT**</span></span>](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="5ffa9-143">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="5ffa9-143">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





