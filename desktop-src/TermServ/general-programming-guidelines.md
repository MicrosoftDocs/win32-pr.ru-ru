---
title: Общие рекомендации по программированию
description: Рекомендации по разработке приложений в среде службы удаленных рабочих столов.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681648"
---
# <a name="general-programming-guidelines"></a><span data-ttu-id="25e65-103">Общие рекомендации по программированию</span><span class="sxs-lookup"><span data-stu-id="25e65-103">General programming guidelines</span></span>

<span data-ttu-id="25e65-104">В следующих разделах приводятся общие рекомендации по разработке приложений в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="25e65-104">The following sections provide general guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="25e65-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="25e65-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="25e65-106">Уровень совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="25e65-106">Application compatibility layer</span></span>](application-compatibility-layer.md)
</dt> <dd>

<span data-ttu-id="25e65-107">Для запуска устаревших приложений в среде службы удаленных рабочих столов можно использовать службы удаленных рабочих столов уровень совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="25e65-107">To run legacy applications in a Remote Desktop Services environment you can use the Remote Desktop Services Application Compatibility layer.</span></span>

</dd> <dt>

[<span data-ttu-id="25e65-108">Рекомендации для клиентских и серверных приложений</span><span class="sxs-lookup"><span data-stu-id="25e65-108">Client/Server application guidelines</span></span>](client-server-application-guidelines.md)
</dt> <dd>

<span data-ttu-id="25e65-109">Клиентские и серверные приложения не должны рассчитывать на то, что соединение с одним компьютером эквивалентно сеансу одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="25e65-109">Client/server applications must not assume that a single computer connection is equivalent to a single user session.</span></span>

</dd> <dt>

[<span data-ttu-id="25e65-110">Наблюдение за подключениями и отсоединениями сеансов</span><span class="sxs-lookup"><span data-stu-id="25e65-110">Monitoring session connections and disconnections</span></span>](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

<span data-ttu-id="25e65-111">Чтобы зарегистрировать приложение в службы удаленных рабочих столов, сохраните имя серверного приложения виртуального канала в реестре, добавив подраздел.</span><span class="sxs-lookup"><span data-stu-id="25e65-111">To register an application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey.</span></span>

</dd> <dt>

[<span data-ttu-id="25e65-112">Рекомендации по периферийным устройствам</span><span class="sxs-lookup"><span data-stu-id="25e65-112">Peripheral hardware guidelines</span></span>](peripheral-hardware-guidelines.md)
</dt> <dd>

<span data-ttu-id="25e65-113">Если устройство оборудования не предназначено для работы в удаленном сеансе, поставщики должны убедиться, что программное обеспечение драйвера устройства принудительно отключает перенаправление устройства, используя системную политику или групповую политику.</span><span class="sxs-lookup"><span data-stu-id="25e65-113">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

</dd> <dt>

[<span data-ttu-id="25e65-114">Связывание во время выполнения с Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="25e65-114">Run-Time linking to Wtsapi32.dll</span></span>](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

<span data-ttu-id="25e65-115">Приложение может использовать службы удаленных рабочих столов API для динамической привязки к Wtsapi32.dll во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="25e65-115">Your application can use the Remote Desktop Services API to dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="25e65-116">Для этого приложение должно вызвать функцию [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) для загрузки Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="25e65-116">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span>

</dd> </dl>

 

 