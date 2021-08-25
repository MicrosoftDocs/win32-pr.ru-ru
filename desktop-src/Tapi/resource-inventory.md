---
description: Приложение должно выполнять инвентаризацию доступных для него ресурсов связи, а затем уведомлять TAPI о том, какие ресурсы будут использоваться и как они будут использоваться.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Инвентаризация ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436479877f63255ce6132a5907f97a511efea16dd5e21db41b0e41000beb8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773424"
---
# <a name="resource-inventory"></a>Инвентаризация ресурсов

Приложение должно выполнять инвентаризацию доступных для него ресурсов связи, а затем уведомлять TAPI о том, какие ресурсы будут использоваться и как они будут использоваться. Дополнительные сведения о типах ресурсов и возможностях, к которым может обращаться приложение, см. в разделе [Управление устройством](device-control.md) .

**Интерфейс TAPI 2. x:** Приложения получают количество доступных строк при возврате [**линеинитиализикс**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) . Затем они могут выполнять [**линежетдевкапс**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) в каждой строке, [**линежетаддресскапс**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) для каждого адреса и [**линеопен**](/windows/win32/api/tapi/nf-tapi-lineopen) для каждой строки, которая будет использоваться.

**Интерфейс TAPI 3. x:** Приложения используют [**адреса иттапи:: енумератеаддрессес**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) или [**иттапи:: \_ Get**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) для обнаружения доступных адресов. [**Итмедиасуппорт**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) и [**итаддресскапабилитиес**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) предоставляют сведения о типах связи для каждого адреса. При реализации поставщиком услуг [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) предоставляет приложению доступ к дополнительным сведениям и элементам управления.

 

 
