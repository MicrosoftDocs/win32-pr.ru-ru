---
description: Возвращает тип аппаратного устройства для получения образа Windows (WIA).
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo. Type, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719369"
---
# <a name="deviceinfotype-property"></a><span data-ttu-id="a4bf3-103">DeviceInfo. Type, свойство</span><span class="sxs-lookup"><span data-stu-id="a4bf3-103">DeviceInfo.Type property</span></span>

<span data-ttu-id="a4bf3-104">Возвращает тип аппаратного устройства для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="a4bf3-104">Retrieves the type of Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="a4bf3-105">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a4bf3-105">Possible values are:</span></span>

-   <span data-ttu-id="a4bf3-106">дигиталкамера</span><span class="sxs-lookup"><span data-stu-id="a4bf3-106">DigitalCamera</span></span>
-   <span data-ttu-id="a4bf3-107">Сканер</span><span class="sxs-lookup"><span data-stu-id="a4bf3-107">Scanner</span></span>
-   <span data-ttu-id="a4bf3-108">стреамингвидео</span><span class="sxs-lookup"><span data-stu-id="a4bf3-108">StreamingVideo</span></span>
-   <span data-ttu-id="a4bf3-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a4bf3-109">Default</span></span>

<span data-ttu-id="a4bf3-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a4bf3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bf3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4bf3-111">Syntax</span></span>


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a><span data-ttu-id="a4bf3-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a4bf3-112">Property value</span></span>

<span data-ttu-id="a4bf3-113">Строка, получающая устройство.</span><span class="sxs-lookup"><span data-stu-id="a4bf3-113">String that receives the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4bf3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a4bf3-114">Requirements</span></span>



| <span data-ttu-id="a4bf3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a4bf3-115">Requirement</span></span> | <span data-ttu-id="a4bf3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a4bf3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4bf3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4bf3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4bf3-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a4bf3-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4bf3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4bf3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4bf3-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4bf3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a4bf3-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a4bf3-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4bf3-122"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a4bf3-122"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




