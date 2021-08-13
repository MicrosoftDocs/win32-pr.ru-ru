---
description: Атрибуты (API регистрации сертификатов) — атрибуты можно добавить в запрос на сертификат, чтобы предоставить центр сертификации (ЦС) с дополнительными сведениями, которые могут использоваться при создании и выдаче сертификата.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Атрибуты (API регистрации сертификатов)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aec93ec47a700902cb1275e25af6649e6988b76f7204b01487249e0130dd35b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903106"
---
# <a name="attributes-certificate-enrollment-api"></a>Атрибуты (API регистрации сертификатов)

В запрос на сертификат можно добавить атрибуты, чтобы предоставить центр сертификации (ЦС) с дополнительными сведениями, которые он может использовать при создании и выдаче сертификата. каждый атрибут представляет собой закодированную в [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) [*нотацию абстрактного синтаксиса*](/windows/desktop/SecGloss/a-gly) (ASN. 1), которая содержит идентификатор объекта (OID) и ноль или более значений. Атрибуты определяются с помощью интерфейсов, входящих в API регистрации сертификатов. Атрибуты более подробно обсуждаются в следующих разделах:

-   [Поддерживаемые атрибуты](supported-attributes.md)
-   [Архитектура атрибута](attribute-architecture.md)
-   [\#АТРИБУТЫ PKCS 7](pkcs--7-attributes.md)
-   [\#АТРИБУТЫ PKCS 10](pkcs--10-attributes.md)
-   [Атрибуты CMC](cmc-attributes.md)

 

 
