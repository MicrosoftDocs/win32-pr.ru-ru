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
ms.openlocfilehash: b4d98bfe1552156071efde0b46899ad058e75aec
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841316"
---
# <a name="wiadevices-property"></a><span data-ttu-id="74fd7-103">Свойство WIA. Devices</span><span class="sxs-lookup"><span data-stu-id="74fd7-103">Wia.Devices property</span></span>

<span data-ttu-id="74fd7-104">Коллекция объектов [**DeviceInfo**](-wia-deviceinfo.md) , представляющих все устройства, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="74fd7-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="74fd7-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="74fd7-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="74fd7-106">Эта коллекция основана на 0.</span><span class="sxs-lookup"><span data-stu-id="74fd7-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="74fd7-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="74fd7-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="74fd7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74fd7-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="74fd7-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="74fd7-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="74fd7-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="74fd7-110">Examples</span></span>

<span data-ttu-id="74fd7-111">В следующем примере показано использование коллекции **устройств** для перечисления устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="74fd7-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="74fd7-112">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="74fd7-112">Requirements</span></span>



| <span data-ttu-id="74fd7-113">Требование</span><span class="sxs-lookup"><span data-stu-id="74fd7-113">Requirement</span></span> | <span data-ttu-id="74fd7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="74fd7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74fd7-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74fd7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="74fd7-116">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="74fd7-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74fd7-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74fd7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="74fd7-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74fd7-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="74fd7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="74fd7-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74fd7-120"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="74fd7-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




