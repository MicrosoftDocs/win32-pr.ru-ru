---
title: Структура RAS_PPP_IPCP_RESULT (Рассапи. h)
description: '\_ \_ \_ Результирующая структура RAS PPP РРР используется для передачи результатов операции проекции протокола IP PPP для порта.'
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS структуры RAS_PPP_IPCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534265"
---
# <a name="ras_ppp_ipcp_result-structure"></a><span data-ttu-id="22e68-104">\_ \_ Результирующая структура PPP удаленного доступа IPCP \_</span><span class="sxs-lookup"><span data-stu-id="22e68-104">RAS\_PPP\_IPCP\_RESULT structure</span></span>

<span data-ttu-id="22e68-105">\[**\_ \_ \_ Результирующая структура RAS PPP РРР** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="22e68-105">\[The **RAS\_PPP\_IPCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="22e68-106">**\_ \_ \_ Результирующая структура RAS PPP РРР** используется для передачи результатов операции проекции протокола IP PPP для порта.</span><span class="sxs-lookup"><span data-stu-id="22e68-106">The **RAS\_PPP\_IPCP\_RESULT** structure is used to report the result of a PPP Internet Protocol (IP) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e68-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22e68-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="22e68-108">Члены</span><span class="sxs-lookup"><span data-stu-id="22e68-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="22e68-109">**дверрор**</span><span class="sxs-lookup"><span data-stu-id="22e68-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="22e68-110">Указывает результаты операции проецирования IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="22e68-110">Indicates the results of the IP projection operation.</span></span> <span data-ttu-id="22e68-111">Значение NO \_ Error указывает на успешное выполнение, в этом случае член **всзаддресс** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="22e68-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="22e68-112">Если операция проекции не выполнена, **дверрор** является кодом ошибки из Winerror. h или расеррор. h.</span><span class="sxs-lookup"><span data-stu-id="22e68-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="22e68-113">**всзаддресс**</span><span class="sxs-lookup"><span data-stu-id="22e68-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="22e68-114">Строка в Юникоде, заканчивающаяся нулем и указывающая IP-адрес, назначенный удаленному клиенту.</span><span class="sxs-lookup"><span data-stu-id="22e68-114">A null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span> <span data-ttu-id="22e68-115">Эта строка имеет форму \*a ***.** _б_* _._ *_в_*_._ \* _г_.</span><span class="sxs-lookup"><span data-stu-id="22e68-115">This string has the form *a\***.**_b_*_._*_c_*_._\*_d_.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22e68-116">Требования</span><span class="sxs-lookup"><span data-stu-id="22e68-116">Requirements</span></span>



| <span data-ttu-id="22e68-117">Требование</span><span class="sxs-lookup"><span data-stu-id="22e68-117">Requirement</span></span> | <span data-ttu-id="22e68-118">Значение</span><span class="sxs-lookup"><span data-stu-id="22e68-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22e68-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22e68-119">Minimum supported client</span></span><br/> | <span data-ttu-id="22e68-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22e68-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="22e68-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22e68-121">Minimum supported server</span></span><br/> | <span data-ttu-id="22e68-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22e68-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="22e68-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="22e68-123">End of client support</span></span><br/>    | <span data-ttu-id="22e68-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="22e68-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="22e68-125">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="22e68-125">End of server support</span></span><br/>    | <span data-ttu-id="22e68-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="22e68-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="22e68-127">Header</span><span class="sxs-lookup"><span data-stu-id="22e68-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="22e68-128"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="22e68-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e68-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22e68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e68-130">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="22e68-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="22e68-131">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="22e68-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="22e68-132">**\_Порт RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="22e68-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="22e68-133">**\_ \_ результат проекции PPP для RAS \_**</span><span class="sxs-lookup"><span data-stu-id="22e68-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="22e68-134">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="22e68-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





