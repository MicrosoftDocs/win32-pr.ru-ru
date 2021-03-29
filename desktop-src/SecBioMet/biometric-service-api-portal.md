---
title: Биометрическая платформа Windows
description: Вы можете использовать биометрическая платформа Windows API для создания клиентских приложений, которые безопасно захватывают, сохраняют и сравнивают биометрические данные конечного пользователя.
ms.assetid: d9ac9ec1-bb34-402d-a590-73d5070b97ba
keywords:
- API биометрическая платформа Windows API биометрическая платформа Windows
- API-интерфейс биометрическая платформа Windows биометрическая платформа Windows API, Домашняя страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4341f09f3141e1be77bcdf0987ee1273ffddcf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778977"
---
# <a name="windows-biometric-framework"></a><span data-ttu-id="b15fb-105">Биометрическая платформа Windows</span><span class="sxs-lookup"><span data-stu-id="b15fb-105">Windows Biometric Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="b15fb-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="b15fb-106">Purpose</span></span>

<span data-ttu-id="b15fb-107">Вы можете использовать биометрическая платформа Windows API для создания клиентских приложений, которые безопасно захватывают, сохраняют и сравнивают биометрические данные конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b15fb-107">You can use the Windows Biometric Framework API to create client applications that securely capture, save, and compare end-user biometric information.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b15fb-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="b15fb-108">Developer audience</span></span>

<span data-ttu-id="b15fb-109">Разработчики, использующие этот API, должны быть знакомы с языками программирования C и C++ и средой программирования на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="b15fb-109">Developers who use this API should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b15fb-110">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="b15fb-110">Run-time requirements</span></span>

<span data-ttu-id="b15fb-111">Биометрическая платформа Windows API поддерживается начиная с Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b15fb-111">The Windows Biometric Framework API is supported beginning with Windows Server 2008 R2 and Windows 7.</span></span> <span data-ttu-id="b15fb-112">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="b15fb-112">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b15fb-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b15fb-113">In this section</span></span>



| <span data-ttu-id="b15fb-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="b15fb-114">Topic</span></span>                                                                                       | <span data-ttu-id="b15fb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b15fb-115">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b15fb-116">Обзор биометрической платформы</span><span class="sxs-lookup"><span data-stu-id="b15fb-116">Biometric Framework overview</span></span>](biometric-framework-overview.md)<br/>                 | <span data-ttu-id="b15fb-117">Описывает встроенную поддержку биометрии в Windows.</span><span class="sxs-lookup"><span data-stu-id="b15fb-117">Describes the native support for biometrics in Windows.</span></span><br/>                                                                                       |
| [<span data-ttu-id="b15fb-118">Создание клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="b15fb-118">Creating client applications</span></span>](creating-client-applications.md)<br/>                 | <span data-ttu-id="b15fb-119">Клиентский API можно использовать для записи и использования биометрических данных в приложениях.</span><span class="sxs-lookup"><span data-stu-id="b15fb-119">You can use the client API to capture and use biometric information in your applications.</span></span><br/>                                                     |
| [<span data-ttu-id="b15fb-120">Создание подключаемых модулей адаптера</span><span class="sxs-lookup"><span data-stu-id="b15fb-120">Creating Adapter Plug-ins</span></span>](creating-adapter-plug-ins.md)<br/>                       | <span data-ttu-id="b15fb-121">Вы можете создавать адаптеры подсистемы, адаптеры датчика и адаптеры хранилища, используя подразделы этого раздела.</span><span class="sxs-lookup"><span data-stu-id="b15fb-121">You can create engine adapters, sensor adapters, and storage adapters using the topics in this section.</span></span><br/>                                       |
| [<span data-ttu-id="b15fb-122">Создание частного пула датчиков</span><span class="sxs-lookup"><span data-stu-id="b15fb-122">Creating a Private Sensor Pool</span></span>](creating-a-private-sensor-pool.md)<br/>             | <span data-ttu-id="b15fb-123">Существует два типа пулов датчиков: частный и системный.</span><span class="sxs-lookup"><span data-stu-id="b15fb-123">There are two types of sensor pools: private and system.</span></span> <span data-ttu-id="b15fb-124">В этом разделе описываются все и объясняется, как создать частный пул датчиков.</span><span class="sxs-lookup"><span data-stu-id="b15fb-124">This section describes each and explains how to create a private sensor pool.</span></span> <br/>       |
| [<span data-ttu-id="b15fb-125">Справочник по биометрическая платформа Windows API</span><span class="sxs-lookup"><span data-stu-id="b15fb-125">Windows Biometric Framework API Reference</span></span>](biometric-service-api-reference.md)<br/> | <span data-ttu-id="b15fb-126">Подробное описание функций, структур и других элементов программирования, которые можно использовать для создания клиентских приложений и подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="b15fb-126">Detailed descriptions of functions, structures, and other programming elements that can be used to create a client applications and plug-ins.</span></span><br/> |



 

 

 





