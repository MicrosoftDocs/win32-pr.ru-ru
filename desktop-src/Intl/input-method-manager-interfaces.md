---
description: В этом разделе описываются интерфейсы IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Интерфейсы диспетчера методов ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683520"
---
# <a name="input-method-manager-interfaces"></a>Интерфейсы диспетчера методов ввода

В этом разделе описываются интерфейсы IMM.



| Интерфейс                                                            | Описание                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ифекоммон**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Предоставляет службы, связанные с IME, которые являются общими для разных языков.                                                                         |
| [**ифедиктионари**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Разрешает клиентам доступ к пользовательскому словарю Microsoft IME.                                                                                      |
| [**ифелангуаже**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Предоставляет службы языковой обработки с помощью редактора IME (Майкрософт).                                                                                 |
| [**иимепад**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Вставляет текст в приложения из Имепадапплетс, которые реализуют интерфейс [**иимепадапплет**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .                                 |
| [**иимепадапплет**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Вводит строки в приложения через интерфейс [**иимепад**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .                                                                     |
| [**иимеплугиндиктдиктионарилист**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Предоставляет доступ к списку словарей подключаемых модулей IME.                                                                                       |
| [**иимеспеЦифяпплетс**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Указывает методы, вызываемые из объекта интерфейса [**иимепад**](/windows/desktop/api/Imepad/nn-imepad-iimepad) для эмуляции интерфейса [**иимепадапплет**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) . |



 

 

 



