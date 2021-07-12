---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581982"
---
# <a name="cert2spc"></a>Cert2SPC

средство Cert2SPC создает тестовое [*программное обеспечение Publisher сертификате*](../secgloss/s-gly.md) (SPC) с использованием существующих [*сертификатов*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) . Cert2SPC может заключить несколько сертификатов X. 509 в объект данных, подписанных [*PKCS \# 7*](../secgloss/p-gly.md) . это средство устанавливается в \\ папку Bin установочного пакета Microsoft Windows Software Development Kit (SDK).

Cert2SPC доступен в составе Windows SDK, который можно скачать из <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Это средство предназначено только для тестирования. Допустимый SPC получен из [*центра сертификации*](../secgloss/c-gly.md).


**Cert2SPC** *Cert1. cer Cert2. cer* ... *Output. SPC*

 



| Параметры              | Описание                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1. cer Cert2. cer* ... | Имена сертификатов X. 509 для включения в SPC. Каждое имя сертификата заканчивается расширением CER.                         |
| *Output. SPC*            | Имя \# объекта PKCS 7, содержащего создаваемые сертификаты X. 509. Имя выходного файла заканчивается расширением SPC. |



 

 

 
