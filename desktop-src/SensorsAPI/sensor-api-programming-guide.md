---
description: В этом разделе содержатся сведения, включая пример кода, о том, как использовать функции датчика API. Общие сведения о различных программных интерфейсах см. в разделе об API датчика.
ms.assetid: 4c2ffd22-49ee-4318-bfa0-e0ce4d8c67bb
title: Программное руководством по программированию API датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5886564e66a0a8db64713b280b44f85a197430dc23523266bc45e66e44c956b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073244"
---
# <a name="sensor-api-programming-guide"></a>Программное руководством по программированию API датчика

В этом разделе содержатся сведения, включая пример кода, о том, как использовать функции датчика API. Общие сведения о различных программных интерфейсах см. [в разделе об API датчика](about-the-sensor-api.md).

В примере кода в этом разделе используются следующие дополнительные включаемые заголовки.


```C++
#include <windows.h>
#include <initguid.h>
#include <propkeydef.h>


#include <iostream>
#include <propvarutil.h>
#include <functiondiscoverykeys.h>
#include <assert.h>
```





Также необходимо создать ссылку на эти дополнительные связанные файлы библиотеки: Пропсис. lib и Портабледевицегуидс. lib.

В примере кода в этом разделе используются следующие константы для категорий датчиков, типов и полей данных. эти константы представляют собой пользовательские значения, которые определяются образцом драйвера тимесенсор в наборе драйверов Windows. Обратите внимание, что, хотя платформа датчика позволяет определять и использовать пользовательские типы, такие как, следует использовать типы, определяемые платформой, когда это возможно.


```C++
// Define an object ID.
// {0D77BEE3-7169-42bf-8379-28F9A9B59A57}
DEFINE_GUID(SAMPLE_SENSOR_TIME_ID, 
0xd77bee3, 0x7169, 0x42bf, 0x83, 0x79, 0x28, 0xf9, 0xa9, 0xb5, 0x9a, 0x57);

// Define a custom category.
// {062A5C3B-44C1-4ad1-8EFC-0F65B2E4AD48}
DEFINE_GUID(SAMPLE_SENSOR_CATEGORY_DATE_TIME, 
0x62a5c3b, 0x44c1, 0x4ad1, 0x8e, 0xfc, 0xf, 0x65, 0xb2, 0xe4, 0xad, 0x48);

// Define a custom type.
// {5F199A84-409F-4e35-B2DD-F9C79F5318A0}
DEFINE_GUID(SAMPLE_SENSOR_TYPE_TIME, 
0x5f199a84, 0x409f, 0x4e35, 0xb2, 0xdd, 0xf9, 0xc7, 0x9f, 0x53, 0x18, 0xa0);

// Time sensor fields.
// Because these are related, each field uses the same GUID, but changes the PID.
// {340946F2-9A77-42b0-8176-57D4DF00E5CA}
DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_HOUR, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE); // PID = 2

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_MINUTE, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 1); // PID = 3

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_SECOND, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 2); // PID = 4
```



В примере кода в этом разделе используются следующие переменные.


```C++
HRESULT hr = S_OK;

// Sensor interface pointers
ISensorManager* pSensorManager = NULL;    
ISensorCollection* pSensorColl = NULL;
ISensor* pSensor = NULL; 
ISensorDataReport* pReport = NULL;

// Time sensor data field variables
ULONG ulHour, ulMinute, ulSecond = 0;

```



В примере кода в этом разделе для освобождения указателей на COM-интерфейс используется следующая функция.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="in-this-section"></a>В этом разделе

-   [Получение объекта датчика](retrieving-a-sensor.md)
-   [Запрос разрешений пользователя](requesting-user-permissions.md)
-   [Извлечение и задание свойств датчика](setting-and-retrieving-sensor-properties.md)
-   [Проверка поддерживаемых полей данных датчика](checking-for-supported-sensor-data-fields.md)
-   [Использование событий API датчика](using-sensor-api-events.md)
-   [Получение значений данных датчика](retrieving-sensor-data-fields.md)
-   [Получение типов векторов](retrieving-vector-types.md)
-   [Использование логических датчиков](using-logical-sensors.md)
-   [Создание пользовательских интерфейсов Light-Aware](creating-light-aware-user-interfaces.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об API датчика](about-the-sensor-api.md)
</dt> </dl>

 

 



