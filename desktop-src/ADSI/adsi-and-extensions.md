---
title: Интеграция расширений в ADSI
description: Рекомендации, описывающие взаимодействие ADSI с расширениями.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- расширения ADSI
- ADSI и расширения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070617"
---
# <a name="how-adsi-integrates-extensions"></a><span data-ttu-id="d9523-105">Интеграция расширений в ADSI</span><span class="sxs-lookup"><span data-stu-id="d9523-105">How ADSI Integrates Extensions</span></span>

<span data-ttu-id="d9523-106">Следующие рекомендации описывают взаимодействие ADSI с расширениями.</span><span class="sxs-lookup"><span data-stu-id="d9523-106">The following guidelines describe how ADSI interacts with extensions:</span></span>

-   <span data-ttu-id="d9523-107">Что-то связано с объектом каталога ADSI.</span><span class="sxs-lookup"><span data-stu-id="d9523-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="d9523-108">Например, "LDAP://кН = Жеффсмис, OU = Sales, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="d9523-108">For example, "LDAP://CN=JeffSmith,OU=Sales,DC=Fabrikam,DC=COM".</span></span>
-   <span data-ttu-id="d9523-109">ADSI определяет, что объект находится в классе **User** .</span><span class="sxs-lookup"><span data-stu-id="d9523-109">ADSI identifies that the object is in the **user** class.</span></span>
-   <span data-ttu-id="d9523-110">ADSI выполняет поиск в реестре и определяет расширения CLSID для **пользователя**.</span><span class="sxs-lookup"><span data-stu-id="d9523-110">ADSI performs a lookup in the registry and identifies the extension CLSIDs for **user**.</span></span> <span data-ttu-id="d9523-111">Имейте в виду, что ADSI кэширует эти данные.</span><span class="sxs-lookup"><span data-stu-id="d9523-111">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="d9523-112">Что-то вызывает метод **QueryInterface** для IID \_ имекстенсион.</span><span class="sxs-lookup"><span data-stu-id="d9523-112">Something calls the **QueryInterface** method for IID\_IMyExtension.</span></span> <span data-ttu-id="d9523-113">ADSI ищет интерфейсы, связанные с объектом **пользователя** , начиная с собственных интерфейсов, а затем анализируя интерфейсы расширения.</span><span class="sxs-lookup"><span data-stu-id="d9523-113">ADSI searches the interfaces associated with the **user** object, starting with its own interfaces, then looking at extension interfaces.</span></span>
-   <span data-ttu-id="d9523-114">Если найдено совпадение, ADSI создает экземпляр компонента, который поддерживает IID \_ имекстенсион, и вызывает **QueryInterface** для расширения.</span><span class="sxs-lookup"><span data-stu-id="d9523-114">If a match is found, ADSI creates an instance of the component that supports IID\_IMyExtension, and calls **QueryInterface** for the extension.</span></span> <span data-ttu-id="d9523-115">Полученный интерфейс возвращается.</span><span class="sxs-lookup"><span data-stu-id="d9523-115">The resulting interface is returned.</span></span>
-   <span data-ttu-id="d9523-116">Пользователь использует этот интерфейс для вызова методов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d9523-116">The user uses this interface to call the interface methods.</span></span>
-   <span data-ttu-id="d9523-117">Затем клиент вызывает **QueryInterface** для IID \_ ийаурекстенсион, который находится в другом компоненте.</span><span class="sxs-lookup"><span data-stu-id="d9523-117">Next, the client calls **QueryInterface** for IID\_IYourExtension, which is in a different component.</span></span> <span data-ttu-id="d9523-118">Этот компонент делегирует этот вызов **QueryInterface** интерфейсу [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) агрегатора, который, в свою очередь, является самим ADSI.</span><span class="sxs-lookup"><span data-stu-id="d9523-118">This component delegates this **QueryInterface** call to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the aggregator, which happens to be ADSI itself.</span></span>
-   <span data-ttu-id="d9523-119">Опять же, ADSI ищет интерфейсы и создает экземпляр компонента.</span><span class="sxs-lookup"><span data-stu-id="d9523-119">Again, ADSI searches the interfaces and creates the component instance.</span></span>

 

 