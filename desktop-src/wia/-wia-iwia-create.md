---
description: Метод Create объекта WIA устанавливает соединение с указанным устройством для получения образа Windows (WIA) и возвращает объект Item, представляющий устройство.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Метод WIA. Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d22d45e473cec1d5186c300f97cbdb4661237ab9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841335"
---
# <a name="wiacreate-method"></a><span data-ttu-id="9f765-103">Метод WIA. Create</span><span class="sxs-lookup"><span data-stu-id="9f765-103">Wia.Create method</span></span>

<span data-ttu-id="9f765-104">Метод **CREATE** объекта [**WIA**](-wia-wia.md) устанавливает соединение с указанным устройством для получения образа Windows (WIA) и возвращает объект [**Item**](-wia-item.md) , представляющий устройство.</span><span class="sxs-lookup"><span data-stu-id="9f765-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f765-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f765-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="9f765-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f765-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f765-107">*Устройство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f765-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f765-108">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="9f765-108">Type: **VARIANT\***</span></span>

<span data-ttu-id="9f765-109">Указывает устройство WIA, к которому необходимо подключиться.</span><span class="sxs-lookup"><span data-stu-id="9f765-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f765-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f765-110">Return value</span></span>

<span data-ttu-id="9f765-111">Тип: **ивиадиспатчитем**</span><span class="sxs-lookup"><span data-stu-id="9f765-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="9f765-112">В случае успешного выполнения этот метод возвращает объект [**Item**](-wia-item.md) , представляющий аппаратное устройство WIA (корневой элемент).</span><span class="sxs-lookup"><span data-stu-id="9f765-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f765-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="9f765-113">Remarks</span></span>

<span data-ttu-id="9f765-114">Параметр *Device* указывает объект [**DeviceInfo**](-wia-deviceinfo.md) , передавая сам объект, его индекс из объекта Collection или значение свойства [**ID**](-wia-iwiadeviceinfo-id.md) .</span><span class="sxs-lookup"><span data-stu-id="9f765-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="9f765-115">**Ничего не** передавать, чтобы отобразить диалоговое окно, позволяющее пользователю выбрать устройство.</span><span class="sxs-lookup"><span data-stu-id="9f765-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="9f765-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="9f765-116">Examples</span></span>

<span data-ttu-id="9f765-117">В следующих примерах на языке VBScript показано использование метода **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="9f765-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="9f765-118">В первом примере объект [**DeviceInfo**](-wia-deviceinfo.md) передается в метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="9f765-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="9f765-119">Обратите внимание, что передача свойства [**ID**](-wia-iwiadeviceinfo-id.md) объекта вызывает точно такое же поведение.</span><span class="sxs-lookup"><span data-stu-id="9f765-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



<span data-ttu-id="9f765-120">В следующем примере вызывающее приложение передает индекс объекта [**DeviceInfo**](-wia-deviceinfo.md) в коллекции в метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="9f765-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



<span data-ttu-id="9f765-121">В следующем примере **ничего не** передается в метод **CREATE** , чтобы отобразить диалоговое окно, позволяющее пользователю выбрать устройство.</span><span class="sxs-lookup"><span data-stu-id="9f765-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="9f765-122">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="9f765-122">Requirements</span></span>



| <span data-ttu-id="9f765-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9f765-123">Requirement</span></span> | <span data-ttu-id="9f765-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9f765-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f765-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f765-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9f765-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9f765-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f765-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f765-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9f765-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f765-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9f765-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9f765-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f765-130"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9f765-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




