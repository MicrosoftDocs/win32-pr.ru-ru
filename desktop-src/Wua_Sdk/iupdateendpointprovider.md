---
description: Содержит метод, используемый для получения конечной точки, используемой для подключения к службе.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Интерфейс Иупдатиндпоинтпровидер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 2242e30ccd64c0252d5a1ea97eedd865f9e80bee2c58f749ca6d2eabd64c6167
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896844"
---
# <a name="iupdateendpointprovider-interface"></a>Интерфейс Иупдатиндпоинтпровидер

Содержит метод, используемый для получения конечной точки, используемой для подключения к службе. Этот интерфейс реализуется при записи поставщика конечной точки.

## <a name="members"></a>Элементы

Интерфейс **иупдатиндпоинтпровидер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иупдатиндпоинтпровидер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иупдатиндпоинтпровидер** содержит следующие методы.



| Метод                                                                       | Описание                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**жетсервицеендпоинт**](iupdateendpointauthprovider-getserviceendpoint.md) | Запрашивает конечную точку, используемую для подключения к службе.<br/> |



 

## <a name="remarks"></a>Remarks

WUA вызывает метод [**жетсервицеендпоинт**](iupdateendpointauthprovider-getserviceendpoint.md) для запуска процесса согласования. При вызове WUA передает зарегистрированные типы токенов, а реализация этого интерфейса возвращает типы токенов, которые он предпочитает использовать.

 

 
