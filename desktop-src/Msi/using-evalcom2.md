---
description: Evalcom2.dll можно использовать для реализации операций проверки для пакетов установки и модулей слияния с помощью внутренних оценщиков согласованности — ICEs.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Использование Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809922"
---
# <a name="using-evalcom2"></a><span data-ttu-id="91bb0-103">Использование Evalcom2</span><span class="sxs-lookup"><span data-stu-id="91bb0-103">Using Evalcom2</span></span>

<span data-ttu-id="91bb0-104">Evalcom2.dll можно использовать для реализации операций проверки для пакетов установки и модулей слияния с помощью [внутренних оценщиков согласованности — ICEs](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="91bb0-104">Evalcom2.dll can be used to implement validation operations for installation packages and merge modules using [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="91bb0-105">Основной объект реализует интерфейсы для программ C/C++.</span><span class="sxs-lookup"><span data-stu-id="91bb0-105">The main object implements interfaces for C/C++ programs.</span></span>

<span data-ttu-id="91bb0-106">Основной объект также реализует [интерфейсы Evalcom2](evalcom2-interfaces.md) для программ C/C++.</span><span class="sxs-lookup"><span data-stu-id="91bb0-106">The main object also implements [Evalcom2 interfaces](evalcom2-interfaces.md) for C/C++ programs.</span></span> <span data-ttu-id="91bb0-107">CLSID, необходимый для получения интерфейса из [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , — {6E5E1910-8053-4660-B795-6B612E29BC58}.</span><span class="sxs-lookup"><span data-stu-id="91bb0-107">The CLSID required to obtain the interface from [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is {6E5E1910-8053-4660-B795-6B612E29BC58}.</span></span> <span data-ttu-id="91bb0-108">РЕФИИД имеет значение {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span><span class="sxs-lookup"><span data-stu-id="91bb0-108">The REFIID is {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span></span>

<span data-ttu-id="91bb0-109">Для реализации операций проверки можно использовать следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="91bb0-109">You can use the following procedure to implement validation operations.</span></span>

<span data-ttu-id="91bb0-110">**Реализация операций проверки**</span><span class="sxs-lookup"><span data-stu-id="91bb0-110">**To implement validation operations**</span></span>

1.  <span data-ttu-id="91bb0-111">Инициализируйте COM в вызывающем потоке с помощью [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="91bb0-111">Initialize COM on the calling thread using [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span></span>
2.  <span data-ttu-id="91bb0-112">Получите указатель на интерфейс [**ивалидате**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) , используя [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="91bb0-112">Obtain the pointer to the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>
3.  <span data-ttu-id="91bb0-113">Откройте установочный пакет или модуль слияния с помощью метода [**опендатабасе**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) .</span><span class="sxs-lookup"><span data-stu-id="91bb0-113">Open the installation package or merge module using the [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) method.</span></span>
4.  <span data-ttu-id="91bb0-114">Откройте файл оценки с помощью метода [**опенкуб**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) .</span><span class="sxs-lookup"><span data-stu-id="91bb0-114">Open the evaluation file using the [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) method.</span></span>
5.  <span data-ttu-id="91bb0-115">Задайте функцию обратного вызова для вывода с помощью метода [**сетдисплай**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) .</span><span class="sxs-lookup"><span data-stu-id="91bb0-115">Set the display callback function using the [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) method.</span></span>
6.  <span data-ttu-id="91bb0-116">Задайте функцию обратного вызова состояния с помощью метода [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="91bb0-116">Set the status callback function using the [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) method.</span></span>
7.  <span data-ttu-id="91bb0-117">Выполните проверку с помощью метода [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) .</span><span class="sxs-lookup"><span data-stu-id="91bb0-117">Perform the validation using the [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) method.</span></span>
8.  <span data-ttu-id="91bb0-118">Закройте файл. cub с помощью метода [**клосекуб**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) .</span><span class="sxs-lookup"><span data-stu-id="91bb0-118">Close the .cub file using the [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) method.</span></span>
9.  <span data-ttu-id="91bb0-119">Закройте базу данных с помощью метода [**клоседатабасе**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) .</span><span class="sxs-lookup"><span data-stu-id="91bb0-119">Close the database using the [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) method.</span></span>
10. <span data-ttu-id="91bb0-120">Освободите интерфейс [**ивалидате**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) .</span><span class="sxs-lookup"><span data-stu-id="91bb0-120">Release the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface.</span></span>
11. <span data-ttu-id="91bb0-121">Отменить инициализацию COM с помощью [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="91bb0-121">Uninitialize COM using [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

## <a name="related-topics"></a><span data-ttu-id="91bb0-122">См. также</span><span class="sxs-lookup"><span data-stu-id="91bb0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91bb0-123">Интерфейсы Evalcom2</span><span class="sxs-lookup"><span data-stu-id="91bb0-123">Evalcom2 Interfaces</span></span>](evalcom2-interfaces.md)
</dt> <dt>

[<span data-ttu-id="91bb0-124">Автоматизация проверки</span><span class="sxs-lookup"><span data-stu-id="91bb0-124">Validation Automation</span></span>](validation-automation.md)
</dt> <dt>

[<span data-ttu-id="91bb0-125">Функции обратного вызова проверки</span><span class="sxs-lookup"><span data-stu-id="91bb0-125">Validation Callback Functions</span></span>](validation-callback-functions.md)
</dt> </dl>

 

 
