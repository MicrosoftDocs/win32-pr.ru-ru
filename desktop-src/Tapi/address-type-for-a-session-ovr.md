---
description: Тип адреса определяет формат, необходимый для адреса. Например, если тип — ЛИНЕАДДРЕССТИПЕ \_ PHONENUMBER, адрес, используемый для набора номера в сеансе, должен быть номером телефона.
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: Тип адреса для сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673860"
---
# <a name="address-type-for-a-session"></a>Тип адреса для сеанса

[**Тип адреса**](lineaddresstype--constants.md) определяет формат, необходимый для адреса. Например, если тип — ЛИНЕАДДРЕССТИПЕ \_ PHONENUMBER, адрес, используемый для набора номера в сеансе, должен быть номером телефона.

Данное устройство и поставщик услуг поддерживают один или несколько типов адресов. Сведения о том, как опросить устройство для поддерживаемых форматов адресов, см. в разделе [типы адресов для устройства](address-type-ovr.md) .

**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **Дваддресстипе** Member of [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), который вызывается с помощью элемента **CIL \_ Каллеридаддресстипе**, **CIL \_ калледидаддресстипе** или **CIL \_ коннектедидаддресстипе** [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
