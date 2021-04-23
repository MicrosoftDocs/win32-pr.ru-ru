---
title: Перечисление Транспортстатус
description: Определяет доступное состояние транспорта, определенное правилами UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API потоковой передачи мультимедиа для перечисления Транспортстатус
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718131"
---
# <a name="transportstatus-enumeration"></a><span data-ttu-id="54513-104">Перечисление Транспортстатус</span><span class="sxs-lookup"><span data-stu-id="54513-104">TransportStatus enumeration</span></span>

<span data-ttu-id="54513-105">Определяет доступное состояние транспорта, определенное правилами UPnP.</span><span class="sxs-lookup"><span data-stu-id="54513-105">Defines the available transport status as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="54513-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54513-106">Syntax</span></span>


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a><span data-ttu-id="54513-107">Константы</span><span class="sxs-lookup"><span data-stu-id="54513-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="54513-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="54513-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="54513-109">Ошибочное состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="54513-109">Erroneous device status.</span></span>

</dd> <dt>

<span data-ttu-id="54513-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Хорошо**</span><span class="sxs-lookup"><span data-stu-id="54513-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**</span></span>
</dt> <dd>

<span data-ttu-id="54513-111">Устройство имеет хорошее состояние.</span><span class="sxs-lookup"><span data-stu-id="54513-111">The device is in a good status.</span></span>

</dd> <dt>

<span data-ttu-id="54513-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ерророккурред**</span><span class="sxs-lookup"><span data-stu-id="54513-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span></span>
</dt> <dd>

<span data-ttu-id="54513-113">На устройстве произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="54513-113">An error occurred on the device.</span></span>

</dd> <dt>

<span data-ttu-id="54513-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Последняя**</span><span class="sxs-lookup"><span data-stu-id="54513-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="54513-115">Предыдущее состояние устройства — текущее состояние транспорта.</span><span class="sxs-lookup"><span data-stu-id="54513-115">The device s previous status to the current transport status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54513-116">Требования</span><span class="sxs-lookup"><span data-stu-id="54513-116">Requirements</span></span>



| <span data-ttu-id="54513-117">Требование</span><span class="sxs-lookup"><span data-stu-id="54513-117">Requirement</span></span> | <span data-ttu-id="54513-118">Значение</span><span class="sxs-lookup"><span data-stu-id="54513-118">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54513-119">IDL</span><span class="sxs-lookup"><span data-stu-id="54513-119">IDL</span></span><br/> | <dl> <span data-ttu-id="54513-120"><dt>Windows. Media. Streaming. idl (Reference Windows. Media. Streaming. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="54513-120"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





