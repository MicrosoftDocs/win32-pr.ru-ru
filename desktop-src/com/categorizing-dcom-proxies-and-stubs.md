---
title: Классификация прокси-серверов и заглушек DCOM
description: Классификация прокси-серверов и заглушек DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105710385"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a><span data-ttu-id="d3d1b-103">Классификация прокси-серверов и заглушек DCOM</span><span class="sxs-lookup"><span data-stu-id="d3d1b-103">Categorizing DCOM Proxies and Stubs</span></span>

<span data-ttu-id="d3d1b-104">DCOM маршалирует ссылки на объекты путем построения объектов OBJREF, содержащих идентификаторы CLSID.</span><span class="sxs-lookup"><span data-stu-id="d3d1b-104">DCOM marshals references to objects by constructing OBJREFs that contain CLSIDs.</span></span> <span data-ttu-id="d3d1b-105">Эти идентификаторы CLSID уязвимы для атак безопасности, так как в процессе маршалирования можно загрузить произвольные библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="d3d1b-105">These CLSIDs are vulnerable to security attacks because arbitrary DLLs can be loaded during marshaling.</span></span> <span data-ttu-id="d3d1b-106">Однако \_ \_ \_ при вызове [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) не может быть задан флаг еоак без пользовательского маршалирования (см. раздел [**\_ \_ возможности проверки подлинности Еоле**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span><span class="sxs-lookup"><span data-stu-id="d3d1b-106">However, the EOAC\_NO\_CUSTOM\_MARSHAL flag can be specified when calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (see [**EOLE\_AUTHENTICATION\_CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span></span> <span data-ttu-id="d3d1b-107">Установка этого флага помогает защищать серверную безопасность при использовании DCOM, поскольку снижает вероятность выполнения произвольных библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="d3d1b-107">Setting this flag helps protect server security when using DCOM because it reduces the chances of executing arbitrary DLLs.</span></span> <span data-ttu-id="d3d1b-108">Если этот флаг установлен, сервер разрешает маршалирование только идентификаторов CLSID, реализованных в ole32.dll, comadmin.dll, comsvcs.dll или es.dll или реализующих \_ идентификатор категории МАРШАЛЕРОМ CATID.</span><span class="sxs-lookup"><span data-stu-id="d3d1b-108">When this flag is set, the server allows the marshaling only of CLSIDs that are implemented in ole32.dll, comadmin.dll, comsvcs.dll, or es.dll, or that implement the CATID\_MARSHALER category ID.</span></span>

<span data-ttu-id="d3d1b-109">\_МАРШАЛЕРУ CATID — это идентификатор GUID категории компонента, который может быть связан с настраиваемым МАРШАЛЕРОМ CLSID.</span><span class="sxs-lookup"><span data-stu-id="d3d1b-109">CATID\_MARSHALER is a component category GUID that can be associated with a CLSID that is being custom marshaled.</span></span> <span data-ttu-id="d3d1b-110">Интерфейсы, настраиваемые с помощью этого идентификатора CLSID, разрешены, если \_ не задано значение еоак без \_ пользовательского \_ маршалирования через [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="d3d1b-110">The interfaces being custom marshaled with this CLSID are allowed when the EOAC\_NO\_CUSTOM\_MARSHAL is set via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3d1b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="d3d1b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3d1b-112">Категории компонентов</span><span class="sxs-lookup"><span data-stu-id="d3d1b-112">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 