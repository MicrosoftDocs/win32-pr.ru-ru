---
description: Служба, драйвер или приложение, которые хотят предоставить данные счетчиков, могут создавать библиотеку DLL производительности для предоставления данных.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Предоставление данных счетчиков с помощью библиотеки DLL производительности
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663165"
---
# <a name="providing-counter-data-using-a-performance-dll"></a><span data-ttu-id="44a9a-103">Предоставление данных счетчиков с помощью библиотеки DLL производительности</span><span class="sxs-lookup"><span data-stu-id="44a9a-103">Providing Counter Data Using a Performance DLL</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44a9a-104">Из-за существенных ограничений производительности и надежности метод предоставления данных счетчиков производительности, описанных в этом разделе, может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="44a9a-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="44a9a-105">Вместо этого корпорация Майкрософт рекомендует использовать метод, описанный в разделе [предоставление данных счетчиков с помощью версии 2,0](providing-counter-data-using-version-2-0.md) для создания счетчиков производительности, а также миграция существующих счетчиков производительности для использования этого метода.</span><span class="sxs-lookup"><span data-stu-id="44a9a-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters, and that you migrate existing performance counters to use that method as well.</span></span>

<span data-ttu-id="44a9a-106">Служба, драйвер или приложение, которые хотят предоставить данные счетчиков, могут создавать библиотеку DLL производительности для предоставления данных.</span><span class="sxs-lookup"><span data-stu-id="44a9a-106">A service, driver, or application that wants to provide counter data can write a performance DLL to provide the data.</span></span> <span data-ttu-id="44a9a-107">Когда потребитель запрашивает данные о производительности, система загружает библиотеку DLL поставщика в процесс потребителя и вызывает поставщик для получения данных.</span><span class="sxs-lookup"><span data-stu-id="44a9a-107">When a consumer queries performance data, the system loads the provider DLL into the consumer's process and calls the provider to collect the data.</span></span> <span data-ttu-id="44a9a-108">Дополнительные сведения о создании библиотеки DLL производительности см. в разделе [Создание библиотеки DLL расширения производительности](creating-a-performance-extension-dll.md).</span><span class="sxs-lookup"><span data-stu-id="44a9a-108">For details on writing the performance DLL, see [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md).</span></span>

<span data-ttu-id="44a9a-109">Система использует реестр для определения поставщика, который необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="44a9a-109">The system uses the registry to determine which provider to call.</span></span> <span data-ttu-id="44a9a-110">Сведения о регистрации поставщика и счетчиках, которые он поддерживает, см. в разделе [Добавление счетчиков производительности](adding-performance-counters.md).</span><span class="sxs-lookup"><span data-stu-id="44a9a-110">For information on registering your provider and the counters that it supports, see [Adding Performance Counters](adding-performance-counters.md).</span></span>

> [!Note]
> <span data-ttu-id="44a9a-111">Библиотеки производительности не поддерживаются в Windows OneCore.</span><span class="sxs-lookup"><span data-stu-id="44a9a-111">Performance DLLs are not supported on Windows OneCore.</span></span> <span data-ttu-id="44a9a-112">При написании компонента, который должен выполняться в Windows OneCore, используйте метод, описанный в разделе [предоставление данных счетчиков с помощью версии 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="44a9a-112">If writing a component that must run on Windows OneCore, use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>
