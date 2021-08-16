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
ms.openlocfilehash: 868f13f220dbd5d5867e5ee2bbb54c1ef946e267d87e9ea0aa625108b945d537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697299"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a>Метод Иенумпортабледевицеконнекторс:: Next

**Следующий** метод извлекает следующий один или несколько объектов [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) в последовательности перечисления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*крекуестед* \[ окне\]
</dt> <dd>

Число запрошенных устройств. Это значение также указывает количество элементов в выделенном вызывающем объекте массиве, заданном параметром *пконнекторс* .

</dd> <dt>

*пконнекторс* \[ заполняет\]
</dt> <dd>

массив [**ипортабледевицеконнекторных**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) указателей, каждый из которых указывает парное устройство MTP Bluetooth. Вызывающий объект должен выделить массив **ипортабледевицеконнекторных** указателей с длиной массива, заданной параметром *крекуестед* . При успешном возвращении вызывающий объект должен освободить как массив, так и возвращаемые указатели. Интерфейсы **ипортабледевицеконнектор** освобождаются путем вызова метода **IUnknown:: Release** .

</dd> <dt>

*пкфетчед* \[ в, out\]
</dt> <dd>

Число фактически извлеченных интерфейсов [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) . Если ни один из интерфейсов **ипортабледевицеконнектор** не извлекается и возвращаемое значение равно **\_ false**, то больше нет интерфейсов **ипортабледевицеконнектор** для перечисления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                             | Описание                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | Метод выполнен успешно.<br/>                                 |
| <dl> <dt>**S \_ false**</dt> </dl> | для перечисления больше не Bluetooth устройств MTP.<br/> |



 

## <a name="examples"></a>Примеры

в следующем примере демонстрируется использование этого метода для перечисления связанных устройств MTP/Bluetooth и отправки асинхронного запроса на соединение каждому.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                                                                             |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Портабледевицеконнектапи. idl</dt> </dl>                                                                |
| Библиотека<br/>                  | <dl> <dt>Портабледевицегуидс. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иенумпортабледевицеконнекторс**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




