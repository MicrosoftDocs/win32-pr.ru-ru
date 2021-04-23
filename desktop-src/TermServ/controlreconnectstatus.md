---
title: Перечисление Контролреконнектстатус
description: Указывает результат метода повторного подключения IMsRdpClient8.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Контролреконнектстатус
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672519"
---
# <a name="controlreconnectstatus-enumeration"></a><span data-ttu-id="2f4fe-104">Перечисление Контролреконнектстатус</span><span class="sxs-lookup"><span data-stu-id="2f4fe-104">ControlReconnectStatus enumeration</span></span>

<span data-ttu-id="2f4fe-105">Указывает результат метода [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="2f4fe-105">Specifies the result of the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4fe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f4fe-106">Syntax</span></span>


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a><span data-ttu-id="2f4fe-107">Константы</span><span class="sxs-lookup"><span data-stu-id="2f4fe-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2f4fe-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**контролреконнектстартед**</span><span class="sxs-lookup"><span data-stu-id="2f4fe-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span></span>
</dt> <dd>

<span data-ttu-id="2f4fe-109">Операция повторного подключения была запущена.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-109">The reconnect operation was started.</span></span>

</dd> <dt>

<span data-ttu-id="2f4fe-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**контролреконнектблоккед**</span><span class="sxs-lookup"><span data-stu-id="2f4fe-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span></span>
</dt> <dd>

<span data-ttu-id="2f4fe-111">Не удалось запустить операцию повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-111">The reconnect operation could not be started.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f4fe-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2f4fe-112">Requirements</span></span>



| <span data-ttu-id="2f4fe-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2f4fe-113">Requirement</span></span> | <span data-ttu-id="2f4fe-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2f4fe-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4fe-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f4fe-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2f4fe-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f4fe-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="2f4fe-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f4fe-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2f4fe-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f4fe-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="2f4fe-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2f4fe-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f4fe-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f4fe-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f4fe-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f4fe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4fe-122">**IMsRdpClient8:: Reconnect**</span><span class="sxs-lookup"><span data-stu-id="2f4fe-122">**IMsRdpClient8::Reconnect**</span></span>](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





