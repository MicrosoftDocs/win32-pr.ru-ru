---
description: Событие, возникающее при подключении нового аппаратного устройства для получения образа Windows (WIA).
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Событие WIA. Ондевицеконнектед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264540"
---
# <a name="wiaondeviceconnected-event"></a><span data-ttu-id="6ecb4-103">Событие WIA. Ондевицеконнектед</span><span class="sxs-lookup"><span data-stu-id="6ecb4-103">Wia.OnDeviceConnected event</span></span>

<span data-ttu-id="6ecb4-104">Событие, возникающее при подключении нового аппаратного устройства для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="6ecb4-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ecb4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ecb4-105">Syntax</span></span>


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="6ecb4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ecb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ecb4-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="6ecb4-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="6ecb4-108">Строка, содержащая идентификатор подключенного устройства.</span><span class="sxs-lookup"><span data-stu-id="6ecb4-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ecb4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ecb4-109">Return value</span></span>

<span data-ttu-id="6ecb4-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6ecb4-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ecb4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ecb4-111">Remarks</span></span>

<span data-ttu-id="6ecb4-112">WIA уведомляет сценарий или приложение при подключении нового аппаратного устройства к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="6ecb4-112">WIA notifies the script or application whenever a new hardware device is connected to the computer.</span></span> <span data-ttu-id="6ecb4-113">Реализуйте  \_ подпрограммы обжвиа **ондевицеконнектед ()** , чтобы сценарий или приложение отвечало на подключение устройства.</span><span class="sxs-lookup"><span data-stu-id="6ecb4-113">Implement the **objWia**\_**OnDeviceConnected()** subroutine to allow the script or application to respond to the device connection.</span></span>

<span data-ttu-id="6ecb4-114">Например, может потребоваться, чтобы скрипт обновлял коллекцию [**устройств**](-wia-iwia-devices.md) при установке нового устройства.</span><span class="sxs-lookup"><span data-stu-id="6ecb4-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a new device is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ecb4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6ecb4-115">Requirements</span></span>



| <span data-ttu-id="6ecb4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6ecb4-116">Requirement</span></span> | <span data-ttu-id="6ecb4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6ecb4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecb4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ecb4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ecb4-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ecb4-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ecb4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ecb4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ecb4-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ecb4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6ecb4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6ecb4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ecb4-123"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb4-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




