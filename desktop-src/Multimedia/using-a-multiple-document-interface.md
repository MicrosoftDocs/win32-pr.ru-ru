---
title: Использование многодокументного интерфейса
description: Использование многодокументного интерфейса
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Функция МЦивндрегистеркласс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b75d337c5375b66974161c1c983c1aeec5bed7805457186139771d879132b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941059"
---
# <a name="using-a-multiple-document-interface"></a>Использование многодокументного интерфейса

В приложениях, использующих многодокументный интерфейс (MDI), может потребоваться задать стили окна, недоступные через функцию [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) . Для этих приложений можно зарегистрировать и создать окно МЦивнд с помощью функции [**мЦивндрегистеркласс**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) с функцией [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Функция **мЦивндрегистеркласс** регистрирует \_ класс окна мЦивнд окна \_ классов, а затем **CreateWindowEx** создает экземпляр окна мЦивнд.

 

 