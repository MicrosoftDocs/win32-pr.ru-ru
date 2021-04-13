---
title: Позднее связывание, что происходит внутри
description: В этом разделе описывается работа позднего связывания в ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- расширения ADSI, позднее связывание, что происходит внутри
- Привязка к AD, позднее связывание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488276"
---
# <a name="late-binding-whats-happening-under-the-hood"></a><span data-ttu-id="50dbc-105">Позднее связывание: что происходит внутри?</span><span class="sxs-lookup"><span data-stu-id="50dbc-105">Late Binding: What's Happening Under the Hood?</span></span>

<span data-ttu-id="50dbc-106">В следующем списке описан общий процесс выполнения поздней привязки:</span><span class="sxs-lookup"><span data-stu-id="50dbc-106">The following list outlines the general process for performing a late bind:</span></span>

-   <span data-ttu-id="50dbc-107">Что-то связано с объектом каталога ADSI.</span><span class="sxs-lookup"><span data-stu-id="50dbc-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="50dbc-108">Например, "LDAP://кН = Жеффсмис, OU = Sales, DC = Fabrikam, DC = COM" привязывается с помощью позднего связывания COM.</span><span class="sxs-lookup"><span data-stu-id="50dbc-108">For example, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" binds using COM late binding.</span></span> <span data-ttu-id="50dbc-109">Это приводит к тому, что ADSI вызывает метод [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в интерфейсе **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="50dbc-109">This causes ADSI to call the [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) method on the **IDispatch** interface.</span></span>
-   <span data-ttu-id="50dbc-110">ADSI находит объект в классе User и создает объект, поддерживающий соответствующие интерфейсы, такие как [**iAds**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span><span class="sxs-lookup"><span data-stu-id="50dbc-110">ADSI finds an object in the user class and creates an object that supports the appropriate interfaces, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span></span>
-   <span data-ttu-id="50dbc-111">ADSI выполняет поиск в реестре и находит расширения CLSID для пользователя.</span><span class="sxs-lookup"><span data-stu-id="50dbc-111">ADSI performs a lookup in the registry and finds extension CLSIDs for user.</span></span> <span data-ttu-id="50dbc-112">Имейте в виду, что ADSI кэширует эти данные.</span><span class="sxs-lookup"><span data-stu-id="50dbc-112">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="50dbc-113">Что-то вызывает метод **миневмесод** .</span><span class="sxs-lookup"><span data-stu-id="50dbc-113">Something makes a call to the **MyNewMethod** method.</span></span> <span data-ttu-id="50dbc-114">ADSI ищет идентификатор диспетчеризации и идентификаторы диспетчеризации для других расширений ADSI.</span><span class="sxs-lookup"><span data-stu-id="50dbc-114">ADSI looks up its dispatch ID and the dispatch IDs for other ADSI extensions.</span></span> <span data-ttu-id="50dbc-115">Затем ADSI находит расширение, которое обслуживает этот вызов, и вызывает интерфейс [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) для этого расширения.</span><span class="sxs-lookup"><span data-stu-id="50dbc-115">ADSI then finds the extension that serves this call, and calls the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>
-   <span data-ttu-id="50dbc-116">Расширение выполняет функцию.</span><span class="sxs-lookup"><span data-stu-id="50dbc-116">The extension executes the function.</span></span>
-   <span data-ttu-id="50dbc-117">Теперь модуль записи клиента вызывает метод **йоурневмесод** , используя интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) для текущего расширения.</span><span class="sxs-lookup"><span data-stu-id="50dbc-117">Now, the client writer invokes the **YourNewMethod** method using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the current extension.</span></span> <span data-ttu-id="50dbc-118">Реализация расширения **IDispatch** делегирует интерфейсу **IDispatch** для ADSI.</span><span class="sxs-lookup"><span data-stu-id="50dbc-118">The extension's **IDispatch** implementation delegates back to the **IDispatch** for ADSI.</span></span>
-   <span data-ttu-id="50dbc-119">Интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) для ADSI снова ищет соответствующее расширение или само себя, а затем вызывает соответствующее расширение с помощью интерфейса [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) для этого расширения.</span><span class="sxs-lookup"><span data-stu-id="50dbc-119">The [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) for ADSI again searches for the appropriate extension, or itself, then it calls the appropriate extension using the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>

 

 