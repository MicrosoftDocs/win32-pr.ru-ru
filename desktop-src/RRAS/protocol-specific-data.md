---
title: Структура PROTOCOL_SPECIFIC_DATA (RTM. h)
description: '\_Структура данных, характерная для протокола, \_ содержит память, зарезервированную для данных конкретного протокола маршрутизации.'
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- RAS структуры PROTOCOL_SPECIFIC_DATA
- RAS — указатель структуры PPROTOCOL_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802794"
---
# <a name="protocol_specific_data-structure"></a><span data-ttu-id="cd437-105">\_Структура данных, характерная для протокола \_</span><span class="sxs-lookup"><span data-stu-id="cd437-105">PROTOCOL\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="cd437-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cd437-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="cd437-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="cd437-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="cd437-108">Структура **\_ \_ данных, характерная для протокола** , содержит память, зарезервированную для данных конкретного протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="cd437-108">The **PROTOCOL\_SPECIFIC\_DATA** structure contains memory reserved for data specific to a particular routing protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd437-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd437-109">Syntax</span></span>


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="cd437-110">Члены</span><span class="sxs-lookup"><span data-stu-id="cd437-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd437-111">**\_Данные PSD**</span><span class="sxs-lookup"><span data-stu-id="cd437-111">**PSD\_Data**</span></span>
</dt> <dd>

<span data-ttu-id="cd437-112">Задает массив переменных **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="cd437-112">Specifies an array of **DWORD** variables.</span></span> <span data-ttu-id="cd437-113">Эта память резервируется для данных, относящихся к протоколам маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="cd437-113">This memory is reserved for data that is specific to routing protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd437-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cd437-114">Requirements</span></span>



| <span data-ttu-id="cd437-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cd437-115">Requirement</span></span> | <span data-ttu-id="cd437-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cd437-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cd437-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd437-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd437-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cd437-118">None supported</span></span><br/>                                                        |
| <span data-ttu-id="cd437-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd437-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd437-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cd437-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cd437-121">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cd437-121">End of server support</span></span><br/>    | <span data-ttu-id="cd437-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd437-122">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="cd437-123">Header</span><span class="sxs-lookup"><span data-stu-id="cd437-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd437-124"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd437-124"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd437-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd437-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd437-126">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="cd437-126">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="cd437-127">Структуры диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="cd437-127">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="cd437-128">**Окончательная версия \_ IP- \_ маршрута**</span><span class="sxs-lookup"><span data-stu-id="cd437-128">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="cd437-129">**\_маршрут IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="cd437-129">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





