---
title: Функции динамических ключевых слов брандмауэра
description: Динамические ключевые слова брандмауэра содержат следующие функции.
keywords:
- Динамические ключевые слова брандмауэра, функции
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: d086c3aeb3caf7ff85a7fceeec17943c7112a7e0
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "112681188"
---
# <a name="firewall-dynamic-keywords-functions"></a>Функции динамических ключевых слов брандмауэра

Динамические ключевые слова брандмауэра содержат следующие функции.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | Запрашивает доставку уведомлений об изменениях определенных объектов динамических адресов ключевых слов ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)). |
| [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | Отменяет доставку уведомлений об изменениях определенных объектов динамических адресов ключевых слов ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)). |
| [**PFN_FWADDDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | Тип указателя функции точки входа в службе, вызываемой для добавления указанного динамического адреса ключевого слова. |
| [**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | Тип указателя функции точки входа в службе, вызываемой для удаления динамического адреса ключевого слова с указанным ИДЕНТИФИКАТОРом. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | Тип указателя функции точки входа в службе, вызываемой для перечисления конкретных динамических адресов ключевых слов по ИДЕНТИФИКАТОРу. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | Тип указателя функции точки входа в службе, вызываемой для перечисления динамических адресов ключевых слов по типу. Можно запросить определенное подмножество объектов на основе переданных флагов перечисления. |
| [**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | Тип указателя функции точки входа в службе, которая вызывается для освобождения динамических структур данных адреса ключевого слова, выделенных службой. |
| [**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | Тип указателя функции точки входа в службе, которая вызывается для обновления динамического адреса ключевого слова с входным ИДЕНТИФИКАТОРом. |

## <a name="related-topics"></a>Связанные темы

* [Справочник по динамическим ключевым словам брандмауэра](firewall-dynamic-keywords-reference.md)
