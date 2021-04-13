---
title: Получение службы и пользователя Сдос
description: Чтобы получить Сдос для NPS (IAS) или определенного пользователя, вызовите методы Исдомачине Жетсервицесдо или Исдомачине Жетусерсдо.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338244"
---
# <a name="obtaining-service-and-user-sdos"></a>Получение службы и пользователя Сдос

> [!Note]  
> Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.

 

Чтобы получить Сдос для NPS (IAS) или определенного пользователя, вызовите методы [**исдомачине:: жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) или [**Исдомачине:: жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) . Эти методы возвращают указатели на интерфейсы [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для этих объектов. Для пользователя SDO используйте метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить интерфейс [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) для объекта. Для SDO службы используйте **IUnknown:: QueryInterface** для получения интерфейса [**Исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) или интерфейса [**исдосервицеконтрол**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .

Перед вызовом метода [**исдомачине:: жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) или [**Исдомачине:: Жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)вызовите [**исдомачине:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) , чтобы связать объект компьютера с локальным компьютером.

Пример кода, демонстрирующий, как получить эти Сдос, см. в разделе [Получение SDO службы](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) и [Получение пользовательского SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) .

 

 