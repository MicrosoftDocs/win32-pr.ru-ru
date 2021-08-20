---
title: Получение службы и пользователя Сдос
description: Чтобы получить Сдос для NPS (IAS) или определенного пользователя, вызовите методы Исдомачине Жетсервицесдо или Исдомачине Жетусерсдо.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebef1e695236bd1449ab886cb998a67f09c2cafc8ded446b0b7e1ad89b01181
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128594"
---
# <a name="obtaining-service-and-user-sdos"></a>Получение службы и пользователя Сдос

> [!Note]  
> служба проверки подлинности в интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.

 

Чтобы получить Сдос для NPS (IAS) или определенного пользователя, вызовите методы [**исдомачине:: жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) или [**Исдомачине:: жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) . Эти методы возвращают указатели на интерфейсы [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для этих объектов. Для пользователя SDO используйте метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить интерфейс [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) для объекта. Для SDO службы используйте **IUnknown:: QueryInterface** для получения интерфейса [**Исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) или интерфейса [**исдосервицеконтрол**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .

Перед вызовом метода [**исдомачине:: жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) или [**Исдомачине:: Жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)вызовите [**исдомачине:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) , чтобы связать объект компьютера с локальным компьютером.

Пример кода, демонстрирующий, как получить эти Сдос, см. в разделе [Получение SDO службы](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) и [Получение пользовательского SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) .

 

 