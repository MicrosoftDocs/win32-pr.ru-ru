---
title: Структура RAS_PPP_IPXCP_RESULT (Рассапи. h)
description: '\_Структура результатов «RAS PPP \_ IPXCP» \_ используется для передачи результатов операции проецирования объединенной сети PPP (IPX) для порта.'
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS структуры RAS_PPP_IPXCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071700"
---
# <a name="ras_ppp_ipxcp_result-structure"></a><span data-ttu-id="dd4f5-104">\_ \_ Структура результатов PPP для RAS РРР \_</span><span class="sxs-lookup"><span data-stu-id="dd4f5-104">RAS\_PPP\_IPXCP\_RESULT structure</span></span>

<span data-ttu-id="dd4f5-105">\[**\_ \_ \_ Результирующая структура RAS PPP IPXCP** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="dd4f5-105">\[The **RAS\_PPP\_IPXCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="dd4f5-106">Структура **результатов «RAS \_ PPP \_ IPXCP \_** » используется для передачи результатов операции проецирования объединенной сети PPP (IPX) для порта.</span><span class="sxs-lookup"><span data-stu-id="dd4f5-106">The **RAS\_PPP\_IPXCP\_RESULT** structure is used to report the result of a PPP Internetwork Packet Exchange (IPX) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4f5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd4f5-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="dd4f5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="dd4f5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd4f5-109">**дверрор**</span><span class="sxs-lookup"><span data-stu-id="dd4f5-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="dd4f5-110">Указывает результаты операции IPX-проекции.</span><span class="sxs-lookup"><span data-stu-id="dd4f5-110">Indicates the results of the IPX projection operation.</span></span> <span data-ttu-id="dd4f5-111">Значение NO \_ Error указывает на успешное выполнение, в этом случае член **всзаддресс** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="dd4f5-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="dd4f5-112">Если операция проекции не выполнена, **дверрор** является кодом ошибки из Winerror. h или расеррор. h.</span><span class="sxs-lookup"><span data-stu-id="dd4f5-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="dd4f5-113">**всзаддресс**</span><span class="sxs-lookup"><span data-stu-id="dd4f5-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="dd4f5-114">Строка в Юникоде, заканчивающаяся нулем и указывающая IPX-адрес, назначенный удаленному клиенту.</span><span class="sxs-lookup"><span data-stu-id="dd4f5-114">A null-terminated Unicode string that specifies the IPX address assigned to the remote client.</span></span> <span data-ttu-id="dd4f5-115">Эта строка содержит \* NET \***.** Форма _узла_ .</span><span class="sxs-lookup"><span data-stu-id="dd4f5-115">This string has the \*net\***.**_node_ form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd4f5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dd4f5-116">Requirements</span></span>



| <span data-ttu-id="dd4f5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dd4f5-117">Requirement</span></span> | <span data-ttu-id="dd4f5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dd4f5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4f5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd4f5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4f5-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd4f5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dd4f5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd4f5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4f5-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd4f5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dd4f5-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dd4f5-123">End of client support</span></span><br/>    | <span data-ttu-id="dd4f5-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd4f5-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="dd4f5-125">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="dd4f5-125">End of server support</span></span><br/>    | <span data-ttu-id="dd4f5-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd4f5-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="dd4f5-127">Header</span><span class="sxs-lookup"><span data-stu-id="dd4f5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd4f5-128"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd4f5-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd4f5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd4f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4f5-130">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="dd4f5-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="dd4f5-131">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="dd4f5-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="dd4f5-132">**\_Порт RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="dd4f5-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="dd4f5-133">**\_ \_ результат проекции PPP для RAS \_**</span><span class="sxs-lookup"><span data-stu-id="dd4f5-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="dd4f5-134">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="dd4f5-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





