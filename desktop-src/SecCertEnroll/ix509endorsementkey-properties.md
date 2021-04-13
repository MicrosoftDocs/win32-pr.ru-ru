---
description: Интерфейс IX509EndorsementKey предоставляет следующие свойства.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Свойства IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647464"
---
# <a name="ix509endorsementkey-properties"></a>Свойства IX509EndorsementKey

Интерфейс [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) предоставляет следующие свойства.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                        | Описание                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Свойство Length**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | Битовая длина ключа подтверждения. Доступ к этому свойству можно получить только после вызова метода [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/>                                                                                                                                                                                            |
| [**Открытое свойство**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Указывает, был ли успешно вызван метод [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/>                                                                                                                                                                                                                                            |
| [**ProviderName, свойство**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | Имя поставщика шифрования. По умолчанию используется поставщик криптографии платформы Майкрософт. Свойство [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) необходимо задать до вызова метода [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) . Невозможно изменить свойство **providerName** после вызова метода **Open** .<br/> |



 

 

 




