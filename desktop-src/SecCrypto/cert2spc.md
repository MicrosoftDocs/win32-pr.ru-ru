---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66405ffb881e9ab384037bf9e388d3e055c4186a322efe0ab4171da4ece605e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127234"
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



 

 

 
