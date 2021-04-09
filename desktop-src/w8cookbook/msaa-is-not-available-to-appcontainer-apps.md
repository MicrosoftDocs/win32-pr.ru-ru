---
title: MSAA недоступен для приложений Магазина Windows
description: MSAA недоступен для приложений Магазина Windows
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104070757"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a><span data-ttu-id="b1ad7-103">MSAA недоступен для приложений Магазина Windows</span><span class="sxs-lookup"><span data-stu-id="b1ad7-103">MSAA is not available to Windows Store apps</span></span>

## <a name="platform"></a><span data-ttu-id="b1ad7-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="b1ad7-104">Platform</span></span>

<span data-ttu-id="b1ad7-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="b1ad7-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="b1ad7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b1ad7-106">Description</span></span>

<span data-ttu-id="b1ad7-107">Windows 8 не поддерживает MSAA (Microsoft Active Accessibility) для чтения или автоматизации доступных данных из приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-107">Windows 8 does not support MSAA (Microsoft Active Accessibility) for reading or automating accessible data from Windows Store apps.</span></span> <span data-ttu-id="b1ad7-108">Вместо этого следует использовать API автоматизации пользовательского интерфейса (UIA), доступный с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-108">The UI Automation (UIA) API, available since Windows 7, should be used instead.</span></span> <span data-ttu-id="b1ad7-109">Поскольку нет существующих функций приложения для Магазина Windows, существующие реализации, затрагиваемые этим изменением, отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-109">Since there are no existing Windows Store app features, there are no existing implementations that are affected by this change.</span></span> <span data-ttu-id="b1ad7-110">Это касается только новых приложений и функций, написанных для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-110">This affects only new apps and features written for Windows 8.</span></span> <span data-ttu-id="b1ad7-111">Разработчики по-прежнему могут использовать MSAA для предоставления данных о специальных возможностях.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-111">Developers can still use MSAA to expose their accessibility data.</span></span> <span data-ttu-id="b1ad7-112">Если данные MSAA предоставляются поставщиком приложений Магазина Windows, клиенты UIA смогут считывать и автоматизировать данные.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-112">If MSAA data is provided by Windows Store app provider, UIA clients will still be able to read and automate the data.</span></span>

<span data-ttu-id="b1ad7-113">Чтобы упростить API для приложений Магазина Windows 8Windows, мы решили поддерживать только автоматизацию пользовательского интерфейса в качестве клиента для этих приложений.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-113">To simplify the API for Windows 8Windows Store apps, we decided to support only UI Automation as a client for these apps.</span></span> <span data-ttu-id="b1ad7-114">UIA клиенты могут считывать поставщиков UIA в собственном режиме без перевода.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-114">UIA clients can read UIA providers natively, with no translation.</span></span> <span data-ttu-id="b1ad7-115">UIA-клиенты могут считывать поставщиков MSAA в виде преобразования с помощью прокси-сервера UIA в MSAA.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-115">UIA clients can read MSAA providers as translated through the UIA-to-MSAA Proxy.</span></span> <span data-ttu-id="b1ad7-116">Это снизит нагрузку на тестирование для разработчиков приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-116">This will reduce the testing burden for Windows Store app developers.</span></span>

<span data-ttu-id="b1ad7-117">Устранение поддержки поставщиков MSAA еще больше сокращает матрицу тестирования, но существуют основные приложения, которые по-прежнему основаны на MSAA, и мы не хотим, чтобы они были недоступны.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-117">Eliminating support for MSAA providers would further reduce the testing matrix, but there are major apps that are still MSAA-based and we do not want to render them inaccessible.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b1ad7-118">Проявление</span><span class="sxs-lookup"><span data-stu-id="b1ad7-118">Manifestation</span></span>

<span data-ttu-id="b1ad7-119">Разработчики приложений для Магазина Windows не смогут получить доступ к сведениям о MSAA в модели приложения.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-119">Windows Store app developers will not be able to access the details of MSAA within the app model.</span></span>

## <a name="solution"></a><span data-ttu-id="b1ad7-120">Решение</span><span class="sxs-lookup"><span data-stu-id="b1ad7-120">Solution</span></span>

<span data-ttu-id="b1ad7-121">В MSAA для функций приложений Магазина Windows не следует создавать новые автоматические случаи.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-121">No new automated cases should be authored in MSAA for features of Windows Store apps.</span></span>

<span data-ttu-id="b1ad7-122">Переключайте все существующие встроенные инструменты, использующие MSAA, в UIA, если им нужно взаимодействовать с приложениями Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-122">Switch any existing in-box tools that use MSAA to UIA if they need to interact with Windows Store apps.</span></span> <span data-ttu-id="b1ad7-123">Разработчики приложений для Магазина Windows должны использовать API автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b1ad7-123">Windows Store app developers should use the UI Automation API.</span></span>

## <a name="resources"></a><span data-ttu-id="b1ad7-124">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="b1ad7-124">Resources</span></span>

-   [<span data-ttu-id="b1ad7-125">Основы модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="b1ad7-125">UI Automation Fundamentals</span></span>](../winauto/entry-uiauto-win32.md)

 

 