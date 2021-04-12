---
description: Данные вызова — это буфер размера вариабли, который можно использовать для накопления сведений о сеансе связи. Эти сведения становятся доступными для всех приложений, которые владеют и отслеживают сеанс.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Вызов данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344762"
---
# <a name="call-data"></a>Вызов данных

Данные вызова — это буфер размера вариабли, который можно использовать для накопления сведений о сеансе связи. Эти сведения становятся доступными для всех приложений, которые владеют и отслеживают сеанс.

Например, начальный обработчик входящего сеанса может запросить и ввести сведения об учетной записи клиента в буфер данных вызова, а затем последующим обработчикам не пришлось повторять запрос.

Не все поставщики служб поддерживают использование этих сведений.

**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**линесеткаллдата**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**двкаллдатасизе** and **Двкаллдатаоффсет** Members of [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**Line \_ каллинфо**](./line-callinfo.md) Message (*dwParam1* Set to LINECALLINFOSTATE \_ CALLDATA).

**Интерфейс TAPI 3. x:** См [**. раздел иткаллинфо::p UT \_ каллинфобуффер**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**ЦИБ \_ каллдатабуффер** Member в [**каллинфо \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**Иткаллинфочанжеевент:: Get \_ Причина**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) Возвращает элемент **ЦИК \_ каллдата** из [**каллинфочанже \_ Причина**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).

 

 
