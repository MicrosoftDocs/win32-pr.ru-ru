---
description: Тип адреса устройства описывает формы адресации, допустимые для адреса, например номер телефона или IP-адрес.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Тип адреса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674031"
---
# <a name="address-type"></a>Тип адреса

Тип адреса устройства описывает формы адресации, допустимые для адреса, например номер телефона или IP-адрес. Данное устройство будет распознавать один или несколько типов адресов. Список типов адресов, поддерживаемых TAPI, см. в разделе [ \_ константы линеаддресстипе](lineaddresstype--constants.md). [Преобразование адреса](initiate-a-session-ovr.md) можно использовать для преобразования адреса из одного типа в другой.

Общие сведения [об адресах см. в](address-ovr.md) разделе [категории устройств](device-categories.md).

[Тип адреса для сеанса](address-type-for-a-session-ovr.md) будет подмножеством типов адресов устройств.

**Интерфейс TAPI 2. x:** См. раздел [**линежетдевкапс**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) и элемент **дваддресстипе** в [**линедевкапс**](/windows/win32/api/tapi/ns-tapi-linedevcaps).

**Интерфейс TAPI 3. x:** См. раздел [**итаддресскапабилитиес:: Get \_ аддресскапабилити**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability)с параметром *аддресскап* , равным входящему в [**адрес \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) **AC \_ аддресстипес** .

 

 
