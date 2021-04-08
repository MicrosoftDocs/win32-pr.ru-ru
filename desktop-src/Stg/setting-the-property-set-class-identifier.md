---
title: Установка идентификатора класса набора свойств
description: Метод Ипропертистораже Сеткласс задает идентификатор CLSID объекта хранилища и значение тега класса, хранящееся в наборе свойств COM. Это происходит при вызове непростого хранилища свойств, хранящегося в структурированном объекте хранилища.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Установка идентификатора класса набора свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068415"
---
# <a name="setting-the-property-set-class-identifier"></a>Установка идентификатора класса набора свойств

Метод [**ипропертистораже:: сеткласс**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) задает идентификатор CLSID объекта хранилища и значение тега класса, хранящееся в наборе свойств COM. Это происходит при вызове непростого хранилища свойств, хранящегося в структурированном объекте хранилища.

Это обеспечивает согласованность и единообразие, что создает более эффективное взаимодействие с некоторыми инструментами. Объект хранилища свойств непрост, если он создается путем вызова [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) с установленным флагом **пропсетфлаг \_ unsimple** .

Идентификатор CLSID объекта хранилища задается вызовом метода [**IStorage:: сеткласс**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).

 

 




