---
title: Структура RAS_PPP_ATCP_RESULT (Рассапи. h)
description: '\_Результирующая структура RAS PPP для сервера \_ \_ сообщает результат операции проецирования протокола AppleTalk для порта.'
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS структуры RAS_PPP_ATCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988761"
---
# <a name="ras_ppp_atcp_result-structure"></a><span data-ttu-id="d2549-104">\_ \_ \_ Результирующая структура RAS PPP</span><span class="sxs-lookup"><span data-stu-id="d2549-104">RAS\_PPP\_ATCP\_RESULT structure</span></span>

<span data-ttu-id="d2549-105">\[**\_ \_ \_ Результирующая структура RAS PPP** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="d2549-105">\[The **RAS\_PPP\_ATCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="d2549-106">**\_ \_ \_ Результирующая структура RAS PPP для сервера** сообщает результат операции проецирования протокола AppleTalk для порта.</span><span class="sxs-lookup"><span data-stu-id="d2549-106">The **RAS\_PPP\_ATCP\_RESULT** structure is used to report the result of an AppleTalk protocol projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2549-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2549-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="d2549-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d2549-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2549-109">**дверрор**</span><span class="sxs-lookup"><span data-stu-id="d2549-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="d2549-110">Задает значение, указывающее результаты операции с проекцией AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="d2549-110">Specifies a value that indicates the results of the AppleTalk projection operation.</span></span> <span data-ttu-id="d2549-111">Значение NO \_ Error указывает на успешное выполнение, в этом случае член **всзаддресс** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="d2549-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="d2549-112">Если операция проекции не выполнена, **дверрор** является кодом ошибки из Winerror. h или расеррор. h.</span><span class="sxs-lookup"><span data-stu-id="d2549-112">If the projection operation is not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="d2549-113">**всзаддресс**</span><span class="sxs-lookup"><span data-stu-id="d2549-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d2549-114">Указывает строку в Юникоде, завершающуюся нулем, которая указывает IP-адрес, назначенный удаленному клиенту.</span><span class="sxs-lookup"><span data-stu-id="d2549-114">Specifies a null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2549-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d2549-115">Requirements</span></span>



| <span data-ttu-id="d2549-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d2549-116">Requirement</span></span> | <span data-ttu-id="d2549-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d2549-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2549-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2549-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2549-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d2549-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d2549-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2549-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2549-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d2549-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d2549-122">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d2549-122">End of client support</span></span><br/>    | <span data-ttu-id="d2549-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2549-123">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="d2549-124">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d2549-124">End of server support</span></span><br/>    | <span data-ttu-id="d2549-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2549-125">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="d2549-126">Header</span><span class="sxs-lookup"><span data-stu-id="d2549-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2549-127"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2549-127"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2549-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2549-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2549-129">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="d2549-129">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="d2549-130">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="d2549-130">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="d2549-131">**\_ \_ результат проекции PPP для RAS \_**</span><span class="sxs-lookup"><span data-stu-id="d2549-131">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





