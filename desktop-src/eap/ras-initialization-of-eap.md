---
title: Инициализация точки доступа EAP
description: После инициализации точка доступа (AP) запрашивает в реестре установленные протоколы проверки подлинности.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185557c4b908780c09714aa9cc7fa4c80399812f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412970"
---
# <a name="access-point-initialization-of-eap"></a>Инициализация точки доступа EAP

После инициализации точка доступа (AP) запрашивает в реестре установленные протоколы проверки подлинности. Затем AP вызывает экспортированную функцию [**расеапжетинфо**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) для каждого протокола проверки подлинности. Функция **расеапжетинфо** получает один параметр типа [**PPP \_ EAP \_ info**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info). AP использует член **двеаптипеид** этой структуры для указания протокола проверки подлинности. Обратите внимание, что одна библиотека DLL может поддерживать более одного протокола. Если **расеапжетинфо** возвращает любое значение, отличное **от \_ ошибки**, точка AP предполагает, что протокол проверки подлинности недоступен.

При возврате [](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) из расеапжетинфо [**\_ \_ информационная структура PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) содержит указатели на функции [**расеапинитиализе**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)), [**РАСЕАПБЕГИН**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), [**расеапмакемессаже**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))и [**расеапенд**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) в DLL-библиотеке EAP. Служба AP использует эти функции для взаимодействия с протоколом проверки подлинности. ТД немедленно вызывает **расеапинитиализе** для каждого протокола проверки подлинности, чтобы инициализировать его. Когда служба завершает работу, она снова вызывает **расеапинитиализе** , на этот раз с параметром *финитиализе* , установленным в **значение false** , чтобы указать, что протокол проверки подлинности должен завершить работу.

 

 