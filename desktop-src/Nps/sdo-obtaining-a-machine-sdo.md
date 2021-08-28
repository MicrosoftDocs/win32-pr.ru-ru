---
title: Получение машинного SDO
description: Первым шагом при использовании API SDO является создание объекта компьютера SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9217333440235d5adac544e00420f8564513510908a89a1da7494cf7ba2772ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128604"
---
# <a name="obtaining-a-machine-sdo"></a>Получение машинного SDO

Первым шагом при использовании API SDO является создание объекта компьютера SDO.

Используйте функцию [**клсидфромпрогид**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) , чтобы получить идентификатор класса (CLSID) для объекта компьютера SDO. Программный идентификатор (ProgID), используемый для объекта, — это IAS. Сдомачине ".

После получения идентификатора CLSID вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с этим идентификатором CLSID. Укажите [**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) в качестве интерфейса, для которого возвращается указатель.

Пример кода, демонстрирующий получение машинного SDO, см. [в разделе Присоединение к SDO-Enabled компьютеру](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .

 

 