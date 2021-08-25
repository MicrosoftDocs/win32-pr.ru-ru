---
title: Получение примера страницы задачи
description: Чтобы получить страницу задачи, необходимо вызвать ITask QueryInterface, чтобы получить интерфейс Ипровидетаскпаже, а затем вызвать Ипровидетаскпаже @ Page. Метод метода Page возвращает на страницу маркер, который затем может использоваться для вывода запрошенной страницы.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- получение планировщик задач страницы задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d619f76b4de416fe2bef9faa679851c613df05e427d6203a6a91936644ad07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872274"
---
# <a name="retrieving-a-task-page-example"></a>Получение примера страницы задачи

Чтобы получить страницу задачи, необходимо вызвать метод **ITask:: QueryInterface** , чтобы получить интерфейс [**ипровидетаскпаже**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) , а затем вызвать [**ипровидетаскпаже::-Page**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage). Метод метода **Page** возвращает на страницу маркер, который затем может использоваться для вывода запрошенной страницы.

> [!Note]  
> В следующем примере кода все интерфейсы освобождаются после того, как они больше не нужны.

 

В следующей процедуре описывается создание нового триггера.

**Создание нового триггера**

1.  Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач. (В этом примере предполагается, что служба планировщик задач запущена).
2.  Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task. (Обратите внимание, что в этом примере возвращается задача "задача тестирования".)
3.  Вызовите метод **ITask:: QueryInterface** , чтобы получить интерфейс [**ипровидетаскпаже**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) и [**ипровидетаскпаже::-Page**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) , чтобы получить страницу.
4.  С помощью возвращенного маркера страницы отобразите страницу.



| Пример кода                                   | См.                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Получение и отображение страницы задачи для известной задачи | [Получение страницы задачи](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Примеры планировщик задач 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 