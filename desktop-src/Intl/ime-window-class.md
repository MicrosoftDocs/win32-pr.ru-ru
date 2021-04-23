---
description: Класс окна IME — это стандартный глобальный системный класс, определяющий внешний вид и поведение стандартных окон IME.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Класс окна IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910119"
---
# <a name="ime-window-class"></a><span data-ttu-id="429a7-103">Класс окна IME</span><span class="sxs-lookup"><span data-stu-id="429a7-103">IME Window Class</span></span>

<span data-ttu-id="429a7-104">Класс окна IME — это стандартный глобальный системный класс, определяющий внешний вид и поведение стандартных окон IME.</span><span class="sxs-lookup"><span data-stu-id="429a7-104">The IME window class is a predefined system global class that defines the appearance and behavior of the standard IME windows.</span></span> <span data-ttu-id="429a7-105">Класс аналогичен общим классам элементов управления, так как приложение создает окно этого класса с помощью функции [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="429a7-105">The class is similar to common control classes in that the application creates a window of this class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="429a7-106">Как и статические элементы управления, окно IME не реагирует на вводимые пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="429a7-106">Like static controls, an IME window does not respond to user input by itself.</span></span> <span data-ttu-id="429a7-107">Вместо этого он уведомляет редактор IME о действиях ввода данных пользователя и обрабатывает сообщения управления, отправляемые редактором IME или приложениями для выполнения ответа на действие пользователя.</span><span class="sxs-lookup"><span data-stu-id="429a7-107">Instead, it notifies the IME of user input actions and processes control messages sent to it by the IME or applications to carry out a response to the user action.</span></span>

<span data-ttu-id="429a7-108">Приложения, поддерживающие IME, иногда создают настраиваемые окна IME с помощью класса окна IME.</span><span class="sxs-lookup"><span data-stu-id="429a7-108">IME-aware applications sometimes create customized IME windows using the IME window class.</span></span> <span data-ttu-id="429a7-109">Использование настройки окна позволяет приложению использовать преимущества обработки окна IME по умолчанию при управлении положением окна.</span><span class="sxs-lookup"><span data-stu-id="429a7-109">Use of window customization allows the application to take advantage of the default processing of the IME window while having control of window positioning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="429a7-110">См. также</span><span class="sxs-lookup"><span data-stu-id="429a7-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="429a7-111">О диспетчере методов ввода</span><span class="sxs-lookup"><span data-stu-id="429a7-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
