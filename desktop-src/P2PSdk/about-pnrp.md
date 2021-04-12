---
description: Поставщик пространства имен PNRP (NSP) — это бессерверная технология разрешения имен, позволяющая узлам обнаруживать друг друга.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Об PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156547"
---
# <a name="about-pnrp"></a>Об PNRP

Поставщик пространства имен PNRP (NSP) — это бессерверная технология разрешения имен, позволяющая узлам обнаруживать друг друга. PNRP использует API поставщика пространства имен Winsock 2.

Поддержка IPv6 необходима для PNRP и является единственным Интернет-протоколом, встроенным в API. Однако протокол PNRP может разрешать IPv4-адреса через технологии туннелирования 6to4 или [Teredo](/windows/desktop/Teredo/portal) . Пользователи Windows XP с пакетом обновления 1 (SP1) должны загрузить [Расширенный сетевой пакет](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) , чтобы включить поддержку IPv6, НЕОБХОДИМУЮ для PNRP.

> [!Note]  
> Приложениям, использующим PNRP в среде с брандмауэром, требуются группы исключений, охватывающие порт, характерный для приложения, а также порт "3540-UDP" для PNRP. Эти группы исключений должны быть включены при каждом запуске приложения.

 

Хотя протокол PNRP 2,0 является собственным для платформ Windows Vista и Windows Server 2008, пользователям Windows XP необходимо загрузить Центр обновления Windows [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) для обновления до PNRP 2,0.

 

 
