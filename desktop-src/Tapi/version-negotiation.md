---
description: Со временем для приложений TAPI, TAPI и поставщиков услуг могут существовать разные версии.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Согласование версий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999294"
---
# <a name="version-negotiation"></a><span data-ttu-id="1993a-103">Согласование версий</span><span class="sxs-lookup"><span data-stu-id="1993a-103">Version Negotiation</span></span>

<span data-ttu-id="1993a-104">Со временем для приложений TAPI, TAPI и поставщиков услуг могут существовать разные версии.</span><span class="sxs-lookup"><span data-stu-id="1993a-104">Over time, different versions may exist for TAPI applications, TAPI, and the service providers.</span></span> <span data-ttu-id="1993a-105">Для оптимального взаимодействия приложения TAPI необходимо знать не только версию TAPI приложения, но также и версии служб DLL, ТАПИСВР и поставщика услуг TAPI.</span><span class="sxs-lookup"><span data-stu-id="1993a-105">Optimal interoperability of a TAPI application requires knowledge of not just the application's TAPI version, but also of the TAPI DLL, TAPISVR, and service provider versions.</span></span>

<span data-ttu-id="1993a-106">Несоблюдение правильного согласования версий может привести к серьезным проблемам.</span><span class="sxs-lookup"><span data-stu-id="1993a-106">Failure to do proper version negotiation can result in serious problems.</span></span> <span data-ttu-id="1993a-107">Например, некоторые из часто используемых структур имеют члены данных, добавленные из одной версии в следующую.</span><span class="sxs-lookup"><span data-stu-id="1993a-107">For example, some heavily used structures have data members added from one version to the next.</span></span> <span data-ttu-id="1993a-108">Если размер структуры не совпадает с предполагаемым приложением или TAPI, то последствия от утечки памяти до периодического значения AVs не будут.</span><span class="sxs-lookup"><span data-stu-id="1993a-108">If the structure size does not match what the application or TAPI expects, the consequences range from memory leaks to intermittent AVs.</span></span>

<span data-ttu-id="1993a-109">Дополнительные сведения см. в разделе [Управление версиями с интерфейсом TAPI](./tapi-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="1993a-109">For additional information, see [TAPI Versioning](./tapi-versioning.md).</span></span>

<span data-ttu-id="1993a-110">**Интерфейс TAPI 2. x:** Приложения согласовываются с TAPI и ТАПИСВР во время [**линеинитиализикс**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="1993a-110">**TAPI 2.x:** Applications negotiate with TAPI and TAPISVR during [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span> <span data-ttu-id="1993a-111">Приложения выполняют согласование устройств с поставщиками услуг, вызывая [**линенеготиатеапиверсион**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) для каждой строки, которую может использовать приложение.</span><span class="sxs-lookup"><span data-stu-id="1993a-111">Applications perform device negotiation with service providers by calling [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) for each line that the application might use.</span></span>

<span data-ttu-id="1993a-112">**Интерфейс TAPI 3. x:** Нет необходимости выполнять согласование версий; Однако можно использовать [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы определить, доступен ли интерфейс в своей версии.</span><span class="sxs-lookup"><span data-stu-id="1993a-112">**TAPI 3.x:** There is no need to perform version negotiation; however, you can use [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to determine if an interface is available on their version.</span></span>

 

 
