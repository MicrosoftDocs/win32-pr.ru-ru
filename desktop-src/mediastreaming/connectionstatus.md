---
title: Перечисление ConnectionStatus
description: Представляет состояние устройства в сети как Последнее появление.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- API потоковой передачи мультимедиа для перечисления ConnectionStatus
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717919"
---
# <a name="connectionstatus-enumeration"></a><span data-ttu-id="32c9c-104">Перечисление ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="32c9c-104">ConnectionStatus enumeration</span></span>

<span data-ttu-id="32c9c-105">Представляет состояние устройства в сети как Последнее появление.</span><span class="sxs-lookup"><span data-stu-id="32c9c-105">Represents the state of the device in the network as last seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c9c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32c9c-106">Syntax</span></span>


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a><span data-ttu-id="32c9c-107">Константы</span><span class="sxs-lookup"><span data-stu-id="32c9c-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="32c9c-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Онлайн**</span><span class="sxs-lookup"><span data-stu-id="32c9c-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**</span></span>
</dt> <dd>

<span data-ttu-id="32c9c-109">Устройство подключено и активно в сети.</span><span class="sxs-lookup"><span data-stu-id="32c9c-109">Device is online and active on the network.</span></span>

</dd> <dt>

<span data-ttu-id="32c9c-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Работа**</span><span class="sxs-lookup"><span data-stu-id="32c9c-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**</span></span>
</dt> <dd>

<span data-ttu-id="32c9c-111">устройство вне сети;</span><span class="sxs-lookup"><span data-stu-id="32c9c-111">Device is offline.</span></span>

</dd> <dt>

<span data-ttu-id="32c9c-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Сна**</span><span class="sxs-lookup"><span data-stu-id="32c9c-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Sleeping**</span></span>
</dt> <dd>

<span data-ttu-id="32c9c-113">Устройство находится в автономном режиме, но может автоматически выходить из системы при попытке взаимодействия с ним.</span><span class="sxs-lookup"><span data-stu-id="32c9c-113">Device is currently offline but might automatically wake up when an attempt is made to communicate with it.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32c9c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="32c9c-114">Requirements</span></span>



| <span data-ttu-id="32c9c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="32c9c-115">Requirement</span></span> | <span data-ttu-id="32c9c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="32c9c-116">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c9c-117">IDL</span><span class="sxs-lookup"><span data-stu-id="32c9c-117">IDL</span></span><br/> | <dl> <span data-ttu-id="32c9c-118"><dt>Windows. Media. Streaming. idl (Reference Windows. Media. Streaming. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="32c9c-118"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





