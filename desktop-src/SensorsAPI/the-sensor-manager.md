---
description: Объект диспетчера датчиков предоставляет доступ к датчикам, доступным для использования.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: Объект диспетчера датчиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144386"
---
# <a name="the-sensor-manager-object"></a><span data-ttu-id="2498b-103">Объект диспетчера датчиков</span><span class="sxs-lookup"><span data-stu-id="2498b-103">The Sensor Manager Object</span></span>

<span data-ttu-id="2498b-104">Объект диспетчера датчиков предоставляет доступ к датчикам, доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="2498b-104">The sensor manager object provides access to the sensors that are available for your use.</span></span>

<span data-ttu-id="2498b-105">Чтобы использовать API датчика, сначала необходимо вызвать метод COM **CoCreateInstance** , чтобы создать экземпляр объекта диспетчера датчиков и получить указатель на его интерфейс с именем [**исенсорманажер**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span><span class="sxs-lookup"><span data-stu-id="2498b-105">To use the Sensor API, you must first call the COM **CoCreateInstance** method to create an instance of the sensor manager object and retrieve a pointer to its interface, named [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span></span> <span data-ttu-id="2498b-106">Диспетчер датчиков поддерживает список доступных датчиков.</span><span class="sxs-lookup"><span data-stu-id="2498b-106">The sensor manager maintains the list of available sensors.</span></span> <span data-ttu-id="2498b-107">**Исенсорманажер** можно использовать для вызова методов, извлекающих группы датчиков по категориям или по типу, или можно вызвать метод для получения конкретного датчика с помощью его уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="2498b-107">You can use **ISensorManager** to call methods that retrieve groups of sensors by category or by type, or you can call a method to retrieve a particular sensor by using its unique ID.</span></span> <span data-ttu-id="2498b-108">Диспетчер датчиков также позволяет регистрироваться для получения события, которое уведомляет вас о подключении нового датчика к платформе.</span><span class="sxs-lookup"><span data-stu-id="2498b-108">The sensor manager also enables you to register to receive an event that notifies you when a new sensor has been connected to the platform.</span></span>

<span data-ttu-id="2498b-109">Иногда диспетчер датчиков предоставляет указатель на датчик, но пользователь не включил датчик.</span><span class="sxs-lookup"><span data-stu-id="2498b-109">Sometimes, the sensor manager provides a pointer to a sensor, but the user has not enabled the sensor.</span></span> <span data-ttu-id="2498b-110">Например, можно получить значения для свойств датчика, не являющихся частными, например производителя или модели датчика, прежде чем пользователь включит датчик.</span><span class="sxs-lookup"><span data-stu-id="2498b-110">For example, you can often retrieve values for non-private sensor properties, such as the sensor manufacturer or model, before the user enables the sensor.</span></span> <span data-ttu-id="2498b-111">Эта информация может помочь решить, следует ли запросить у пользователя разрешение на использование датчика.</span><span class="sxs-lookup"><span data-stu-id="2498b-111">This information can help you to decide whether to ask the user for permission to use the sensor.</span></span> <span data-ttu-id="2498b-112">Можно вызвать [**исенсорманажер:: рекуестпермиссионс**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) , чтобы предложить пользователю включить определенный датчик или коллекцию датчиков.</span><span class="sxs-lookup"><span data-stu-id="2498b-112">You can call [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) to prompt the user to enable a particular sensor or collection of sensors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2498b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2498b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2498b-114">Управление разрешениями пользователей</span><span class="sxs-lookup"><span data-stu-id="2498b-114">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> <dt>

[<span data-ttu-id="2498b-115">Запрос разрешений пользователя</span><span class="sxs-lookup"><span data-stu-id="2498b-115">Requesting User Permissions</span></span>](requesting-user-permissions.md)
</dt> </dl>

 

 
