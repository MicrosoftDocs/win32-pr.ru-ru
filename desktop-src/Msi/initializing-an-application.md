---
description: Чтобы включить функции установщика, приложение должно вызвать ряд функций при инициализации.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Инициализация приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264176"
---
# <a name="initializing-an-application"></a><span data-ttu-id="0f30f-103">Инициализация приложения</span><span class="sxs-lookup"><span data-stu-id="0f30f-103">Initializing an Application</span></span>

<span data-ttu-id="0f30f-104">Чтобы включить функции установщика, приложение должно вызвать ряд функций при инициализации.</span><span class="sxs-lookup"><span data-stu-id="0f30f-104">To enable installer functionality, an application must call a number of functions when it is initializing.</span></span> <span data-ttu-id="0f30f-105">Дополнительные сведения см. в разделе [механизм установки](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="0f30f-105">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span> <span data-ttu-id="0f30f-106">Следующие шаги описывают использование установщика для инициализации приложения.</span><span class="sxs-lookup"><span data-stu-id="0f30f-106">The following steps describe how to use the installer to initialize an application:</span></span>

<span data-ttu-id="0f30f-107">**Инициализация приложения**</span><span class="sxs-lookup"><span data-stu-id="0f30f-107">**To initialize an application**</span></span>

1.  <span data-ttu-id="0f30f-108">Вызовите функцию [**мсижетпродукткоде**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) , чтобы приложение могла идентифицировать себя в установщике.</span><span class="sxs-lookup"><span data-stu-id="0f30f-108">Call the [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) function so the application can identify itself to the installer.</span></span>

    <span data-ttu-id="0f30f-109">Код продукта является обязательным параметром для многих функций установщика.</span><span class="sxs-lookup"><span data-stu-id="0f30f-109">The product code is a required parameter for many installer functions.</span></span>

2.  <span data-ttu-id="0f30f-110">Вызовите функцию [**мсижетусеринфо**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) , чтобы получить сведения о пользователе при первом запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="0f30f-110">Call the [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) function to collect user information the first time the application starts.</span></span>

    <span data-ttu-id="0f30f-111">Если вызов [**мсижетусеринфо**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) завершается неудачей, вызовите функцию [**мсиколлектусеринфо**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) , чтобы получить сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="0f30f-111">If the call to [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) fails, call the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function to collect user information.</span></span>

3.  <span data-ttu-id="0f30f-112">При необходимости Отобразите пользовательский интерфейс по умолчанию, вызвав функцию [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .</span><span class="sxs-lookup"><span data-stu-id="0f30f-112">Display a default user interface, if necessary, by calling the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function.</span></span>

    <span data-ttu-id="0f30f-113">Чтобы создать собственный пользовательский интерфейс, зарегистрируйте его с помощью установщика, вызвав функцию [**мсисетекстерналуи**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="0f30f-113">To author your own user interface, register it with the installer by calling the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span>

4.  <span data-ttu-id="0f30f-114">Вызовите функцию [**мсиенаблелог**](/windows/desktop/api/Msi/nf-msi-msienableloga) , чтобы задать уровень ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="0f30f-114">Call the [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) function to set the logging level.</span></span>
5.  <span data-ttu-id="0f30f-115">Предоставление пользователю доступных функций путем перечисления функций приложения.</span><span class="sxs-lookup"><span data-stu-id="0f30f-115">Present the user with available features by enumerating the features of your application.</span></span> <span data-ttu-id="0f30f-116">Перечисление компонентов можно выполнить следующими способами.</span><span class="sxs-lookup"><span data-stu-id="0f30f-116">You can enumerate features in the following ways:</span></span>
    -   <span data-ttu-id="0f30f-117">Запросите функции установщика.</span><span class="sxs-lookup"><span data-stu-id="0f30f-117">Query the installer feature-by-feature.</span></span> <span data-ttu-id="0f30f-118">Например, перед рисованием кнопки или пункта меню приложение вызывает функцию [**мсикуерифеатурестате**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) , чтобы установщик мог проверить доступность этой функции.</span><span class="sxs-lookup"><span data-stu-id="0f30f-118">For example, before the application draws a button or a menu item, the application calls the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function so the installer can check that the feature is available.</span></span>
    -   <span data-ttu-id="0f30f-119">Перечислить все доступные компоненты одновременно, вызвав функцию [**мсиенумфеатурес**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) .</span><span class="sxs-lookup"><span data-stu-id="0f30f-119">Enumerate all of the available features at once by calling the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) function.</span></span> <span data-ttu-id="0f30f-120">Чтобы использовать эту функцию, приложение должно многократно вызывать **мсиенумфеатурес** при увеличении индекса.</span><span class="sxs-lookup"><span data-stu-id="0f30f-120">To use this function, the application must call **MsiEnumFeatures** repeatedly while incrementing an index.</span></span>
6.  <span data-ttu-id="0f30f-121">Получите подробные сведения о текущей установке, вызвав следующие функции перечисления многократно, увеличивая переменную индекса для каждого вызова:</span><span class="sxs-lookup"><span data-stu-id="0f30f-121">Get detailed information about the current installation by calling the following enumeration functions repeatedly, incrementing an index variable for each call:</span></span>

    -   <span data-ttu-id="0f30f-122">Вызовите функцию [**мсиенумпродуктс**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) для перечисления продуктов, зарегистрированных в установщике.</span><span class="sxs-lookup"><span data-stu-id="0f30f-122">Call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) function to enumerate products registered with the installer.</span></span>
    -   <span data-ttu-id="0f30f-123">Вызовите функцию [**мсиенумкомпонентс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) для перечисления компонентов.</span><span class="sxs-lookup"><span data-stu-id="0f30f-123">Call the [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) function to enumerate components.</span></span>
    -   <span data-ttu-id="0f30f-124">Вызовите функцию [**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) , чтобы перечислить квалификаторы компонента.</span><span class="sxs-lookup"><span data-stu-id="0f30f-124">Call the [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) function to enumerate component qualifiers.</span></span>
    -   <span data-ttu-id="0f30f-125">Вызовите функцию [**мсиенумклиентс**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) , чтобы перечислить продукты для определенного компонента.</span><span class="sxs-lookup"><span data-stu-id="0f30f-125">Call the [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) function to enumerate the products for a particular component.</span></span>

    <span data-ttu-id="0f30f-126">Если возвращаемое значение функции перечисления является \_ успешным, то по-прежнему есть больше элементов для перечисления и функция должна вызываться повторно с увеличивающейся переменной индекса.</span><span class="sxs-lookup"><span data-stu-id="0f30f-126">If the return value on an enumeration function is ERROR\_SUCCESS, there are still more items to be enumerated and the function should be called again with an incremented index variable.</span></span> <span data-ttu-id="0f30f-127">Если возвращаемое значение не содержит \_ \_ больше \_ элементов, то все элементы были перечислены, и функция не должна вызываться повторно.</span><span class="sxs-lookup"><span data-stu-id="0f30f-127">If the return value is ERROR\_NO\_MORE\_ITEMS, then all of the items have been enumerated, and the function should not be called again.</span></span>

 

 



