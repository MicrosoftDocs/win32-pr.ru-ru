---
description: До 2006 августа WS-MetadataExchange определен собственный метод получения метаданных Get, который использовался профилем устройств для веб-служб (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Соответствие спецификации WS-MetadataExchange и WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bec29d96b4ba3671f176349a56b891cd4d642762670fd16cf582da53208c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793974"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>Соответствие спецификации WS-MetadataExchange и WS-Transfer

До 2006 августа [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) определил собственный метод [получения метаданных Get](get--metadata-exchange--http-request-and-message.md) , который использовался [профилем устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). Спецификация WS-MetadataExchange версии 1,1 заменила этот метод методом GET, определенным в спецификации WS-Transfer.

В текущей модели WS-Transfer предоставляет метод [Get](get--metadata-exchange--http-request-and-message.md) и не делает ссылку на тип тела. WS-MetadataExchange описывает формат текста и механизм упаковки нескольких фрагментов метаданных в одном ответе, а DPWS описывает конкретные фрагменты метаданных, которые служба должна включать в ответ на метаданные.

WSDAPI не полностью поддерживает спецификацию WS-Transfer. Поскольку для устройств требуется только метод [Get](get--metadata-exchange--http-request-and-message.md) , никакие другие части WS-Transfer не реализованы. Кроме того, WSDAPI не реализует дополнительный метод, описанный в WS-MetadataExchange.

 

 



