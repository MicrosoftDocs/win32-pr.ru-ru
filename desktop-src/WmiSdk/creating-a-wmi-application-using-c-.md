---
description: Чтобы создать приложение для WMI с помощью C++, необходимо инициализировать COM, доступ и задать протоколы WMI, а также выполнить ручную очистку.
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Создание приложения WMI с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348405"
---
# <a name="creating-a-wmi-application-using-c"></a><span data-ttu-id="bc11a-103">Создание приложения WMI с помощью C++</span><span class="sxs-lookup"><span data-stu-id="bc11a-103">Creating a WMI Application Using C++</span></span>

<span data-ttu-id="bc11a-104">Чтобы создать приложение для WMI с помощью C++, необходимо инициализировать COM, доступ и задать протоколы WMI, а также выполнить ручную очистку.</span><span class="sxs-lookup"><span data-stu-id="bc11a-104">To create an application for WMI using C++: you must initialize COM, access and set WMI protocols, and perform a manual cleanup.</span></span> <span data-ttu-id="bc11a-105">Однако C++ обладает преимуществом гибкости и энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="bc11a-105">However, C++ does have the advantage of flexibility and power.</span></span> <span data-ttu-id="bc11a-106">Таким образом, если вы лучше используете Visual Basic Scripting Edition (VBScript) или Windows PowerShell для простых процессов, C++ работает лучше для более сложных приложений и требуется для написания [поставщиков](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="bc11a-106">Therefore, while you are better served in using Visual Basic Scripting Edition (VBScript) or Windows PowerShell for simple processes, C++ works better for more sophisticated applications and is required for writing [providers](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="bc11a-107">В следующей процедуре описывается создание приложения WMI.</span><span class="sxs-lookup"><span data-stu-id="bc11a-107">The following procedure describes how to create a WMI application.</span></span>

<span data-ttu-id="bc11a-108">**Создание приложения WMI**</span><span class="sxs-lookup"><span data-stu-id="bc11a-108">**To create a WMI application**</span></span>

1.  <span data-ttu-id="bc11a-109">[Инициализация COM](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="bc11a-109">[Initialize COM](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="bc11a-110">Поскольку Инструментарий WMI основан на технологии COM, необходимо выполнять вызовы функций [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) для доступа к WMI.</span><span class="sxs-lookup"><span data-stu-id="bc11a-110">Because WMI is based on COM technology, you must perform calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span>

2.  <span data-ttu-id="bc11a-111">[Создайте соединение с пространством имен WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="bc11a-111">[Create a connection to a WMI namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="bc11a-112">По определению Инструментарий WMI работает в процессе, отличном от процесса приложения.</span><span class="sxs-lookup"><span data-stu-id="bc11a-112">By definition, WMI runs in a different process than your application.</span></span> <span data-ttu-id="bc11a-113">Поэтому необходимо создать подключение между приложением и WMI.</span><span class="sxs-lookup"><span data-stu-id="bc11a-113">Therefore, you must create a connection between your application and WMI.</span></span>

3.  <span data-ttu-id="bc11a-114">[Задайте уровни безопасности для WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bc11a-114">[Set the security levels on the WMI connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

    <span data-ttu-id="bc11a-115">Чтобы использовать подключение, созданное в WMI, необходимо задать уровни олицетворения и проверки подлинности для приложения.</span><span class="sxs-lookup"><span data-stu-id="bc11a-115">To use the connection you create to WMI, you must set the impersonation and authentication levels for your application.</span></span>

4.  <span data-ttu-id="bc11a-116">Реализуйте назначение приложения.</span><span class="sxs-lookup"><span data-stu-id="bc11a-116">Implement the purpose of your application.</span></span>

    <span data-ttu-id="bc11a-117">Инструментарий WMI предоставляет разнообразные интерфейсы COM, используемые для доступа к данным и управления ими на предприятии.</span><span class="sxs-lookup"><span data-stu-id="bc11a-117">WMI exposes a variety of COM interfaces use to access and manipulate data across your enterprise.</span></span> <span data-ttu-id="bc11a-118">Дополнительные сведения см. в статьях [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md), [Получение WMI-события](receiving-a-wmi-event.md)и [COM API для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="bc11a-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Receiving a WMI Event](receiving-a-wmi-event.md), and [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="bc11a-119">Именно здесь должно существовать основная часть клиентского приложения инструментария WMI, например доступ к объектам WMI или обработка данных.</span><span class="sxs-lookup"><span data-stu-id="bc11a-119">This is where the bulk of your WMI client application should exist, such as accessing WMI objects or manipulating data.</span></span>

5.  <span data-ttu-id="bc11a-120">[Очистка и завершение работы приложения](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="bc11a-120">[Cleanup and shut down your application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

    <span data-ttu-id="bc11a-121">После выполнения запросов к инструментарию WMI следует уничтожить все COM-указатели и правильно завершить работу приложения.</span><span class="sxs-lookup"><span data-stu-id="bc11a-121">After you complete your queries to WMI, you should destroy all COM pointers and shut down your application correctly.</span></span>

<span data-ttu-id="bc11a-122">Дополнительные сведения и пример кода о создании приложения WMI см. в разделе [пример. Создание приложения WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="bc11a-122">For more information and a code example about how to create a WMI application, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

 

 
