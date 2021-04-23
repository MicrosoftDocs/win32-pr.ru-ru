---
description: Метод Create объекта DeviceInfo устанавливает соединение с устройством получения образа Windows (WIA), заданным объектом DeviceInfo, и возвращает объект Item, представляющий устройство.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: DeviceInfo. Create, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719376"
---
# <a name="deviceinfocreate-method"></a><span data-ttu-id="e01d9-103">DeviceInfo. Create, метод</span><span class="sxs-lookup"><span data-stu-id="e01d9-103">DeviceInfo.Create method</span></span>

<span data-ttu-id="e01d9-104">Метод **CREATE** объекта [**DeviceInfo**](-wia-deviceinfo.md) устанавливает соединение с устройством получения образа Windows (WIA), заданным объектом **DeviceInfo** , и возвращает объект [**Item**](-wia-item.md) , представляющий устройство.</span><span class="sxs-lookup"><span data-stu-id="e01d9-104">The **Create** method of the [**DeviceInfo**](-wia-deviceinfo.md) object makes a connection to the Windows Image Acquisition (WIA) device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e01d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e01d9-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a><span data-ttu-id="e01d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e01d9-106">Parameters</span></span>

<span data-ttu-id="e01d9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e01d9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e01d9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e01d9-108">Return value</span></span>

<span data-ttu-id="e01d9-109">Тип: **ивиадиспатчитем**</span><span class="sxs-lookup"><span data-stu-id="e01d9-109">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="e01d9-110">Этот метод возвращает объект [**Item**](-wia-item.md) , представляющий созданное устройство.</span><span class="sxs-lookup"><span data-stu-id="e01d9-110">This method returns the [**Item**](-wia-item.md) object that represents the device that is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="e01d9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e01d9-111">Remarks</span></span>

<span data-ttu-id="e01d9-112">Используйте метод **CREATE** , чтобы создать подключение к аппаратному устройству WIA после перечисления коллекции [**устройств**](-wia-iwia-devices.md) .</span><span class="sxs-lookup"><span data-stu-id="e01d9-112">Use the **Create** method to create a connection to a WIA hardware device after enumerating the [**Devices**](-wia-iwia-devices.md) collection.</span></span> <span data-ttu-id="e01d9-113">Метод возвращает объект [**Item**](-wia-item.md) , представляющий устройство (корневой элемент).</span><span class="sxs-lookup"><span data-stu-id="e01d9-113">The method returns an [**Item**](-wia-item.md) object that represents the device (a root item).</span></span>

## <a name="examples"></a><span data-ttu-id="e01d9-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="e01d9-114">Examples</span></span>

<span data-ttu-id="e01d9-115">В следующем примере демонстрируется использование метода **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="e01d9-115">The following example demonstrates the use of the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="e01d9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e01d9-116">Requirements</span></span>



| <span data-ttu-id="e01d9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e01d9-117">Requirement</span></span> | <span data-ttu-id="e01d9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e01d9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e01d9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e01d9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e01d9-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e01d9-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e01d9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e01d9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e01d9-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e01d9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e01d9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e01d9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e01d9-124"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="e01d9-124"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




