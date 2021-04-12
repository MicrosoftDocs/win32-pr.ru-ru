---
description: Событие, возникающее при отключении нового аппаратного устройства для получения образа Windows (WIA).
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Событие WIA. Ондевицедисконнектед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264539"
---
# <a name="wiaondevicedisconnected-event"></a><span data-ttu-id="a6f2d-103">Событие WIA. Ондевицедисконнектед</span><span class="sxs-lookup"><span data-stu-id="a6f2d-103">Wia.OnDeviceDisconnected event</span></span>

<span data-ttu-id="a6f2d-104">Событие, возникающее при отключении нового аппаратного устройства для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="a6f2d-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is disconnected.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6f2d-105">Syntax</span></span>


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="a6f2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6f2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f2d-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="a6f2d-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="a6f2d-108">Строка, содержащая идентификатор подключенного устройства.</span><span class="sxs-lookup"><span data-stu-id="a6f2d-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f2d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6f2d-109">Return value</span></span>

<span data-ttu-id="a6f2d-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a6f2d-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f2d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6f2d-111">Remarks</span></span>

<span data-ttu-id="a6f2d-112">WIA уведомляет сценарий или приложение каждый раз при отключении аппаратного устройства от компьютера.</span><span class="sxs-lookup"><span data-stu-id="a6f2d-112">WIA notifies the script or application whenever a hardware device is disconnected from the computer.</span></span> <span data-ttu-id="a6f2d-113">Реализуйте  \_ подпрограммы обжвиа **ондевицедисконнектед ()** , чтобы разрешить сценарию или приложению отвечать на отключение устройства.</span><span class="sxs-lookup"><span data-stu-id="a6f2d-113">Implement the **objWia**\_**OnDeviceDisconnected()** subroutine to allow the script or application to respond to the device disconnection.</span></span>

<span data-ttu-id="a6f2d-114">Например, может потребоваться, чтобы скрипт обновлял коллекцию [**устройств**](-wia-iwia-devices.md) при удалении устройства с компьютера.</span><span class="sxs-lookup"><span data-stu-id="a6f2d-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a device is removed from the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f2d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a6f2d-115">Requirements</span></span>



| <span data-ttu-id="a6f2d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a6f2d-116">Requirement</span></span> | <span data-ttu-id="a6f2d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a6f2d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f2d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6f2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f2d-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6f2d-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6f2d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6f2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f2d-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6f2d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a6f2d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a6f2d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6f2d-123"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a6f2d-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




