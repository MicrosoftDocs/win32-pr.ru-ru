---
title: Интерфейс Ивмдрмлиценсеманажемент
description: Интерфейс Ивмдрмлиценсеманажемент предоставляет методы, выполняющие общие операции, связанные с локальным хранилищем лицензий. Чтобы получить экземпляр этого интерфейса, вызовите Ивмдрмпровидер CreateObject. Передайте IID \_ ивмдрмлиценсеманажемент в качестве параметра riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Формат Windows Media в интерфейсе Ивмдрмлиценсеманажемент
- Ивмдрмлиценсеманажемент интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63baeeb46baa877ccc294d1136351ec123d6c4661ee73d548b62d8cb4db05734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027552"
---
# <a name="iwmdrmlicensemanagement-interface"></a>Интерфейс Ивмдрмлиценсеманажемент

Интерфейс **ивмдрмлиценсеманажемент** предоставляет методы, выполняющие общие операции, связанные с локальным хранилищем лицензий.

Чтобы получить экземпляр этого интерфейса, вызовите метод [**ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md). Передайте **IID \_ ивмдрмлиценсеманажемент** в качестве параметра *riid* .

## <a name="members"></a>Элементы

Интерфейс **ивмдрмлиценсеманажемент** наследует от [**ивмдрмевентженератор**](iwmdrmeventgenerator.md). **Ивмдрмлиценсеманажемент** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивмдрмлиценсеманажемент** содержит следующие методы.



| Метод                                                                                               | Описание                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Асинхронно получает лицензию по указанному URL-адресу.<br/>                                                      |
| [**баккуплиценсес**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Создает резервную копию лицензий в локальном хранилище лицензий.<br/>                                                 |
| [**клеанлиценсесторе**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Удаляет помеченные лицензии из хранилища лицензий и выполняет дефрагментацию хранилища для повышения производительности.<br/>             |
| [**креателиценсинумератион**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Создает объект перечислителя лицензий, заполненный сведениями о лицензиях на основе значений параметров.<br/>            |
| [**креателиценсеревокатиончалленже**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Создает запрос отзыва лицензии.<br/>                                                                    |
| [**делетелиценсе**](iwmdrmlicensemanagement-deletelicense.md)                                       | Удаляет лицензию из временного локального хранилища лицензий.<br/>                                                    |
| [**мониторлиценсеаккуиситион**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | Инициирует мониторинг процесса получения лицензии.<br/>                                                      |
| [**процесслиценседелетионмессаже**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | Удаляет лицензию, которая была импортирована для содержимого, изначально защищенного с помощью другой системы защиты содержимого.<br/> |
| [**процесслиценсеревокатионреспонсе**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | Отменяет лицензии из локального хранилища лицензий.<br/>                                                               |
| [**ресторелиценсес**](iwmdrmlicensemanagement-restorelicenses.md)                                   | Восстановление ранее резервных копий лицензий.<br/>                                                                      |
| [**сторелиценсе**](iwmdrmlicensemanagement-storelicense.md)                                         | Добавляет лицензию в локальное хранилище лицензий.<br/>                                                                   |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейсы**](drm-interfaces.md)
</dt> <dt>

[**ивмдрмевентженератор**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





