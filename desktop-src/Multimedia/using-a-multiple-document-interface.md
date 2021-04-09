---
title: Использование многодокументного интерфейса
description: Использование многодокументного интерфейса
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Функция МЦивндрегистеркласс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890580"
---
# <a name="using-a-multiple-document-interface"></a>Использование многодокументного интерфейса

В приложениях, использующих многодокументный интерфейс (MDI), может потребоваться задать стили окна, недоступные через функцию [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) . Для этих приложений можно зарегистрировать и создать окно МЦивнд с помощью функции [**мЦивндрегистеркласс**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) с функцией [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Функция **мЦивндрегистеркласс** регистрирует \_ класс окна мЦивнд окна \_ классов, а затем **CreateWindowEx** создает экземпляр окна мЦивнд.

 

 