---
description: Объект TAPI является основным объектом для TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Интерфейсы объектов TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1e49fe83a75c802b06ded953f309a157365d482d22d06c6bbedf97a5b8ac7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139857"
---
# <a name="tapi-object-interfaces"></a>Интерфейсы объектов TAPI

[Объект TAPI](tapi-object.md) является основным объектом для TAPI 3.

Интерфейс [**иттапиобжектевент**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) напрямую не предоставляется в объекте TAPI, но тесно связан с ним и указан в справочных целях для удобства.



| Интерфейсы                                                 | Описание                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иттапи**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Основной интерфейс TAPI 3.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Является производным от [**иттапи**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); предоставляет дополнительные методы, поддерживающие телефонные устройства.                                                         |
| [**иттапиевентнотификатион**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Исходящий интерфейс, используемый для получения асинхронных сведений о событиях TAPI 3.                                                                       |
| [**иттапикаллцентер**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Предоставляет интерфейс ввода в элементы управления центра обработки вызовов.                                                                                                 |
| [**иттапиобжектевент**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Предоставляет методы для получения сведений о событиях объекта TAPI.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Расширяет [**иттапиобжектевент**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); предоставляет метод для получения указателя на объект Phone, вызвавший событие объекта TAPI. |



 

 

 
