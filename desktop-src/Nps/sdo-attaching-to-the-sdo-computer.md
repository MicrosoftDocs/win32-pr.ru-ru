---
title: Подключение к компьютеру SDO
description: При помощи указателя интерфейса, возвращенного CoCreateInstance, вызовите метод Исдомачине Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987585"
---
# <a name="attaching-to-the-sdo-computer"></a>Подключение к компьютеру SDO

При помощи указателя интерфейса, возвращенного [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), вызовите метод [**Исдомачине:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) . Передайте **значение NULL** в качестве параметра в метод **attach** . Значение **null** указывает, что **Присоединение** связывает объект компьютера с локальным компьютером. Присоединение к удаленному компьютеру не поддерживается.

Чтобы определить, присоединен ли локальный компьютер, вызовите метод [**исдомачине:: жетаттачедкомпутер**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .

Пример кода, демонстрирующий, как присоединиться к локальному компьютеру, см. [в разделе Присоединение к SDO-Enabled компьютеру](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .

 

 