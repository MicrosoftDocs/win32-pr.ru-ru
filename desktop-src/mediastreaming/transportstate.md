---
title: Перечисление Транспортстате
description: Определяет доступные состояния транспорта, определенные правилами UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API потоковой передачи мультимедиа для перечисления Транспортстате
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718132"
---
# <a name="transportstate-enumeration"></a><span data-ttu-id="b1c31-104">Перечисление Транспортстате</span><span class="sxs-lookup"><span data-stu-id="b1c31-104">TransportState enumeration</span></span>

<span data-ttu-id="b1c31-105">Определяет доступные состояния транспорта, определенные правилами UPnP.</span><span class="sxs-lookup"><span data-stu-id="b1c31-105">Defines the available transport states as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1c31-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1c31-106">Syntax</span></span>


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a><span data-ttu-id="b1c31-107">Константы</span><span class="sxs-lookup"><span data-stu-id="b1c31-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1c31-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="b1c31-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="b1c31-109">Ошибочное состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b1c31-109">Erroneous device state.</span></span>

</dd> <dt>

<span data-ttu-id="b1c31-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлена**</span><span class="sxs-lookup"><span data-stu-id="b1c31-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped**</span></span>
</dt> <dd>

<span data-ttu-id="b1c31-111">Транспорт устройства находится в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b1c31-111">The device s transport is in a stopped state.</span></span>

</dd> <dt>

<span data-ttu-id="b1c31-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Игре**</span><span class="sxs-lookup"><span data-stu-id="b1c31-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Playing**</span></span>
</dt> <dd>

<span data-ttu-id="b1c31-113">Транспорт устройства находится в воспроизводимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="b1c31-113">The device s transport is in a playing state.</span></span>

</dd> <dt>

<span data-ttu-id="b1c31-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход**</span><span class="sxs-lookup"><span data-stu-id="b1c31-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning**</span></span>
</dt> <dd>

<span data-ttu-id="b1c31-115">Транспорт устройства находится в состоянии перехода, что приведет к другому значению состояния.</span><span class="sxs-lookup"><span data-stu-id="b1c31-115">The device s transport is in a transitioning state which will result in another state value.</span></span>

</dd> <dt>

<span data-ttu-id="b1c31-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлена**</span><span class="sxs-lookup"><span data-stu-id="b1c31-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused**</span></span>
</dt> <dd>

<span data-ttu-id="b1c31-117">Транспортное устройство s находится в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b1c31-117">The device s transport is in a paused state.</span></span>

</dd> <dt>

<span data-ttu-id="b1c31-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Запись**</span><span class="sxs-lookup"><span data-stu-id="b1c31-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Recording**</span></span>
</dt> <dd>

<span data-ttu-id="b1c31-119">Транспорт устройства находится в состоянии записи.</span><span class="sxs-lookup"><span data-stu-id="b1c31-119">The device s transport is in a recording state.</span></span>

</dd> <dt>

<span data-ttu-id="b1c31-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**номедиапресент**</span><span class="sxs-lookup"><span data-stu-id="b1c31-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span></span>
</dt> <dd>

<span data-ttu-id="b1c31-121">Для транспорта устройства не задан универсальный код ресурса (URI) для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b1c31-121">The device s transport does not have an URI set for playback.</span></span>

</dd> <dt>

<span data-ttu-id="b1c31-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Последняя**</span><span class="sxs-lookup"><span data-stu-id="b1c31-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="b1c31-123">Предыдущее состояние устройства в текущее состояние транспорта.</span><span class="sxs-lookup"><span data-stu-id="b1c31-123">The device s previous state to the current transport state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1c31-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b1c31-124">Requirements</span></span>



| <span data-ttu-id="b1c31-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b1c31-125">Requirement</span></span> | <span data-ttu-id="b1c31-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b1c31-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c31-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b1c31-127">IDL</span></span><br/> | <dl> <span data-ttu-id="b1c31-128"><dt>Windows. Media. Streaming. idl (Reference Windows. Media. Streaming. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="b1c31-128"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





