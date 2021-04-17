---
description: 'Освобождает идентификаторы самонастраивающийся (PnP), которые извлекаются методами Ипортабледевицеманажер:: или Ипортабледевицесервицеманажер:: Жетдевицесервицес.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Функция Фрипортабледевицепнпидс (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265678"
---
# <a name="freeportabledevicepnpids-function"></a><span data-ttu-id="690d6-103">Функция Фрипортабледевицепнпидс</span><span class="sxs-lookup"><span data-stu-id="690d6-103">FreePortableDevicePnPIDs function</span></span>

<span data-ttu-id="690d6-104">Вспомогательная функция **фрипортабледевицепнпидс** освобождает идентификаторы Самонастраивающийся (PnP), которые извлекаются методами [**ипортабледевицеманажер::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) или [**ипортабледевицесервицеманажер:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="690d6-104">The **FreePortableDevicePnPIDs** helper function frees the Plug and Play (PnP) identifiers that are retrieved by the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) or [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="690d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="690d6-105">Syntax</span></span>


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a><span data-ttu-id="690d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="690d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="690d6-107">*ппнпидс*</span><span class="sxs-lookup"><span data-stu-id="690d6-107">*pPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="690d6-108">Массив идентификаторов самонастраивающийся (PnP), которые должны быть освобождены.</span><span class="sxs-lookup"><span data-stu-id="690d6-108">The array of Plug and Play (PnP) identifiers to be freed.</span></span>

</dd> <dt>

<span data-ttu-id="690d6-109">*кпнпидс*</span><span class="sxs-lookup"><span data-stu-id="690d6-109">*cPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="690d6-110">Число идентификаторов в массиве, заданном параметром *ппнпидс* .</span><span class="sxs-lookup"><span data-stu-id="690d6-110">The number of identifiers in the array specified by the *pPnPIDs* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="690d6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="690d6-111">Return value</span></span>

<span data-ttu-id="690d6-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="690d6-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="690d6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="690d6-113">Remarks</span></span>

<span data-ttu-id="690d6-114">Приложение отвечает за освобождение массива указателей, которые он выделяет.</span><span class="sxs-lookup"><span data-stu-id="690d6-114">The application is responsible for freeing the array of pointers that it allocates.</span></span>

## <a name="examples"></a><span data-ttu-id="690d6-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="690d6-115">Examples</span></span>


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a><span data-ttu-id="690d6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="690d6-116">Requirements</span></span>



| <span data-ttu-id="690d6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="690d6-117">Requirement</span></span> | <span data-ttu-id="690d6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="690d6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="690d6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="690d6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="690d6-120">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="690d6-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="690d6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="690d6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="690d6-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="690d6-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="690d6-123">Header</span><span class="sxs-lookup"><span data-stu-id="690d6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="690d6-124"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="690d6-124"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




