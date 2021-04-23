---
description: Извлекает следующий один или несколько объектов Ипортабледевицеконнектор в последовательности перечисления.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: 'Метод Иенумпортабледевицеконнекторс:: Next (Девпкэй. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 709e938c28f9bf09e34d918eea7be3029c7a11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712789"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a><span data-ttu-id="a3efe-103">Метод Иенумпортабледевицеконнекторс:: Next</span><span class="sxs-lookup"><span data-stu-id="a3efe-103">IEnumPortableDeviceConnectors::Next method</span></span>

<span data-ttu-id="a3efe-104">**Следующий** метод извлекает следующий один или несколько объектов [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="a3efe-104">The **Next** method retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3efe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3efe-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="a3efe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3efe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3efe-107">*крекуестед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3efe-107">*cRequested* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3efe-108">Число запрошенных устройств.</span><span class="sxs-lookup"><span data-stu-id="a3efe-108">The number of requested devices.</span></span> <span data-ttu-id="a3efe-109">Это значение также указывает количество элементов в выделенном вызывающем объекте массиве, заданном параметром *пконнекторс* .</span><span class="sxs-lookup"><span data-stu-id="a3efe-109">This value also indicates the number of elements in the caller-allocated array specified by the *pConnectors* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a3efe-110">*пконнекторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a3efe-110">*pConnectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3efe-111">Массив указателей [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , каждый из которых указывает парное устройство MTP Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="a3efe-111">An array of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) pointers, each specifying a paired MTP Bluetooth device.</span></span> <span data-ttu-id="a3efe-112">Вызывающий объект должен выделить массив **ипортабледевицеконнекторных** указателей с длиной массива, заданной параметром *крекуестед* .</span><span class="sxs-lookup"><span data-stu-id="a3efe-112">The caller must allocate an array of **IPortableDeviceConnector** pointers, with the array length specified by the *cRequested* parameter.</span></span> <span data-ttu-id="a3efe-113">При успешном возвращении вызывающий объект должен освободить как массив, так и возвращаемые указатели.</span><span class="sxs-lookup"><span data-stu-id="a3efe-113">On successful return, the caller must free both the array and the returned pointers.</span></span> <span data-ttu-id="a3efe-114">Интерфейсы **ипортабледевицеконнектор** освобождаются путем вызова метода **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="a3efe-114">The **IPortableDeviceConnector** interfaces are freed by calling the **IUnknown::Release** method.</span></span>

</dd> <dt>

<span data-ttu-id="a3efe-115">*пкфетчед* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a3efe-115">*pcFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3efe-116">Число фактически извлеченных интерфейсов [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) .</span><span class="sxs-lookup"><span data-stu-id="a3efe-116">The number of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces that are actually retrieved.</span></span> <span data-ttu-id="a3efe-117">Если ни один из интерфейсов **ипортабледевицеконнектор** не извлекается и возвращаемое значение равно **\_ false**, то больше нет интерфейсов **ипортабледевицеконнектор** для перечисления.</span><span class="sxs-lookup"><span data-stu-id="a3efe-117">If no **IPortableDeviceConnector** interfaces are retrieved and the return value is **S\_FALSE**, there are no more **IPortableDeviceConnector** interfaces to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3efe-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3efe-118">Return value</span></span>

<span data-ttu-id="a3efe-119">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a3efe-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a3efe-120">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a3efe-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a3efe-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a3efe-121">Return code</span></span>                                                                             | <span data-ttu-id="a3efe-122">Описание</span><span class="sxs-lookup"><span data-stu-id="a3efe-122">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3efe-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a3efe-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a3efe-124">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a3efe-124">The method succeeded.</span></span><br/>                                 |
| <dl> <span data-ttu-id="a3efe-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a3efe-125"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a3efe-126">Отсутствуют устройства MTP Bluetooth для перечисления.</span><span class="sxs-lookup"><span data-stu-id="a3efe-126">There are no more MTP Bluetooth devices to enumerate.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="a3efe-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="a3efe-127">Examples</span></span>

<span data-ttu-id="a3efe-128">В следующем примере демонстрируется использование этого метода для перечисления связанных устройств MTP/Bluetooth и отправки асинхронного запроса на соединение каждому.</span><span class="sxs-lookup"><span data-stu-id="a3efe-128">The following example demonstrates the use of this method to enumerate paired MTP/Bluetooth devices, and to send an asynchronous connection request to each.</span></span>


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a><span data-ttu-id="a3efe-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a3efe-129">Requirements</span></span>



| <span data-ttu-id="a3efe-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a3efe-130">Requirement</span></span> | <span data-ttu-id="a3efe-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a3efe-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3efe-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3efe-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a3efe-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a3efe-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="a3efe-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3efe-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a3efe-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a3efe-135">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="a3efe-136">Header</span><span class="sxs-lookup"><span data-stu-id="a3efe-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3efe-137"><dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3efe-137"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="a3efe-138">IDL</span><span class="sxs-lookup"><span data-stu-id="a3efe-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3efe-139"><dt>Портабледевицеконнектапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3efe-139"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="a3efe-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3efe-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3efe-141"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3efe-141"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="a3efe-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3efe-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3efe-143">**иенумпортабледевицеконнекторс**</span><span class="sxs-lookup"><span data-stu-id="a3efe-143">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




