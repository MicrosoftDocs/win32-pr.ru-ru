---
description: Библиотека администрирования MTS, поставляемая с интерфейсами администрирования COM+, обеспечивает обратную совместимость с библиотекой администрирования MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Библиотека администрирования MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538807"
---
# <a name="mts-administration-library"></a><span data-ttu-id="4485e-103">Библиотека администрирования MTS</span><span class="sxs-lookup"><span data-stu-id="4485e-103">MTS Administration Library</span></span>

<span data-ttu-id="4485e-104">Библиотека администрирования MTS, поставляемая с интерфейсами администрирования COM+, обеспечивает обратную совместимость с библиотекой администрирования MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="4485e-104">The MTS Administration Library shipped with the COM+ Administration interfaces provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="4485e-105">Большая часть существующего кода администрирования MTS 2,0 по-прежнему будет работать с предоставленной библиотекой Мтсадмин. Однако некоторые функциональные возможности изменились.</span><span class="sxs-lookup"><span data-stu-id="4485e-105">Most existing MTS 2.0 administration code will still work with the MTSAdmin Library that is provided; however, some functionality has changed.</span></span>

<span data-ttu-id="4485e-106">Чтобы воспользоваться преимуществами новых функций или при первом написании кода администрирования, следует использовать библиотеку Комадмин.</span><span class="sxs-lookup"><span data-stu-id="4485e-106">To take advantage of new functionality or if you are writing administration code for the first time, you should use the COMAdmin Library.</span></span>

<span data-ttu-id="4485e-107">Следующие элементы в текущей библиотеке администрирования MTS изменяются из библиотеки администрирования MTS 2,0:</span><span class="sxs-lookup"><span data-stu-id="4485e-107">The following elements in the current MTS Administration Library are changed from the MTS 2.0 Administration Library:</span></span>

-   <span data-ttu-id="4485e-108">Интерфейс **иремотекомпонентутил** больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="4485e-108">The **IRemoteComponentUtil** interface is no longer available.</span></span>
-   <span data-ttu-id="4485e-109">Коллекция **ремотекомпонентс** больше недоступна.</span><span class="sxs-lookup"><span data-stu-id="4485e-109">The **RemoteComponents** collection is no longer available.</span></span>
-   <span data-ttu-id="4485e-110">Свойство RoleID больше не доступно, имя роли теперь используется в качестве ключа для этого.</span><span class="sxs-lookup"><span data-stu-id="4485e-110">The RoleID property is no longer available, the Role Name is now used as the key for this.</span></span>
-   <span data-ttu-id="4485e-111">Метод **експортпаккаже** больше не экспортирует client.exe.</span><span class="sxs-lookup"><span data-stu-id="4485e-111">The **ExportPackage** method no longer exports a client.exe.</span></span>
-   <span data-ttu-id="4485e-112">Свойство Ремотекомпонентинсталлпас больше не предоставляется в коллекции [**локалкомпутер**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="4485e-112">The RemoteComponentInstallPath property is no longer exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="4485e-113">Свойство Аппликатионинсталлпас больше не будет предоставляться в коллекции [**локалкомпутер**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="4485e-113">The ApplicationInstallPath property will no longer be exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="4485e-114">Системный пакет теперь называется системным приложением.</span><span class="sxs-lookup"><span data-stu-id="4485e-114">The System package is now named System Application.</span></span>
-   <span data-ttu-id="4485e-115">Пакет служебных программ теперь называется служебными программами COM+.</span><span class="sxs-lookup"><span data-stu-id="4485e-115">The Utilities package is now named COM+ Utilities.</span></span>
-   <span data-ttu-id="4485e-116">Свойство IsCollection существует в коллекции [**Components**](components.md) в мтсадмин, но будет возвращать "нотимпл", если установлен флажок и не будет сохранен, если задано значение.</span><span class="sxs-lookup"><span data-stu-id="4485e-116">The IsSystem property exists in the [**Components**](components.md) collection in MTSAdmin but will return "NotImpl" when checked and will not be saved if set.</span></span>
-   <span data-ttu-id="4485e-117">Свойство PackageName больше не поддерживается коллекцией [**Components**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="4485e-117">The PackageName property is no longer supported by the [**Components**](components.md) collection.</span></span> <span data-ttu-id="4485e-118">Чтобы выяснить имя пакета, необходимо получить PackageID, а затем найти соответствующий пакет в коллекции пакетов.</span><span class="sxs-lookup"><span data-stu-id="4485e-118">To figure out the package's name, you will now need to get the PackageID and then find the matching package in the Packages collection.</span></span>
-   <span data-ttu-id="4485e-119">Следующие свойства больше не существуют в коллекции [**интерфацесфоркомпонент**](interfacesforcomponent.md) :</span><span class="sxs-lookup"><span data-stu-id="4485e-119">The following properties no longer exist on the [**InterfacesForComponent**](interfacesforcomponent.md) collection:</span></span>
    -   <span data-ttu-id="4485e-120">**проксиклсид**</span><span class="sxs-lookup"><span data-stu-id="4485e-120">**ProxyCLSID**</span></span>
    -   <span data-ttu-id="4485e-121">**проксидлл**</span><span class="sxs-lookup"><span data-stu-id="4485e-121">**ProxyDLL**</span></span>
    -   <span data-ttu-id="4485e-122">**проксисреадингмодел**</span><span class="sxs-lookup"><span data-stu-id="4485e-122">**ProxyThreadingModel**</span></span>
    -   <span data-ttu-id="4485e-123">**типелибфиле**</span><span class="sxs-lookup"><span data-stu-id="4485e-123">**TypeLibFile**</span></span>
    -   <span data-ttu-id="4485e-124">**типелибид**</span><span class="sxs-lookup"><span data-stu-id="4485e-124">**TypeLibID**</span></span>
    -   <span data-ttu-id="4485e-125">**типелиблангид**</span><span class="sxs-lookup"><span data-stu-id="4485e-125">**TypeLibLangID**</span></span>
    -   <span data-ttu-id="4485e-126">**типелибплатформ**</span><span class="sxs-lookup"><span data-stu-id="4485e-126">**TypeLibPlatform**</span></span>
    -   <span data-ttu-id="4485e-127">**TypeLibVersion**</span><span class="sxs-lookup"><span data-stu-id="4485e-127">**TypeLibVersion**</span></span>

## <a name="related-topics"></a><span data-ttu-id="4485e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4485e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4485e-129">Автоматическое преобразование из MTS</span><span class="sxs-lookup"><span data-stu-id="4485e-129">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="4485e-130">Результаты и проблемы преобразования COM+</span><span class="sxs-lookup"><span data-stu-id="4485e-130">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="4485e-131">Ручное преобразование из MTS</span><span class="sxs-lookup"><span data-stu-id="4485e-131">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> </dl>

 

 



