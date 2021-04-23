---
description: Представление функциональных возможностей
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Представление функциональных возможностей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911123"
---
# <a name="representing-functionality"></a><span data-ttu-id="f243a-103">Представление функциональных возможностей</span><span class="sxs-lookup"><span data-stu-id="f243a-103">Representing Functionality</span></span>

<span data-ttu-id="f243a-104">Существуют функциональные объекты, которые позволяют вычислить или логически сгруппировать возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="f243a-104">Functional objects exist to identify or logically group feature capabilities of a device.</span></span> <span data-ttu-id="f243a-105">Например, приложение может видеть, что устройство поддерживает SMS, выполняя поиск функционального объекта SMS.</span><span class="sxs-lookup"><span data-stu-id="f243a-105">For example, an application can see that a device supports SMS by looking for the SMS functional object.</span></span> <span data-ttu-id="f243a-106">Аналогичным образом приложение может видеть, что устройство имеет возможности камеры, выполняя поиск функционального объекта захвата образа.</span><span class="sxs-lookup"><span data-stu-id="f243a-106">Similarly, the application can see that a device has camera capabilities by looking for the Still Image Capture functional object.</span></span>

<span data-ttu-id="f243a-107">Это гибкое представление объекта помогает обеспечить простую поддержку устройств с несколькими функциями.</span><span class="sxs-lookup"><span data-stu-id="f243a-107">This flexible object representation helps enable easy support for devices with multi-function capabilities.</span></span> <span data-ttu-id="f243a-108">Драйверы могут просто предоставлять любые функциональные объекты, представляющие их устройства, что более детально, чем использование традиционных классов устройств.</span><span class="sxs-lookup"><span data-stu-id="f243a-108">Drivers can simply expose whatever functional objects represent their device, which is more granular than using traditional device classes.</span></span> <span data-ttu-id="f243a-109">Представление объекта также помогает изолировать перекрывающиеся функциональные элементы. Например, некоторые телефоны могут иметь две камеры или четыре хранилища.</span><span class="sxs-lookup"><span data-stu-id="f243a-109">The object representation also helps isolate overlapping functional pieces; for example, some phones may have two cameras or four storages.</span></span>

<span data-ttu-id="f243a-110">В операционной системе Windows 7 службы расширяют функциональные объекты путем предоставления обширных запросов возможностей и абстрактного группирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="f243a-110">In the Windows 7 operating system, services extend functional objects by providing rich queries of capabilities and an abstract grouping of content.</span></span> <span data-ttu-id="f243a-111">Приложения могут использовать службы для обнаружения возможностей устройства и более эффективного взаимодействия с содержимым.</span><span class="sxs-lookup"><span data-stu-id="f243a-111">Applications can use services to discover device capabilities and to interact with content more efficiently.</span></span> <span data-ttu-id="f243a-112">Например, приложение может видеть, что устройство поддерживает возможности синхронизации контактов путем поиска объекта службы Contacts и может найти все контакты как дочерние объекты объекта службы без рекурсивного поиска в иерархии хранилища.</span><span class="sxs-lookup"><span data-stu-id="f243a-112">For example, an application can see that a device supports the contacts-synchronization capabilities by looking for a Contacts service object, and can find all contacts as child objects of the service object, without having to recursively search the storage hierarchy.</span></span>

<span data-ttu-id="f243a-113">Службы также позволяют приложениям обнаруживать и вызывать пользовательское поведение на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f243a-113">Services also allow applications to discover and invoke custom behavior on a device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f243a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f243a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f243a-115">**Общие сведения о приложении**</span><span class="sxs-lookup"><span data-stu-id="f243a-115">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



