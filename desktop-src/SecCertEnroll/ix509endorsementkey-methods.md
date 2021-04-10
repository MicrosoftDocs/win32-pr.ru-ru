---
description: Интерфейс IX509EndorsementKey предоставляет следующие методы.
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: Методы IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c1eb6a96cd555d4b0a0fdcd2ad52ccf80ec4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272596"
---
# <a name="ix509endorsementkey-methods"></a>Методы IX509EndorsementKey

Интерфейс [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) предоставляет следующие методы.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                        | Описание                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Метод Аддцертификате**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | Добавьте сертификат ключа подтверждения в поставщик хранилища ключей (KSP), который поддерживает ключи подтверждения.<br/>                                                                                                                                                                                     |
| [**Метод Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | Закрывает ключ подтверждения. Метод [**Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) можно вызвать только после успешного вызова метода [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/>                                                                                              |
| [**Метод Експортпубликкэй**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | Экспортирует открытый ключ подтверждения.<br/>                                                                                                                                                                                                                                                      |
| [**Метод Жетцертификатебиндекс**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | Возвращает сертификат подтверждения, связанный с ключом подтверждения от поставщика хранилища ключей для указанного индекса.<br/>                                                                                                                                                              |
| [**Метод Жетцертификатекаунт**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | Возвращает число сертификатов подтверждения в поставщике хранилища ключей.<br/>                                                                                                                                                                                                              |
| [**Метод Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | Открывает ключ подтверждения. Ключ подтверждения должен быть открыт, прежде чем можно будет получить сведения из ключа подтверждения, добавить или удалить сертификаты или экспортировать ключ подтверждения.<br/>                                                                                                  |
| [**Метод RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | Удаляет сертификат подтверждения, связанный с ключом подтверждения, от поставщика хранилища ключей. Метод [**RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) можно вызвать только после успешного вызова метода [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/> |



 

 

 




