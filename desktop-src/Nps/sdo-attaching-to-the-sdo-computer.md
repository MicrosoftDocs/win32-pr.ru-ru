---
title: Подключение к компьютеру SDO
description: При помощи указателя интерфейса, возвращенного CoCreateInstance, вызовите метод Исдомачине Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5863302da3f213c1360c254782a31c0dfc4fcb9a946f5827155862bca01405cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362192"
---
# <a name="attaching-to-the-sdo-computer"></a>Подключение к компьютеру SDO

При помощи указателя интерфейса, возвращенного [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), вызовите метод [**Исдомачине:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) . Передайте **значение NULL** в качестве параметра в метод **attach** . Значение **null** указывает, что **Присоединение** связывает объект компьютера с локальным компьютером. Присоединение к удаленному компьютеру не поддерживается.

Чтобы определить, присоединен ли локальный компьютер, вызовите метод [**исдомачине:: жетаттачедкомпутер**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .

Пример кода, демонстрирующий, как присоединиться к локальному компьютеру, см. [в разделе Присоединение к SDO-Enabled компьютеру](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .

 

 