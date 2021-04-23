---
description: Компоненты CRM можно установить в серверное приложение COM+ или приложение библиотеки COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Настройка компонентов COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701284"
---
# <a name="configuring-com-crm-components"></a><span data-ttu-id="24a73-103">Настройка компонентов COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="24a73-103">Configuring COM+ CRM Components</span></span>

<span data-ttu-id="24a73-104">Компоненты CRM можно установить в серверное приложение COM+ или приложение библиотеки COM+.</span><span class="sxs-lookup"><span data-stu-id="24a73-104">CRM components can be installed into either a COM+ server application or a COM+ library application.</span></span> <span data-ttu-id="24a73-105">Однако они всегда должны выполняться в серверном приложении COM+.</span><span class="sxs-lookup"><span data-stu-id="24a73-105">However, they must always run in a COM+ server application.</span></span> <span data-ttu-id="24a73-106">Если они установлены в приложении библиотеки COM+, они недоступны для использования в клиентских процессах.</span><span class="sxs-lookup"><span data-stu-id="24a73-106">If they are installed in a COM+ library application, they are not available for use in client processes.</span></span>

<span data-ttu-id="24a73-107">Если компоненты CRM установлены в библиотечном приложении, они доступны для нескольких серверных приложений.</span><span class="sxs-lookup"><span data-stu-id="24a73-107">If the CRM components they are installed in a library application, they are available to more than one server application.</span></span> <span data-ttu-id="24a73-108">При установке в определенном серверном приложении они доступны только для этого конкретного серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="24a73-108">If installed in a specific server application, they are available only to that specific server application.</span></span>

<span data-ttu-id="24a73-109">Чтобы включить использование CRM в серверном приложении, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="24a73-109">To enable use of a CRM in a server application, use the following steps:</span></span>

1.  <span data-ttu-id="24a73-110">В разделе службы компонентов на странице свойства серверного приложения перейдите на вкладку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="24a73-110">From Component Services, under the server application properties page, click the **Advanced** tab.</span></span>

2.  <span data-ttu-id="24a73-111">Выберите параметр **Включить компенсирующие диспетчеры ресурсов** для этого серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="24a73-111">Select the **Enable compensating Resource Managers** option for that server application.</span></span> <span data-ttu-id="24a73-112">Если этот параметр не выбран, попытки использования CRM в этом серверном приложении завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="24a73-112">If this option is not selected, attempts to use a CRM within this server application will fail.</span></span>

    > [!Note]  
    > <span data-ttu-id="24a73-113">При установке в библиотечном приложении нет необходимости выбирать параметр **Включить компенсирующие диспетчеры ресурсов** для этого приложения библиотеки, но этот параметр необходимо выбрать для серверного приложения, на котором планируется запускать CRM.</span><span class="sxs-lookup"><span data-stu-id="24a73-113">If installed in a library application, it is not necessary to select the **Enable compensating Resource Managers** option for that library application, but this option must be selected for the server application in which the CRM is intended to run.</span></span>

     

<span data-ttu-id="24a73-114">В одном приложении рекомендуется устанавливать компоненты CRM Worker и CRM для конкретного CRM.</span><span class="sxs-lookup"><span data-stu-id="24a73-114">It is recommended that the CRM Worker and CRM Compensator components for a specific CRM be installed in the same application.</span></span>

<span data-ttu-id="24a73-115">Ниже приведены рекомендуемые параметры для компонентов CRM.</span><span class="sxs-lookup"><span data-stu-id="24a73-115">The recommended settings for CRM components are as follows.</span></span>



| <span data-ttu-id="24a73-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="24a73-116">Component</span></span>           | <span data-ttu-id="24a73-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="24a73-117">Settings</span></span>                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a73-118">**Рабочая роль CRM**</span><span class="sxs-lookup"><span data-stu-id="24a73-118">**CRM Worker**</span></span>      | <span data-ttu-id="24a73-119">Transaction = рекуиредсинк = Есжит = ессреадинг модель = обе (или потоковая модель = апартамент)</span><span class="sxs-lookup"><span data-stu-id="24a73-119">transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)</span></span>     |
| <span data-ttu-id="24a73-120">**Компенсатор CRM**</span><span class="sxs-lookup"><span data-stu-id="24a73-120">**CRM Compensator**</span></span> | <span data-ttu-id="24a73-121">Transaction = дисабледсинк = Дисабледжит = модель беспотоковой обработки = обе (или потоковая модель = апартамент)</span><span class="sxs-lookup"><span data-stu-id="24a73-121">transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment)</span></span> |



 

> [!Note]  
> <span data-ttu-id="24a73-122">Компоненты, использующие CRM, должны явно указывать модель потоков при регистрации.</span><span class="sxs-lookup"><span data-stu-id="24a73-122">Components that use the CRM must explicitly specify a threading model when they are registered.</span></span> <span data-ttu-id="24a73-123">Значение по умолчанию "основной контейнер потока," не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="24a73-123">The default, 'Main Thread Apartment,' is not supported.</span></span> <span data-ttu-id="24a73-124">Поддерживаются только две модели потоков — подразделение и оба.</span><span class="sxs-lookup"><span data-stu-id="24a73-124">The only two threading models supported are Apartment and Both.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="24a73-125">См. также</span><span class="sxs-lookup"><span data-stu-id="24a73-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24a73-126">Основные понятия о компенсации диспетчер ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="24a73-126">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



