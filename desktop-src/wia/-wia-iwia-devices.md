---
description: Коллекция объектов DeviceInfo, представляющих все устройства, установленные на компьютере.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Свойство WIA. Devices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d03aa0b7e73d5dfbc6449816f3b64147e51db882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711253"
---
# <a name="wiadevices-property"></a><span data-ttu-id="63577-103">Свойство WIA. Devices</span><span class="sxs-lookup"><span data-stu-id="63577-103">Wia.Devices property</span></span>

<span data-ttu-id="63577-104">Коллекция объектов [**DeviceInfo**](-wia-deviceinfo.md) , представляющих все устройства, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="63577-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="63577-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63577-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="63577-106">Эта коллекция основана на 0.</span><span class="sxs-lookup"><span data-stu-id="63577-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="63577-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63577-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63577-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63577-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="63577-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="63577-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="63577-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="63577-110">Examples</span></span>

<span data-ttu-id="63577-111">В следующем примере показано использование коллекции **устройств** для перечисления устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="63577-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="63577-112">Требования</span><span class="sxs-lookup"><span data-stu-id="63577-112">Requirements</span></span>



| <span data-ttu-id="63577-113">Требование</span><span class="sxs-lookup"><span data-stu-id="63577-113">Requirement</span></span> | <span data-ttu-id="63577-114">Значение</span><span class="sxs-lookup"><span data-stu-id="63577-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63577-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63577-115">Minimum supported client</span></span><br/> | <span data-ttu-id="63577-116">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="63577-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63577-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63577-117">Minimum supported server</span></span><br/> | <span data-ttu-id="63577-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63577-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="63577-119">DLL</span><span class="sxs-lookup"><span data-stu-id="63577-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63577-120"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="63577-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




