---
title: Узел протокола расширяемой проверки подлинности
description: Сведения о узле протокола расширенной проверки подлинности (EAP). См. требования к времени выполнения и Просмотр дополнительных доступных ресурсов.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104134827"
---
# <a name="extensible-authentication-protocol-host"></a>Узел протокола расширяемой проверки подлинности

## <a name="purpose"></a>Назначение


EAPHost — это сетевой компонент Microsoft Windows, предоставляющий инфраструктуру расширенной проверки подлинности (EAP) для проверки подлинности реализаций протоколов, таких как [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) и [точка-точка](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP). Она также позволяет выполнять проверку подлинности с помощью таких технологий, как сервер политики сети (NPS) (Майкрософт). В отличие от предыдущего сервера IAS ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS поддерживает [защиту доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP).


API-интерфейсы EAPHost позволяют приложениям проходить проверку подлинности с помощью службы EAPHost и предоставлять шаблон для разработки согласованных методов проверки подлинности для использования с EAPHost.

## <a name="run-time-requirements"></a>Требования к среде выполнения

API-интерфейсы EAPHost поддерживаются только в Windows Vista и более поздних операционных системах.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Об EAPHost](about-eap-host.md)
</dt> <dt>

[Использование EAPHost](using-eap-host.md)
</dt> <dt>

[Справочник по API EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 