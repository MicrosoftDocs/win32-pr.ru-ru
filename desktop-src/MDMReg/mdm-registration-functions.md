---
title: Функции регистрации MDM
description: Следующие функции объявляются в `mdmregistration.h` и используются при регистрации MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/19/2020
ms.openlocfilehash: f9149c4bd2f9f931a506dc35d05b5e1c641dc87445fbf88fd73ff9ad20ac514b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040374"
---
# <a name="mdm-registration-functions"></a>Функции регистрации MDM

Следующие функции объявляются в `mdmregistration.h` и используются при регистрации MDM.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**дисковерманажементсервице**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementservice) | Обнаружение службы MDM. |
| [**дисковерманажементсервицеекс**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex) | Обнаружение службы MDM с помощью сервера-кандидата. |
| [**жетдевицеманажементконфигинфо**](/windows/win32/api/mdmregistration/nf-mdmregistration-getdevicemanagementconfiginfo) | Возвращает сведения о конфигурации, связанные с ИДЕНТИФИКАТОРом поставщика. |
| [**жетдевицерегистратионинфо**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo) | Извлекает сведения о регистрации устройства. |
| [**жетманажементапфиперлинк**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink) | Извлекает гиперссылку приложения управления, связанной со службой MDM. |
| [**исдевицерегистередвисманажемент**](/windows/win32/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement) | Проверяет, зарегистрировано ли устройство в службе MDM. |
| [**исманажементрегистратионалловед**](/windows/win32/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed) | Проверяет, разрешена ли регистрация MDM локальной политикой. |
| [**регистердевицевисманажемент**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement) | Регистрирует устройство в службе MDM, используя [ \[ протокол MS-MDE \] : Mobile Device](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267)Register. |
| [**регистердевицевисманажементусингаадкредентиалс**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials) | регистрирует устройство в службе MDM, используя учетные данные Azure Active Directory (AAD). |
| [**сетдевицеманажементконфигинфо**](/windows/win32/api/mdmregistration/nf-mdmregistration-setdevicemanagementconfiginfo) | Задает сведения о конфигурации, связанные с ИДЕНТИФИКАТОРом поставщика. |
| [**сетманажедекстерналли**](/windows/win32/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) | Указывает агенту MDM, что устройство управляется извне и не регистрируется в службе MDM. |
| [**унрегистердевицевисманажемент**](/windows/win32/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement) | Отменяет регистрацию устройства в службе MDM. |

## <a name="related-topics"></a>Связанные темы

* [Справочник по регистрации MDM](./mdm-registration-reference.md)
