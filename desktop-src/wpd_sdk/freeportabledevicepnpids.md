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
ms.openlocfilehash: 150796912d2796a2697d3c088963c20e1523288f5a1301e9467a6859845db68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590322"
---
# <a name="freeportabledevicepnpids-function"></a>Функция Фрипортабледевицепнпидс

Вспомогательная функция **фрипортабледевицепнпидс** освобождает идентификаторы Самонастраивающийся (PnP), которые извлекаются методами [**ипортабледевицеманажер::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) или [**ипортабледевицесервицеманажер:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .

## <a name="syntax"></a>Синтаксис


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппнпидс* 
</dt> <dd>

Массив идентификаторов самонастраивающийся (PnP), которые должны быть освобождены.

</dd> <dt>

*кпнпидс* 
</dt> <dd>

Число идентификаторов в массиве, заданном параметром *ппнпидс* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Приложение отвечает за освобождение массива указателей, которые он выделяет.

## <a name="examples"></a>Примеры


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Заголовок<br/>                   | <dl> <dt>Портабледевице. h</dt> </dl> |



 

 




