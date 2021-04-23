---
title: Структура CB_TARGET_INFO (Кбклиент. h)
description: Содержит сведения о целевом компьютере и IP-адресах, на которые должны перенаправляться входящие подключения.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO структуры службы удаленных рабочих столов
- PCB_TARGET_INFO службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415085"
---
# <a name="cb_target_info-structure"></a><span data-ttu-id="755bd-105">\_ \_ Структура сведений о целевом объекте CB</span><span class="sxs-lookup"><span data-stu-id="755bd-105">CB\_TARGET\_INFO structure</span></span>

<span data-ttu-id="755bd-106">Содержит сведения о целевом компьютере и IP-адресах, на которые должны перенаправляться входящие подключения.</span><span class="sxs-lookup"><span data-stu-id="755bd-106">Contains information about the target computer and IP addresses where incoming connections should be redirected.</span></span> <span data-ttu-id="755bd-107">Эта структура используется с методом [**иконнектионброкерклиент:: жеттаржетинфо**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="755bd-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="755bd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="755bd-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="755bd-109">Члены</span><span class="sxs-lookup"><span data-stu-id="755bd-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="755bd-110">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="755bd-110">**ServerName**</span></span>
</dt> <dd>

<span data-ttu-id="755bd-111">Представляет полное доменное имя целевого сервера.</span><span class="sxs-lookup"><span data-stu-id="755bd-111">Represents the fully qualified domain name of the target server.</span></span> <span data-ttu-id="755bd-112">Для сценария удаленный рабочий стол Virtualization (RDV) этот член имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="755bd-112">For a Remote Desktop virtualization (RDV) scenario, this member is **NULL**.</span></span> <span data-ttu-id="755bd-113">Для сценария узла удаленный рабочий стол сеансов (узлов сеансов удаленных рабочих столов) этот член содержит имя сервера, на котором перенаправляется входящее подключение.</span><span class="sxs-lookup"><span data-stu-id="755bd-113">For a Remote Desktop session host (RDSH) scenario, this member contains the server name where the incoming connection is redirected.</span></span>

</dd> <dt>

<span data-ttu-id="755bd-114">**аддресскаунт**</span><span class="sxs-lookup"><span data-stu-id="755bd-114">**AddressCount**</span></span>
</dt> <dd>

<span data-ttu-id="755bd-115">Количество допустимых записей в массиве **addresses** .</span><span class="sxs-lookup"><span data-stu-id="755bd-115">The number of valid entries in the **Addresses** array.</span></span>

</dd> <dt>

<span data-ttu-id="755bd-116">**Адреса**</span><span class="sxs-lookup"><span data-stu-id="755bd-116">**Addresses**</span></span>
</dt> <dd>

<span data-ttu-id="755bd-117">Массив строк, содержащий IP-адреса, на которые перенаправляются входящие подключения.</span><span class="sxs-lookup"><span data-stu-id="755bd-117">An array of strings that contain the IP addresses where the incoming connections are redirected.</span></span> <span data-ttu-id="755bd-118">Число допустимых элементов в этом массиве указано в элементе **аддресскаунт** .</span><span class="sxs-lookup"><span data-stu-id="755bd-118">The number of valid elements in this array is specified in the **AddressCount** member.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="755bd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="755bd-119">Requirements</span></span>



| <span data-ttu-id="755bd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="755bd-120">Requirement</span></span> | <span data-ttu-id="755bd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="755bd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="755bd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="755bd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="755bd-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="755bd-123">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="755bd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="755bd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="755bd-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="755bd-125">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="755bd-126">Header</span><span class="sxs-lookup"><span data-stu-id="755bd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="755bd-127"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="755bd-127"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="755bd-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="755bd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755bd-129">**Иконнектионброкерклиент:: Жеттаржетинфо**</span><span class="sxs-lookup"><span data-stu-id="755bd-129">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





